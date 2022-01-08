---
theme: seriph
background: https://s3.amazonaws.com/demo.avinashdalvi.com/assets/devsecops-2022.png
class: text-white
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
  
---
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #004aad 10%, #004aad 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
<!--
Hello everyone, 
My self Avinash Shashikant Dalvi, you call me Avi. I am full stack developer and Currently working as senior software engineer at Eagleview India. I am AWS Community Builder.
Today we are going to learn about Infrastructure as code and how to keep secure
-->

<!--
Hello everyone, 
My self Avinash Shashikant Dalvi, you call me Avi. I am full stack developer and Currently working as senior software engineer at Eagleview India. I am AWS Community Builder.
Today we are going to learn about Infrastructure as code and how to keep secure
-->

---

# Agenda
- What Problem Does IaC Solve?
- What is an IaC
- Who are provider for IACs
- Keeping infrastructure as code is vulnerable ? 
- What are steps can be taken care to keep secure
- Best practices to keep IAC as secure as and scalable.
 

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->



---

# What Problem Does IaC Solve ?

The Pain of Managing IT Infrastructure

- Cost of infra
- Scalability and availability
- Monitoring and performance visibility

<!--
With the “what” out of the way, let’s turn our focus to the “why” of infrastructure as code. Why is it needed? What problem does it solve?

Infrastructure as code (IaC) means to manage your IT infrastructure using configuration files.

Infrastructure as Code evolved to solve the problem of environment drift in the release pipeline. Without IaC, teams must maintain the settings of individual deployment environments.


-->

---

# What is an IaC ?

<i>Infrastructure as code (IaC) means to manage your cloud or IT infrastructure using configuration files.</i>


<br><br>
<img src="/images/IacThoughts.png">


---

# Keeping IaC is vulnerable ? 

- Secrets and stuff in cloudformation
- Push CF directly instead of going through Git and without versioning
- Without validating directly push nested config
- Learning Curve

for some resources CF doesn't do proper cleanup of resources - so the templates should be broken down appropriately

<!--
Infrastructure as code is a powerful tool, but a risk of utilising it includes propagating small configuration mistakes across the cloud infrastructure. Misconfigurations may take several different forms, such as insecure default configurations–including nearly half of CloudFormation templates. Other forms of misconfiguration include publicly accessible S3 buckets or unencrypted databases. These issues can lead to breaches just as easily (and in some cases more easily) than exploiting a zero-day in custom code or a CVE in an open-source library.

Detecting and fixing misconfigurations helps eliminate “environmental drift”, a scenario in which the configurations for different deployment environments fall out of sync with their templates
-->

---

# Who are provider for IACs
<!-- This is a note -->
- AWS CloudFormation
- Azure Resource Manager
- Google Cloud Deployment Manager
- Terraform


<!--
There are many provider who enable IaC but these are most used providers. The first three are considered native IaC providers, and their offerings work best within their own clouds. IaC templates from all four providers can be written in JavaScript Object Notation (JSON) format, but JSON syntax can be tricky to understand, and it’s also error prone. For this reason, three of the four IaC providers have enabled the use of YAML ( which humorously stands for Yet Another Markup Language).

The only collective drawback for Cloudformation, ARM and Google Cloud Deployment Manager is they’re more suitable for their own clouds and not for organizations wishing to leverage multi-cloud environments. Here Terraform rocks. Terraform delivered IaC which encapsulates for all major cloud in one.
-->

---
class: px-20
---

# What are steps can be taken care to keep secure ?
- Prevent Hard Coded Secrets From Permeating IaC
- Reduce The Time And Impacts Of Code Leaks
- Restrict Access to Environments
- Prevent IaC Code Tampering
- Avoid Complexity
- Alert on Failures


<!--

-->

---

# IaC Best practices 
To keep IaC as secure as and scalable.
<!-- This is a note -->
- Go native whenever possible 
- But consider multi-cloud
- Also consider vendor lock-in
- Terraform
- Use an Immutable Infrastructure Approach
- Use Version Control for IaC Files
- IaC Compliance Regulation
- Don’t Store Secrets in IaC Definitions



<!-- 
IaC can be used to update resources once they are already running
The most efficient and reliable way to manage these updates is to store IaC files in a version-control system
It’s a best practice to scan IaC files automatically and continuously, ensuring that validation occurs whenever an IaC definition is created or updated.
-->

---

# Q&A, Links

* [GitHub repo (slides + sample code)]()
* [What is infrastructure as code](https://docs.microsoft.com/en-us/devops/deliver/what-is-infrastructure-as-code)
* [What Is Infrastructure as Code? How It Works, Best Practices, Tutorials](https://stackify.com/what-is-infrastructure-as-code-how-it-works-best-practices-tutorials/)
* [AWS Iac Cloudformation](https://aws.amazon.com/cloudformation/)
* Connect me on [Twitter](https://twitter.com/aviboy2006), [GitHub](https://github.com/aviboy2006), [LinkedIn](https://www.linkedin.com/in/avinash-dalvi-315b021a/)
