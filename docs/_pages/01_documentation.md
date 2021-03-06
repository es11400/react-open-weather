---
layout: page
title: Documentation
permalink: /docs/
---

### Dependencies
-------------
- [Moment JS](https://momentjs.com/)
- React

### Installation
-------------
First you will need to register and account on open weather map website and obtain an [API key](https://www.apixu.com/pricing.aspx)

Next, in your project directory run:
```sh
    $ npm install react-open-weather
```
you will need to add link to weather icons css file in your html file or require it in your build process
[Weather Icons](https://erikflowers.github.io/weather-icons/), or you can directly use the CDN.

```html
  <link rel="stylesheet" 
        href="https://cdnjs.cloudflare.com/ajax/libs/weather-icons/2.0.9/css/weather-icons.min.css" 
        type="text/css"/>
```

Then in your code file you can import the component
##### Using ES2015 import
```js
import ReactWeather from 'react-open-weather';
//Optional include of the default css styles 
import 'react-open-weather/lib/css/ReactWeather.css';
```
##### Using CommonJS
```js
var ReactWeather = require('react-open-weather').default;
//Optional include of the default css styles 
require('react-open-weather/lib/css/ReactWeather.css');
```

##### UMD build is available with script tag
```html
<script src="node_modules/react-open-weather/lib/js/ReactWeather.js"></script>
```

### Usage
-------------

#### 1-Loading today weather data by city name
```html
  <ReactWeather
    forecast="today"
    apikey="YOUR_API_KEY"
    type="city"
    city="Munich"/>
```

----------

#### 2-Loading today data by longitude and latitude
```html
  <ReactWeather
    forecast="today"  
    apikey="YOUR_API_KEY"
    type="geo"
    lat="48.1351"
    lon="11.5820"
  />
```

#### 3-Loading 5 days forecast 
```html
  <ReactWeather
    forecast="5days"
    apikey="YOUR_API_KEY"
    type="city"
    city="Munich"/>
```

#### 4-Changing the the units to imperial system
```html
  <ReactWeather
    forecast="today"
    unit="imperial"
    apikey="YOUR_API_KEY"
    type="city"
    city="Munich"/>
```

## Props Options

| Props        | Options               | Default | Description                                                                |
|--------------|-----------------------|---------|----------------------------------------------------------------------------|
| **type**     | 'city', 'geo'         | geo     | Determine the data should be loaded by city name or longitude and latitude |
| **city**     |                       |         | Name of the city to show forecast for, must be provided if the type='city'|
| **lon**      |                       |         | Longitude value, must be provided if the type='geo' |
| **lat**      |                       |         | latitude value, must be provided if the type='geo'  |
| **forecast** | 'today', '5days'      | today   | Determine what forecast to show, today or today plus 4 days ahead |
| **apikey**   |                       |         | Your API key for open weather map API |
| **unit**     | 'imperial', 'meteric' | meteric | The unit system you want to use, for Meteric the temperature will be shown in Celsius and distances will be in kilometers, for Imperial the temperature will be shown in Fahrenheit and distances in miles. |

## Contribution
If you want to contribute to the project and make it better, your help is very welcome, create a pull request with your suggested feature/bug fix/ enhancements.
