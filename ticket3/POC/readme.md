# Dependency Scanning

![dependency-scanning](https://github.com/user-attachments/assets/4220ebf9-ff06-4651-a8f4-5a723fb8135d)

| **Created**     | **Version**   | **Author** | **Comment**       | **Reviewer**      |
|:----------------:|:-------------:|:-----------:|:------------------:|:-----------------:|
| 24-02-2025       | V1            | Sahil        | Initial Commit   |                   |

## Table of Contents


1. [Introduction](#introduction)
2. [POC](#poc)
3. [Contact Information](#contact-information)
4. [References](#references)


## Introduction


## What is Dependency Scanning in CI?

**Dependency Scanning** is the process of analyzing third-party libraries and dependencies that an application relies on to detect known vulnerabilities, outdated versions, license issues, and other potential risks. This scanning is done automatically in a Continuous Integration (CI) pipeline to ensure that security issues are caught early in the development process.

CI checks, including dependency scanning, help ensure that the code integrated into the application doesn't introduce security or functional issues caused by its dependencies.

## POC


## Dependency Scanning for Java Projects

This guide outlines the steps to clone a Java project, identify the build tool (Maven or Gradle), and scan the project's dependencies for vulnerabilities using OWASP Dependency-Check.

## Step 1: Clone the GitHub Repository

First, clone the repository from GitHub:



```bash
git clone https://github.com/OT-MICROSERVICES/salary-api.git
cd salary-api
```

## Step 2: Identify the Build Tool

You need to determine which build tool the project uses. Java projects typically use either Maven or Gradle.

- **Maven Project:** Look for the `pom.xml` file.
- **Gradle Project:** Look for the `build.gradle` file.

## Step 3: Perform Dependency Scanning

### Option 1: Dependency Scanning for Maven Projects

If the project uses Maven (it has a `pom.xml` file), follow the steps below.

#### Step 1: Install Maven (if not installed)

If Maven is not installed, you can install it by following the [official Maven installation guide](https://maven.apache.org/install.html).

To check if Maven is installed, run:

```bash
mvn -v
```

#### Step 2: Run Dependency Scanning Maven dependency plugin

Navigate to the project root where the `pom.xml` file is located and use the following Maven commands.

- To view the project's dependency tree:

  ```bash
  mvn dependency:tree
  ```

  This will display all the dependencies, their versions, and any transitive dependencies.
![Screenshot (3)](https://github.com/user-attachments/assets/c0996808-0440-4926-9344-2c4e207ef805)
![Screenshot (4)](https://github.com/user-attachments/assets/c5a7216d-0609-465c-b945-2ad76e70d5b5)

- To check for outdated dependencies:

  ```bash
  mvn versions:display-dependency-updates
  ```
![Screenshot (5)](https://github.com/user-attachments/assets/bc0133f3-a303-4eb2-ae7e-d86f162faafe)
![Screenshot (6)](https://github.com/user-attachments/assets/453e12d2-e2a1-4278-af7c-54292da7f0eb)

  This will list any dependencies that have newer versions available.




## Contact Information

|    NAME           |   Email Address                       |
|:-----------------:|:-------------------------------------:|
|Sahil  | 

---


## References


 **Maven Dependency Plugin** - [https://maven.apache.org/plugins/maven-dependency-plugin/](https://maven.apache.org/plugins/maven-dependency-plugin/)
