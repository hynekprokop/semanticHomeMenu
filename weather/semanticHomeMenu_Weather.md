## semanticHomeMenu - Weather

![grafik](https://github.com/hmerk/semanticHomeMenu/raw/main/screenshots/Weather.jpg)

This Weather Widget was inspired by the iOS Weather Widget.

## Configuration and Use
No additional configuration is needed. Just create the following Items and change the channels according to your needs.
Please note, the temperature bars mostly appear after a menu change only. We have to figure out why.
```csv
Group                       owmWeather                                                      "Weather Data"                        <climate>                                                                   ["WeatherService"]
Group:Number:Temperature:MIN  minTempForecastDays                                           "Minimum forecasted temperature for next 6 days"                  
Group:Number:Temperature:MAX  maxTempForecastDays                                           "Maximum forecasted temperature for next 6 days"                  
// Local weather and forecast Thing
String                      Localweatherandforecast_StationName                             "Station Name"                                              (owmWeather)                                          ["Point"]                          {channel="openweathermap:weather-and-forecast:account:local:station#name"}
// OneCall API Thing
DateTime                    OneCallAPIweatherandforecast_Current_Sunrise                    "Current Sunrise"                     <Time>                (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:current#sunrise"}
DateTime                    OneCallAPIweatherandforecast_Current_Sunset                     "Current Sunset"                      <Time>                (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:current#sunset"}
String                      OneCallAPIweatherandforecast_Current_Condition                  "Current Condition"                   <Sun_Clouds>          (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:current#condition"}
Number:Temperature          OneCallAPIweatherandforecast_Current_Temperature                "Current Temperature"                 <Temperature>         (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:current#temperature"}
DateTime                    OneCallAPIweatherandforecast_ForecastHours01_Timestamp          "Forecast Timestamp Hours 01"         <Time>                (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours01#time-stamp"}
String                      OneCallAPIweatherandforecast_ForecastHours01_Iconid             "Forecast Icon Id Hours 01"                                 (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours01#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastHours01_Temperature        "Forecast Temperature Hours 01"       <Temperature>         (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours01#temperature"}
DateTime                    OneCallAPIweatherandforecast_ForecastHours02_Timestamp          "Forecast Timestamp Hours 02"         <Time>                (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours02#time-stamp"}
String                      OneCallAPIweatherandforecast_ForecastHours02_Iconid             "Forecast Icon Id Hours 02"                                 (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours02#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastHours02_Temperature        "Forecast Temperature Hours 02"       <Temperature>         (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours02#temperature"}
DateTime                    OneCallAPIweatherandforecast_ForecastHours03_Timestamp          "Forecast Timestamp Hours 03"         <Time>                (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours03#time-stamp"}
String                      OneCallAPIweatherandforecast_ForecastHours03_Iconid             "Forecast Icon Id Hours 03"                                 (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours03#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastHours03_Temperature        "Forecast Temperature Hours 03"       <Temperature>         (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours03#temperature"}
DateTime                    OneCallAPIweatherandforecast_ForecastHours04_Timestamp          "Forecast Timestamp Hours 04"         <Time>                (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours04#time-stamp"}
String                      OneCallAPIweatherandforecast_ForecastHours04_Iconid             "Forecast Icon Id Hours 04"                                 (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours04#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastHours04_Temperature        "Forecast Temperature Hours 04"       <Temperature>         (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours04#temperature"}
DateTime                    OneCallAPIweatherandforecast_ForecastHours05_Timestamp          "Forecast Timestamp Hours 05"         <Time>                (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours05#time-stamp"}
String                      OneCallAPIweatherandforecast_ForecastHours05_Iconid             "Forecast Icon Id Hours 05"                                 (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours05#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastHours06_Temperature        "Forecast Temperature Hours 05"       <Temperature>         (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours05#temperature"}
DateTime                    OneCallAPIweatherandforecast_ForecastHours06_Timestamp          "Forecast Timestamp Hours 06"         <Time>                (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours06#time-stamp"}
String                      OneCallAPIweatherandforecast_ForecastHours06_Iconid             "Forecast Icon Id Hours 06"                                 (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours06#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastHours06_Temperature        "Forecast Temperature Hours 06"       <Temperature>         (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastHours06#temperature"}
String                      OneCallAPIweatherandforecast_ForecastToday_Iconid               "Forecast Icon Id Today"                                    (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastToday#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastToday_Mintemperature       "Forecast Mintemperature Today"       <Temperature>         (owmWeather, minTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastToday#min-temperature"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastToday_Maxtemperature       "Forecast Maxtemperature Today"       <Temperature>         (owmWeather, maxTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastToday#max-temperature"}
String                      OneCallAPIweatherandforecast_ForecastTomorrow_Iconid            "Forecast Icon Id Tomorrow"                                 (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastTomorrow#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastTomorrow_Mintemperature    "Forecast Mintemperature Tomorrow"    <Temperature>         (owmWeather, minTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastTomorrow#min-temperature"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastTomorrow_Maxtemperature    "Forecast Maxtemperature Tomorrow"    <Temperature>         (owmWeather, maxTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastTomorrow#max-temperature"}
String                      OneCallAPIweatherandforecast_ForecastDay2_Iconid                "Forecast Icon Id Day 02"                                   (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay2#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastDay2_Mintemperature        "Forecast Mintemperature Day 02"      <Temperature>         (owmWeather, minTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay2#min-temperature"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastDay2_Maxtemperature        "Forecast Maxtemperature Day 02"      <Temperature>         (owmWeather, maxTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay2#max-temperature"}
String                      OneCallAPIweatherandforecast_ForecastDay3_Iconid                "Forecast Icon Id Day 03"                                   (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay3#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastDay3_Mintemperature        "Forecast Mintemperature Day 03"      <Temperature>         (owmWeather, minTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay3#min-temperature"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastDay3_Maxtemperature        "Forecast Maxtemperature Day 03"      <Temperature>         (owmWeather, maxTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay3#max-temperature"}
String                      OneCallAPIweatherandforecast_ForecastDay4_Iconid                "Forecast Icon Id Day 04"                                   (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay4#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastDay4_Mintemperature        "Forecast Mintemperature Day 04"      <Temperature>         (owmWeather, minTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay4#min-temperature"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastDay4_Maxtemperature        "Forecast Maxtemperature Day 04"      <Temperature>         (owmWeather, maxTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay4#max-temperature"}
String                      OneCallAPIweatherandforecast_ForecastDay5_Iconid                "Forecast Icon Id Day 05"                                   (owmWeather)                                          ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay5#icon-id"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastDay5_Mintemperature        "Forecast Mintemperature Day 05"      <Temperature>         (owmWeather, minTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay5#min-temperature"}
Number:Temperature          OneCallAPIweatherandforecast_ForecastDay5_Maxtemperature        "Forecast Maxtemperature Day 05"      <Temperature>         (owmWeather, maxTempForecastDays)                     ["Point"]                          {channel="openweathermap:onecall:account:local:forecastDay5#max-temperature"}
```
## Community
Please check [openHAB community](https://community.openhab.org/t/semantichomemenu-for-openhab-4-discussions/152202) for discussions and proposals. Do not post on the marketplace topics.

## Changelog
### Version 1.0.3
- added documentation and missing groups to show temperature bars
### Version 1.0.2
- fix incorrect sunrise and sunset items
### Version 1.0.1
- ressource link corrected
### Version 1.0
- initial release for openHAB 4

## Resources
https://github.com/hmerk/semanticHomeMenu/raw/main/weather/semanticHomeMenu_Weather.yaml