# Qwant API

<p align="center">
<img height="150" width="auto" src="https://www.qwant.com/favicon.png" /><br>
Unofficial API wrapper for qwant
</p>

## :postbox: NPM

[![](https://nodei.co/npm/qwant-api.svg?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/qwant-api)

<hr>

## :wrench: Installation

```Assembly
npm i qwant-api
```

<hr>

## :white_check_mark: Features

Qwant Feature support
  
| web | images | news | social |
| :---: | :---: | :---: | :---: |
| :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |

<hr>

## :bulb: Usage

### Search:


```javascript
qwant.search(<category>, { <options> }, <callback>{ /*...*/ });
```

Returns search results

**Categories:**

- web
- images
- news
- social

**Options:**

| Option | Required | Type | Default | Explanation |
|--------|----------|------|---------|-------------|
| `query` | **Yes** | string | none | The term(s) to search |
| `count` | no | integer | 1 | The amount of results |
| `offset` | no | integer | 0 | The index of the first result |

**Example:**

```Javascript
var qwant = require("qwant-api");

qwant.search("web", { query: "test", count: 10, offset: 1 }, function(err, data){
    if (err) return console.log(err);
    console.log(data);
});
```

### Languages:

```javascript
qwant.getLanguages(<options>);
```

Returns a list of supported languages

**Options:**

| Option | Required | Type | Default | Explanation |
|--------|----------|------|---------|-------------|
| list codes | No | boolean | false  | List languages and language codes |

**Example:**

```Javascript
var qwant = require("qwant-api");

var languages = qwant.getLanguages();

console.log(languages);
// => ['english', 'german', 'french', 'welsh', 'scottish', ... ]

var languagesAndCodes = qwant.getLanguages(true);

console.log(languagesAndCodes);
// => { english: 'en_en', german: 'de_de', french: 'fr_fr', ... }

```

<hr>

## :nut_and_bolt: Dependencies

- [request](https://www.npmjs.com/package/request)

<hr>

## :clipboard: TODO:

Everything.

<hr>

## :copyright: Copyright & Disclaimer

`Copyright (c) 2017 NullDev`

This is **NOT** an official API Wraper for [Qwant](http://qwant.com).
