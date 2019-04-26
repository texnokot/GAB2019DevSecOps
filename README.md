**Global Azure Bootcamp 2019 Oslo. DevSecOps workshop**

Workshop fully focuses on implementing security practices in CI/CD pipelines. The goal of workshop is to introduce at least 2 security solutions such as WhiteSource Bolt and OWASP ZAP penetration testing tool.

**Contents**
<!-- TOC -->

- [Requirements](#requirements)
  - [MS Azure subscription](#ms-azure-subscription)
  - [MS Azure DevOps](#ms-azure-devops)
- [DevSecOps workshop steps](#devsecops-workshop-steps)
- [Additional tools after workshop](#additional-tools-after-workshop)
  - [Microsoft Security Code Analysis](#microsoft-security-code-analysis)
  - [Secure DevOps Kit (AzSK) CI/CD Extensions for Azure](#secure-devops-kit-azsk-cicd-extensions-for-azure)
  - [SonarQube extension](#sonarqube-extension)

<!-- /TOC -->
DevSecOps in Azure DevOps workshop

# Requirements
1. Microsoft Azure subscription 
2. Microsoft Azure DevOps organization
## MS Azure subscription 
If you don't have MS Azure subscription, create Azure free account here: <https://azure.microsoft.com/en-us/free/> by choosing "Start free"
## MS Azure DevOps
To create a brand new Azure DevOps Organization navigate to <https://dev.azure.com> and choose "Start free"
# DevSecOps workshop steps

In this step you should follow to the repository: <https://github.com/devsecopsbiz/technical-lab> and make following steps:
1. **Lab: Create Azure DevOps Organization** - if you don't have Azure DevOps Organization
2. **Lab: Create Azure DevOps Project** - to get prebuilt setup. You can skip step "Azure Cost Insights" extension installation as this workshop is focused purely on the security
3. **Lab: Azure DevOps CI/CD** - configure CI/CD pipelines
4. You can skip steps 2 and 3 if you have already project where you want to implement security tasks and go directly to **Lab: Security** - this step focuses on 2 security tools: WhiteSource Bolt and OWASP ZAP penetration testing tool
5. **Lab: Azure DevOps Business** - is out of the scope for current workshop, but you can try it later at self-pace.

# Additional tools after workshop

This section provides other useful tools and tasks to improve security in the software development. 

## Microsoft Security Code Analysis

The Microsoft Security Code Analysis extension is in Preview. It provides several security oriented tasks:
* **Anti-Malware Scan** - Run MpCmdRun.exe on your build artifacts - Windows Defender on microsoft.com, Windows Defender Build Task
* **BinSkim** - Cutting edge binary static analysis - BinSkim on GitHub, BinSkim Build Task
* **CredScan** - Find credentials in source code - CredScan Build Task
Risk Detection / Binary Fuzzing - Risk Detection on microsoft.com, MSRD Build Task
* **Roslyn Analyzers** - .NET managed code analysis - Roslyn Analyzers on GitHub
* **TSLint for Windows** - Linter and security rules for TypeScript - TSLint on GitHub

Since extensions are in Preview you need to go <https://secdevtools.azurewebsites.net/> and **Sign Up**. You need to write an email with Azure DevOps Organization name and Microsoft engineers will add extension to your Organization. It can takes few days. Once you get extension in your Organization you will be able to add security tasks in your Build pipelines.

## Secure DevOps Kit (AzSK) CI/CD Extensions for Azure

The CICD Extension from the Secure DevOps Kit for Azure (AzSK) contains two tasks:

* **ARM Template Checker** - a task that can check security settings in ARM templates and
* **Security Verification Tests (SVTs)** - a task that can check deployed resources for secure configuration

Install an extension from Marketplace: https://marketplace.visualstudio.com/items?itemName=azsdktm.AzSDK-task

## SonarQube extension

SonarQube extension detect bugs, vulnerabilities and code smells across project branches and pull requests.
Install an extension from Marketplace: https://marketplace.visualstudio.com/items?itemName=SonarSource.sonarqube

