# Weather Plugin

## Description
The Weather Plugin provides weather information for a specified location using the OpenWeather API. It fetches current weather data and forecasts based on the location provided by the user.

## Command Usage
The plugin defines a single command `weather` with the following usage:

### Command: `weather`
**Usage**: `weather [location]`  
**Description**: Retrieves the current weather and forecast for the specified location.

**Parameters**:
- `location`: The name of the location for which to retrieve weather information. This is a required parameter.

### Example Commands
- `weather London`  
  Retrieves the current weather and forecast for London.
- `weather New York`  
  Retrieves the current weather and forecast for New York.

## Properties File
The plugin uses a properties file named `weatherPlugin.properties` to store configuration settings. The file should be placed in the directory specified by the `SCRIPT_SETTINGS_DIR` environment variable.

The plugin contains this as `weatherPlugin-sample.properties` as a template which gets copied automatically upon downloading and installation

### Properties
The properties file contains the following key-value pairs:

- `OPENWEATHER_API_KEY`: The API key for accessing the OpenWeather API. This key is required to make API requests.

### Example `weatherPlugin.properties` File
'''
OPENWEATHER_API_KEY=your_api_key_here
'''

**Note**: Replace `your_api_key_here` with your actual OpenWeather API key. You can obtain an API key by signing up at [OpenWeather](https://home.openweathermap.org/users/sign_up).

## Installation
1. Ensure you have the OpenWeather API key.
2. Create or update the `weatherPlugin.properties` file in the `SCRIPT_SETTINGS_DIR` directory with the appropriate values.
3. Use the `weather` command to retrieve weather information for your desired location.

Use this plugin to easily integrate weather information into your Chatblox instance and enhance your automation capabilities.
