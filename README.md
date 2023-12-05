# THIS IS NPM from https://www.npmjs.com/package/react-html-table-to-excel?activeTab=readme
# https://github.com/zsusac/ReactHTMLTableToExcel
# i create new NPM Because i need xlsx format

# ReactHTMLTableToExcel
Provides a client side generation of Excel (.xlsx) file from HTML table element.

[![Build Status](https://travis-ci.org/zsusac/ReactHTMLTableToExcel.svg?branch=master)](https://travis-ci.org/zsusac/ReactHTMLTableToExcel)

[![NPM](https://nodei.co/npm/react-html-table-to-excel.png)](https://npmjs.org/package/react-html-table-to-excel)

___
No additional dependencies
___

## Installation

```
npm install --save react-html-table-to-excel
```

## Features

* Download HTML table as Excel file in .xlsx format
* No server side code
* Set desired .xlsx filename and sheet
* Set desired class name and id for styling
* Supported IE 11

## Options

A list of available properties can be found below. These must be passed to the containing `ReactHTMLTableToExcel` component.

Property | Type | Description
----- | ----- | -----
**table** | *string* | ID attribute of HTML table element.
**filename** | *string* | Name of Excel file.
**sheet** | *string* | Name of Excel sheet.
**id** | *string* | ID attribute of button element.
**className** | *string* | Class attribute of button element.
**buttonText** | *string* | Button text.


## Example

```javascript
import React, {Component} from 'react';
import ReactHTMLTableToExcel from 'react-html-table-to-excel';

class Test extends Component {

    constructor(props) {
        super(props);
    }

    render() {

        return (
            <div>
                <ReactHTMLTableToExcel
                    id="test-table-xlsx-button"
                    className="download-table-xlsx-button"
                    table="table-to-xlsx"
                    filename="tablexlsx"
                    sheet="tablexlsx"
                    buttonText="Download as XLSX"/>
                <table id="table-to-xlsx">
                    <tr>
                        <th>Firstname</th>
                        <th>Lastname</th>
                        <th>Age</th>
                    </tr>
                    <tr>
                        <td>Jill</td>
                        <td>Smith</td>
                        <td>50</td>
                    </tr>
                    <tr>
                        <td>Eve</td>
                        <td>Jackson</td>
                        <td>94</td>
                    </tr>
                </table>

            </div>
        );
    }
}

export default Test
```
