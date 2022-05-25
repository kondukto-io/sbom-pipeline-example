# Initiating SBOM Creation & SCA Scan On Pipeline

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