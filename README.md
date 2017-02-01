# Open Weather Map API Client

This library shall help you integrate the Open Weather Map API to your webservice.
It is extremely lightweight and provides all necessary code.

## Code Example

Using the API is very easy - you'll only need to provide a API key (Get one [here](https://openweathermap.org/appid)) in order to use it. There are functions for retrieving different weather data by predefined conditions, like "by country and city", "by latitude and longitude", "by airport code" or even "by IP address".

```php
// By default the current conditions will be requested in english language.
$weather = (new \lfischer\openWeatherMap\API('<API-key here>'))->getByLocation('Germany', 'Dusseldorf');
```

## Future to-dos / nice-to-have

At some point I'd like to improve this client to be as readable as possible. For example:

```php
use lfischer\openWeatherMap;

$weather = (new API('<API-key here>'))
  ->getConditions()
  ->byLocation('Germany', 'Dusseldorf')
  ->fetch()
  ->asArray();
```
