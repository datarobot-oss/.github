# AGENTS.md

## What this repo is

The `datarobot-oss` organization profile. `profile/README.md` renders as the public
landing page at <https://github.com/datarobot-oss> — it is the first thing an
outside visitor sees. Treat every change to it as public-facing copy.

## Repo listing rules

`profile/README.md` contains a curated index of DataRobot repositories. A repository
may be listed **only** if it satisfies all three rules below. These are hard gates,
not preferences — verify each one against GitHub before adding or restoring an entry.
Never add a repo from memory, from an older revision of the README, or because it
"looks like it belongs."

### 1. Public only

Only `PUBLIC` repositories may be listed. **Never** list a private or internal repo.
A private repo linked from this page 404s for every visitor who is not an org member,
and the link itself discloses that the project exists.

### 2. Never list archived repos

Archived repositories are read-only and unmaintained. They must not appear, regardless
of how well known or widely used they once were.

### 3. Prune what is not actively maintained

Remove any repository whose last push is **9 or more months** old. An org profile that
advertises abandoned projects is worse than a shorter one. When a listed repo crosses
the 9-month line, delete its row — do not annotate it as deprecated and leave it in
place.

Apply the same 9-month test to repos in other DataRobot orgs (`datarobot`,
`datarobot-community`, `datarobot-forks`) that this page links to.

## Verifying before you edit

Check a single candidate:

```bash
gh repo view datarobot-oss/<repo> --json visibility,isArchived,pushedAt
```

Audit every repo currently linked from the profile — this prints only the rows that
violate a rule, so no output means the listing is clean:

```bash
CUTOFF=$(date -v-9m +%Y-%m-%d 2>/dev/null || date -d '9 months ago' +%Y-%m-%d)
grep -oE 'github\.com/datarobot-oss/[a-zA-Z0-9._-]+' profile/README.md |
  sed 's|.*/||' | sort -u |
  while read -r r; do
    gh repo view "datarobot-oss/$r" \
      --json name,visibility,isArchived,pushedAt \
      -q '[.name,.visibility,(.isArchived|tostring),(.pushedAt[0:10])]|@tsv' \
      2>/dev/null || printf '%s\tNOT-FOUND\t-\t-\n' "$r"
  done |
  awk -F'\t' -v c="$CUTOFF" \
    '$2!="PUBLIC" || $3=="true" || $4<c {printf "%-30s %-10s archived=%-6s %s\n",$1,$2,$3,$4}'
```

Run the audit before opening a PR that touches the listing, and re-run it periodically
— entries rot on their own as repos go quiet or get archived.

## Editing conventions

- Every repo lives in exactly one category table, as `| [name](url) | Description. |`.
- Descriptions are one sentence, ending in a period, describing what the repo is *for*
  — not its implementation.
- Keep the "Jump to a category" list in sync with the `###` headings, including the
  generated anchors. Section titles use `&amp;` for ampersands, so the matching anchor
  collapses to a double hyphen (`### 🤖 AI Agents &amp; Coding Skills` →
  `#-ai-agents--coding-skills`).
- Drop a category heading entirely when its last repo is pruned.
- Verify links resolve before committing; a broken link on the landing page is a
  visible defect.
