# 🏗️ Agent Installation

How to setup SOLFUNMEME eliza agent on aws:

1. setup new aws account
2. setup twitter account.
3. setup grok api key( or nvidia or openai)

The next steps require shell access until our one click cloudformation installer is working

4. setup admin user with access key (will be part of one click installer)
5. &#x20;install terraform. (will be part of one click installer)
6. set secrets in env and in ssm parameters (will be part of one click installer)
7. run terraform. (will be part of one click installer)

**One-click Installer:**

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

## Detailed Walkthrough of what you need & One-click installer:

* AWS account (free start!) 💸
* Grok account (robot's brain) 🧠
* Twitter account (robot's voice) 🐦

Click the one-click installer link 🔗, give:

* Twitter username, password, email ✉️
* Grok key 🔑

It magically:

* Creates storage 📦
* Sets up robot's computer 💻
* Installs apps 🧰
* Connects all 🔗

Notes:

* Start with free AWS account 💳
* Beginner setup (look for "dev") 👶
* If issues, delete and retry 🗑️🔄

Prerequisites:

* AWS: http://aws.amazon.com/free 🌐
* Grok: http://console.grok.com/login 🔓
* Twitter: http://wikihow.com/Make-a-Twitter-Account 📝

Regions:

* US East 1, 2 🇺🇸
* US West 1 🌵
* EU Central 1 🇪🇺
* AP South 1 🇮🇳

AI Tips:

* Use `us-east-1` for region match 🌍
* Launch Stack Button deploys from GitHub/S3 🚀
* Change URL from `us-east-2` to `us-east-1` 🔧

Example link for US East 1: [https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateURL=...\&stackName=...\&param\_S3BucketPattern=...\&param\_GroqKey=...\&param\_TokenizerImage=...\&param\_TwitterPassword=...\&param\_NameTag=...\&param\_SSMParameterPattern=...\&param\_TwitterUserName=...\&param\_LaunchTemplateVersion=...\&param\_TwitterEmail=...\&param\_AgentImage=...\&param\_AmiId=...](https://t.co/7n9jbSTWml)

Check:

* Template access in US East 1 🔐
* Valid AMI ID for region 🆔
* S3 bucket patterns for region fit 🔄

Parameters:

* `templateURL`: Template link 📋
* `stackName`: Stack ID tag 📛
* `param_S3BucketPattern`: S3 naming rule 📁
* `param_GrokKey`: Grok auth key 🔑
* `param_TokenizerImage`: Tokenizer Docker image 🐳
* `param_TwitterPassword`: Twitter pass 🔐
* `param_NameTag`: Resource tag 🏷️
* `param_SSMParameterPattern`: SSM pattern 🧩
* `param_TwitterUserName`: Twitter user 🐦
* `param_LaunchTemplateVersion`: EC2 template version 📅
* `param_TwitterEmail`: Twitter mail 📩
* `param_AgentImage`: Agent Docker image 🐳
* `param_AmiId`: AMI ID for region 🆔

Commands:

* Validate template: `aws cloudformation validate-template --template-body file://ec2.yml` ✅
* Apply Terraform: `terraform apply -auto-approve -var-file .tfvars` 🛠️

