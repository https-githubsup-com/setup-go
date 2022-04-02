# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.

// For format details, see https://aka.ms/vscode-remote/devcontainer.json or this file's README at:
// https://github.com/microsoft/vscode-dev-containers/tree/v0.159.0/containers/java
{
  "name": "Java",
  "build": {
    "dockerfile": "Dockerfile",
    "args": {
      // Update the VARIANT arg to pick a Java version: 11, 14
      "VARIANT": "11",
      // Options
      "INSTALL_MAVEN": "true",
      "INSTALL_GRADLE": "false",
      "INSTALL_NODE": "false",
      "NODE_VERSION": "lts/*"
    }
  },

  // Set *default* container specific settings.json values on container create.
  "settings": {
    "terminal.integrated.shell.linux": "/bin/bash",
    "java.home": "/docker-java-home",
    "maven.executable.path": "/usr/local/sdkman/candidates/maven/current/bin/mvn"
  },

  // Add the IDs of extensions you want installed when the container is created.
  "extensions": [
    "vscjava.vscode-java-pack"
  ],

  // Use 'forwardPorts' to make a list of ports inside the container available locally.
  // "forwardPorts": [],

  // Use 'postCreateCommand' to run commands after the container is created.
  // "postCreateCommand": "java -version",

  // Uncomment to connect as a non-root user. See https://aka.ms/vscode-remote/containers/non-root.
  "remoteUser": "vscode"
}    
