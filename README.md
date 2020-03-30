# covid-usa 
## Import the latest US Covid data in JS
### See NYT for data: https://github.com/nytimes/covid-19-data


## Usage:
### Add to package.json
`npm install covid-usa`

or

```
"dependencies": {
    "covid-usa": "1.2.0"
}
```
### Access the data
```js
var covidData = require("covid-usa");

// latest state level by date
var stateData = covidData.stateData();
console.log(stateData["2020-03-20"]["California"].cases);
console.log(stateData["2020-03-20"]["California"].deaths);
console.log(stateData["2020-03-20"]["California"].fid);
console.log(stateData["2020-03-20"]["Massachusetts"]["Middlesex"].cases);

// county level data by date
var countyData = covidData.countyData();
console.log(countyData["2020-03-10"]["Middlesex"].cases);

// cached APIs to avoid redownloading latest data from NYT
var cachedStateData = covidData.stateDataCached();
var cachedCountyData = covidData.countyDataCached();
```


