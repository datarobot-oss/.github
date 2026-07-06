<p align="center">
  <a href="https://datarobot.com">
    <img src="https://af.datarobot.com/img/datarobot_logo.avif" width="600px" alt="DataRobot Logo"/>
  </a>
</p>
<h2 align="center">DataRobot OSS</h2>
<p align="center">
  <a href="https://datarobot.com">Homepage</a>
  ·
  <a href="https://docs.datarobot.com">Documentation</a>
  ·
  <a href="https://docs.datarobot.com/en/docs/get-started/troubleshooting/general-help.html">Support</a>
</p>
<p align="center">
  <a href="https://join.slack.com/t/datarobot-community/shared_invite/zt-3uzfp8k50-SUdMqeux25ok9_5wr4okrg">
    <img src="https://img.shields.io/badge/%23all--datarobot--community-a?label=Slack&labelColor=30373D&color=81FBA6" alt="Slack #all-datarobot-community">
  </a>
</p>

## DataRobot Open Source Software (OSS)

Welcome to [DataRobot](https://datarobot.com)'s open source home! 👋

Here you'll find open-source software from our Research &amp; Development and Customer-Facing teams — the tools, scripts, and libraries we use to build and work with DataRobot ourselves, shared back with the community.

### Disclaimer

These are first-party open-source repositories, provided as-is with no official support.

## DataRobot Organizations

| Organization | Contents |
| --- | --- |
| [datarobot-oss](https://github.com/datarobot-oss) | Public open source repos published by DataRobot |
| [datarobot-community](https://github.com/datarobot-community) | Public repos contributed by the community |
| [datarobot-forks](https://github.com/datarobot-forks) | Public forks of open source repos |

## Repositories

Jump to a category:

- [🤖 AI Agents &amp; Coding Skills](#-ai-agents--coding-skills)
- [🧠 GenAI Libraries](#-genai-libraries)
- [⌨️ CLI &amp; Command-Line Tools](#️-cli--command-line-tools)
- [🏗️ Infrastructure as Code](#️-infrastructure-as-code)
- [☸️ Kubernetes &amp; Helm](#️-kubernetes--helm)
- [🔁 CI/CD, GitHub Actions &amp; Automation](#-cicd-github-actions--automation)
- [🚀 Application Templates &amp; Samples](#-application-templates--samples)
- [🔌 Integrations &amp; Support Tooling](#-integrations--support-tooling)

### 🤖 AI Agents &amp; Coding Skills

Bring DataRobot into your AI coding agents and build more reliable agentic systems.

| Repository | Description |
| --- | --- |
| [datarobot-agent-skills](https://github.com/datarobot-oss/datarobot-agent-skills) | Skills that bring DataRobot platform capabilities to your coding agents (Claude Code, Cursor, and more). |
| [tensile](https://github.com/datarobot-oss/tensile) | Enhances agent reliability through trajectory analysis and remediation. |
| [datarobot-agent-tester](https://github.com/datarobot-oss/datarobot-agent-tester) | Generate, test, and improve `AGENTS.md` files and AI coding skills via the DataRobot LLM Gateway. |
| [agent-tool-templates](https://github.com/datarobot-oss/agent-tool-templates) | Agent tool functions and worked examples. |

### 🧠 GenAI Libraries

| Repository | Description |
| --- | --- |
| [datarobot-genai](https://github.com/datarobot-oss/datarobot-genai) | The `datarobot-genai` library for building generative AI applications on DataRobot. |

### ⌨️ CLI &amp; Command-Line Tools

| Repository | Description |
| --- | --- |
| [cli](https://github.com/datarobot-oss/cli) | The DataRobot command-line interface. |
| [homebrew-taps](https://github.com/datarobot-oss/homebrew-taps) | Homebrew tap housing DataRobot's binary casks for easy installation on macOS. |
| [drgithelper](https://github.com/datarobot-oss/drgithelper) | Git credentials helper binary used by DataRobot Notebooks. |
| [install-prereqchecker](https://github.com/datarobot-oss/install-prereqchecker) | CLI tool that verifies a target environment meets DataRobot installation requirements. |

### 🏗️ Infrastructure as Code

Provision the cloud infrastructure required to run DataRobot.

| Repository | Description |
| --- | --- |
| [terraform-aws-dr-infra](https://github.com/datarobot-oss/terraform-aws-dr-infra) | Terraform module for the base infrastructure required to run DataRobot on AWS. |
| [terraform-azurerm-dr-infra](https://github.com/datarobot-oss/terraform-azurerm-dr-infra) | Terraform module for the base infrastructure required to run DataRobot on Azure. |
| [terraform-google-dr-infra](https://github.com/datarobot-oss/terraform-google-dr-infra) | Terraform module for the base infrastructure required to run DataRobot on Google Cloud. |
| [datarobot-pulumi-utils](https://github.com/datarobot-oss/datarobot-pulumi-utils) | Pulumi custom resources and utilities built on top of the `pulumi-datarobot` provider. |

### ☸️ Kubernetes &amp; Helm

| Repository | Description |
| --- | --- |
| [helm-datarobot-plugin](https://github.com/datarobot-oss/helm-datarobot-plugin) | Helm plugin providing DataRobot-specific chart tooling. |
| [helm-charts](https://github.com/datarobot-oss/helm-charts) | Helm charts published by DataRobot. |

### 🔁 CI/CD, GitHub Actions &amp; Automation

Reusable automation for building, deploying, and managing DataRobot workloads.

| Repository | Description |
| --- | --- |
| [github-actions](https://github.com/datarobot-oss/github-actions) | Open-source GitHub Actions used across DataRobot repositories. |
| [custom-models-action](https://github.com/datarobot-oss/custom-models-action) | GitHub Action to manage custom inference models and deployments via CI/CD workflows. |
| [review-router](https://github.com/datarobot-oss/review-router) | GitHub Action that routes code reviews based on `CODEOWNERS`. |
| [harness-github-api-plugin](https://github.com/datarobot-oss/harness-github-api-plugin) | Swiss-army-knife plugin for GitHub API operations inside Harness pipelines. |
| [copier-template-validator](https://github.com/datarobot-oss/copier-template-validator) | Action for Application Framework components: reads specs, resolves dependencies, and renders templates. |

### 🚀 Application Templates &amp; Samples

Ready-to-use starters for building custom applications on DataRobot.

| Repository | Description |
| --- | --- |
| [react-base-app](https://github.com/datarobot-oss/react-base-app) | Base template for a Node.js + React custom application. |
| [streamlit-app-base](https://github.com/datarobot-oss/streamlit-app-base) | Ready-to-use Streamlit application template for rapid custom app development. |
| [flask-app-base](https://github.com/datarobot-oss/flask-app-base) | Ready-to-use Flask application template for rapid custom app development. |
| [slack-bot-app](https://github.com/datarobot-oss/slack-bot-app) | Ready-to-use Slack bot template for rapid custom app development. |
| [golang-app](https://github.com/datarobot-oss/golang-app) | Sample Go application. |
| [qa-app-streamlit](https://github.com/datarobot-oss/qa-app-streamlit) | Sample Q&amp;A Streamlit application. |
| [yourself-as-a-service](https://github.com/datarobot-oss/yourself-as-a-service) | Sample "as a service" application showcasing DataRobot capabilities. |
| [streamlit-sal](https://github.com/datarobot-oss/streamlit-sal) | Style and layout utilities for Streamlit applications. |
| [datarobot-asgi-middleware](https://github.com/datarobot-oss/datarobot-asgi-middleware) | Middleware for running ASGI/FastAPI applications on DataRobot. |

### 🔌 Integrations &amp; Support Tooling

| Repository | Description |
| --- | --- |
| [mlops-sap-integration](https://github.com/datarobot-oss/mlops-sap-integration) | Templates and environments for integrating DataRobot MLOps with SAP AI Core. |
| [support-scripts](https://github.com/datarobot-oss/support-scripts) | Scripts to aid support engineers during migrations and upgrades. |

