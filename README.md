# Initiating SBOM Creation & SCA Scan On Pipeline

*In our previous blog post, we have covered what SBOM is, its advantages, how to create it, and how to detect a vulnerability with SBOM. You may find the SBOM 101 blog at [this link](https://kondukto.io/blog/sbom-software-bill-of-materials).*

*If you wish to see the blog post of this repository please click to [this link](https://kondukto.io/blog/how-to-generate-and-audit-sbom-in-a-ci-cd-pipeline).*

This repository contains a vulnerable Log4j version, do not use it in the production environment.

In this repository, you can find an example pom.xml file to understand how you can import various plugins to your Maven project. Besides that, it contains a Github Actions & Jenkins pipeline examples to guide you on how you can create/edit your pipeline according to your needs.

![Github Actions Pipeline](/assets/actions_pipeline.png)

## What is CycloneDX? 

CycloneDX is a Software Bill of Materials(SBOM) standard by OWASP and it’s designed for use in application security contexts. The CycloneDX project provides a bunch of tools for anyone to use in the desired environment. 

To use this plugin, we only need to add the following configuration to the pom.xml file:

![Codedx Maven Plugin](/assets/codedx.png)

## What is Dependency-Check?

Dependency-Check is an SCA tool. The main purpose of it to generate the dependency list and check for the known vulnerabilities via different sources like NVD, OSS Index or Github’s Security Advisory, etc. Some tools may also provide more details about their open source license. 

Here is the import block for the pom.xml file:

![Dependency-Check plugin](/assets/depcheck.png)