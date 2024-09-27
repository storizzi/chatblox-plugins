# Chatblox Plugins Repository

## Overview

The Chatblox Plugins Repository is a central hub for storing, managing, and distributing plugins for the Chatblox system. The repository is designed to provide an organized and efficient way to extend the functionality of Chatblox by adding new features, commands, and integrations.

## Purpose

The primary purpose of this repository is to facilitate the sharing and usage of plugins within the Chatblox ecosystem. By hosting plugins in a centralized location, users can easily discover, download, and install plugins to enhance their Chatblox instance.

## Structure

The repository is organized into multiple directories and files to ensure a clear and consistent structure. Here is an overview of the key components:

### Root Directory

The root directory contains the main configuration files and directories for the repository. It includes:

- **README.md**: Provides an overview of the repository, its purpose, and structure.
- **plugin-list.json**: A JSON file listing all available plugins, their details, and download methods.

### Plugin Directories

Each plugin is stored in its own directory within the repository. The directory name should match the plugin ID. Each plugin directory contains:

- **pluginName**: The name of the plugin directory, which should match the plugin ID.
  - **config.json**: The main configuration file for the plugin, including its commands, hooks, and other settings.
  - **pluginName.js**: The main JavaScript file implementing the plugin logic.
  - **script-settings/**: A subdirectory containing sample properties files that can be copied to the `script-settings` directory specified in the environment variables.
  - **README.md**: A readme file specific to the plugin, providing details about its usage, commands, and configuration settings.

### Example Structure

```
chatblox-plugins/
├── README.md
├── plugin-list.json
├── weatherPlugin/
│   ├── config.json
│   ├── weatherPlugin.js
│   ├── weatherPlugin-sample.properties
│   └── README.md
```

## plugin-list.json
The `plugin-list.json` file is a crucial component of the repository, listing all available plugins and their details. Here is an example structure for this file:

```
{
  "repositoryName": "Chatblox Plugins Repository",
  "repositoryOwner": "Simon Huggins",
  "repositoryEmail": "chatbloxrepo@simonhuggins.com",
  "lastUpdated": "2024-07-01T12:00:00Z",
  "plugins": [
    {
      "pluginName": "weatherPlugin",
      "author": "Simon Huggins",
      "email": "chatbloxrepo@simonhuggins.com",
      "downloadMethod": "git",
      "defaultBranch": "main",
      "developmentBranch": "",
      "latestRelease": "1.0.0",
      "active": true,
      "lastUpdated": "2024-07-01T12:00:00Z",
      "latestReleaseTag": "v1.0.0",
      "downloadUrl": "https://github.com/storizzi/chatblox-plugins",
      "repoSubdirectory": "weatherPlugin",
      "categories": "utilities,weather",
      "description": "Provides weather information for a specified location using the OpenWeather API.",
      "llmDescription": "The weatherPlugin command retrieves current weather data for a given location using the OpenWeather API. Usage: weather [location]"
    }
  ]
}
```
