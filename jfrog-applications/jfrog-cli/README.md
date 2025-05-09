# JFrog CLI

![](../../.gitbook/assets/jfrog-cli-header.png)

JFrog CLI is a compact and smart client that provides a simple interface that automates access to JFrog products simplifying your automation scripts and making them more readable and easier to maintain. JFrog CLI works with JFrog Artifactory, Xray, Distribution and Pipelines (through their respective REST APIs) making your scripts more efficient and reliable in several ways:

**Advanced upload and download capabilities**

JFrog CLI allows you to upload and download artifacts concurrently by a configurable number of threads that help your automated builds run faster. For big artifacts, you can define a number of chunks to split files for parallel download.

JFrog CLI optimizes both upload and download operations by skipping artifacts that already exist in their target location. Before uploading an artifact, JFrog CLI queries Artifactory with the artifact's checksum. If it already exists in Artifactory's storage, the CLI skips sending the file, and if necessary, Artifactory only updates its database to reflect the artifact upload. Similarly, when downloading an artifact from Artifactory, if the artifact already exists in the same download path, it will be skipped. With checksum optimization, long upload and download operations can be paused in the middle, and then be continued later where they were left off.

JFrog CLI supports uploading files to Artifactory using wildcard patterns, regular expressions, and ANT patterns, giving you an easy way to collect all the files you wish to upload. You can also download files using wildcard patterns.

**Support for popular package managers and build tools**

JFrog CLI offers comprehensive support for popular package managers and builds tools. It seamlessly integrates with package managers like npm, Maven, NuGet, Docker, and more, allowing you to easily manage and publish packages.

**Source code and binaries scanning**

JFrog CLI empowers you with robust scanning capabilities to ensure the security and compliance of your source code and software artifacts, including containers. It integrates with JFrog Xray and , enabling you to scan and analyze your projects and packages, including containers, for vulnerabilities, license compliance, and quality issues. With JFrog CLI, you can proactively identify and mitigate potential risks, ensuring the integrity and safety of your software supply chain.

**Support for Build-Info**

Build-Info is a comprehensive metadata Software Bill of Materials (SBOM) that captures detailed information about the components used in a build. It serves as a vital source of information, containing version history, artifacts, project modules, dependencies, and other crucial data collected during the build process. By storing this metadata in Artifactory, developers gain traceability and analysis capabilities to improve the quality and security of their builds. The Build-Info encompasses project module details, artifacts, dependencies, environment variables, and more. It is collected and outputted in a JSON format, facilitating easy access to information about the build and its components. JFrog CLI can create build-info and store the build-info in Artifactory.

#### System Requirements

JFrog CLI runs on any modern OS that fully supports the [Go programming language](https://golang.org/).

#### Contributing to JFrog CLI Documentation

We value your input in making the JFrog CLI documentation better. You can help us enhance and improve it by recommending changes and additions. To contribute, follow these steps:

Go to the documentation project on GitHub: [https://github.com/jfrog/documentation](https://github.com/jfrog/documentation) and create a pull request with your proposed changes and additions.

Your contributions will be reviewed, and if accepted, they will be merged into the documentation to benefit the entire JFrog CLI community.
