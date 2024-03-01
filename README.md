# @piets/homebridge-http-thermostat

Homebridge Plugin for a custom HTTP Thermostat. Sends a simple HTTP POST containing the temperature to set to a server. Reads the current temperature via a HTTP GET request.  
The plugin can be used for example with a simple Arduino sketch controlling a servo, which in turn controls the dial of an old analog thermostat.

## Installation

1. Install homebridge using: `npm install -g homebridge`
2. Install homebridge-udmx using: `npm install -g @piets/homebridge-http-thermostat`
3. Update your configuration file. See below for examples.

## Example Configuration

```
    {
        "accessory": "http-thermostat",
        "name": "Central Heating",
        "url": "https://home.com"
    }
```

## JSON Format

The JSON sent via this plugin has the following format:

```
    {
        "temperature": 21.5
    }
```

The JSON received via this plugin has the following format:

```
    {
        "targetTemperature": 21.5,
        "currentTemperature": 21.5
    }
```
