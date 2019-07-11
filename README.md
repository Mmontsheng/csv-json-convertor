![Converter banner](./images/banner.png)

![npm latest version](https://img.shields.io/npm/v/csv-json-convertor.svg?label=csv-json-convertor)
![package downloads](https://img.shields.io/npm/dw/csv-json-convertor.svg)
![licence](https://img.shields.io/npm/l/csv-json-convertor.svg?style=plastic)



# Overview
Csv-json-convertor, as its name implies, is a simple *csv-json* conversion tool. You can use it to easily convert csv files to json objects and/or files, as well as the other way around (convert json files to csv).

# Installation
**Install via npm**: `npm install csv-json-convertor` <br>
[![NPM](https://nodei.co/npm/csv-json-convertor.png)](https://npmjs.org/package/csv-json-convertor)


# Usage
After installing, import and use in your project as follows:
### CSV to JSON
```js
// require destructured toJSON function
const { toJSON } = require('csv-json-convertor');

// convert csv file
toJSON('path/to/csvFile.csv', api => {
    console.log(api.data) // log or use object (result from the conversion)
    api.save() // save new .json file (./csvFile.json by default) to current directory
});
```

You can specify save options such as `filename`, `prettify` and `spaces` as in the following examples <br>
By default: <br>
`filename`: name of the csv file <br>
`prettify`: false <br>
`spaces`: 1
```js
// filename
toJSON('path/to/csvFile.csv', api => {
    const options = {
        filename: newJsonFile
    };
    api.save(options); 
    // Output: newJsonfile.json, not prettified
}); 

// filename, prettify 
toJSON('path/to/csvFile.csv', api => {
    const options = {
        filename: newJsonFile,
        prettify: true
    };
    api.save(options); 
    // Output: newJsonfile.json, prettified using a spacing of 1
}); 

// filename, prettify, spaces
toJSON('path/to/csvFile.csv', api => {
    const options = {
        filename: newJsonFile,
        prettify: true,
        spaces: 2
    };
    api.save(options); 
    // Output: newJsonfile.json, prettified using a spacing of 2
}); 
```
![Preview of conversion to json](./images/toJsonPreview.png)

### CSV to JSON
Currently working on it :wink:

# Contributing
I need help with writing a good documentation for this project. Also, any ideas or suggestions on new features, enhancements and performance improvement are very welcome.
Feel free to contribute in anyway you can. 
