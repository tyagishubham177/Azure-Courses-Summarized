# Azure App Service

## Overview
Azure App Service is an HTTP-based service for hosting:
- Web applications
- REST APIs
- Mobile back ends

Supports development in various programming languages and frameworks, and runs on both Windows and Linux environments.

## Key Features

### Built-in Auto Scale Support
- **Scale Up/Down:** Adjusts the number of cores or RAM.
- **Scale Out/In:** Modifies the number of machine instances running the app.

### Continuous Integration/Deployment Support
- Integrates with Azure DevOps Services, GitHub, Bitbucket, FTP, or local Git.
- Auto-syncs code and changes with the web app.

### Deployment Slots
- Allows use of separate deployment slots in the Standard App Service Plan or better.
- Each slot is a live app with its own hostname.
- Content and configurations can be swapped between slots.

### App Service on Linux
- Hosts web apps natively on Linux for supported application stacks.
- Runs custom Linux containers (Web App for Containers).
- Supports languages: Node.js, Java (JRE 8 & JRE 11), PHP, Python, .NET, and Ruby.
- Allows deployment with custom containers if the runtime isn't supported by built-in images.

### Supported Languages and Versions
Retrieve the current list of supported languages and versions using:
```bash
az webapp list-runtimes --os-type linux
```

## Limitations
- Not supported on Shared pricing tier.
- Portal shows features that currently work for Linux apps.
- Disk latency for built-in images can be higher and more variable than container filesystem. For heavy read-only access, custom container options may be better.

## Summary Table

| Feature                        | Description                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| Built-in Auto Scale Support  | Scale resources up/down or in/out based on web app usage.                                          |
| Continuous Integration       | Auto-syncs code from various sources like Azure DevOps, GitHub, Bitbucket, FTP, local Git.        |
| Deployment Slots             | Separate live apps with their own hostnames for easier deployment and configuration management.   |
| App Service on Linux         | Supports web apps natively on Linux, including custom containers, with many language options.      |
| Limitations                  | Not available on Shared tier, feature visibility in portal, variable disk latency for built-in images. |

