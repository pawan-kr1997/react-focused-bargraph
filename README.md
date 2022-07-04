# react-focused-bargraph

> Made with create-react-library

[![NPM](https://img.shields.io/npm/v/react-focused-bargraph.svg)](https://www.npmjs.com/package/react-focused-bargraph) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## What is react-focused-bargraph?

`react-focused-bargraph` is a NPM package that helps to create bar graph best suited for responsive application with a good user experience.

## What to expect after using this package?

One can achieve the below bar graph by using this package.

![Focused Bar Graph](https://i.imgur.com/VZawnlo.gif)


## Install

```bash
npm install --save react-focused-bargraph
```

## Usage

```jsx
import React from 'react';
import {Bar} from 'react-focused-bargraph';
import 'react-focused-bargraph/dist/index.css';

const Example=()=> {
    
    //Dummy data to be passed to populate the bargraph
    let data = [
      { Date: "1/12/22", "Steps Counts": 268 },
      { Date: "2/12/22", "Steps Counts": 350 },
      { Date: "3/12/22", "Steps Counts": 200 },
      { Date: "4/12/22", "Steps Counts": 368 },
      { Date: "5/12/22", "Steps Counts": 68 },
      { Date: "6/12/22", "Steps Counts": 468 },
      { Date: "7/12/22", "Steps Counts": 68 },
      { Date: "8/12/22", "Steps Counts": 168 }
    ]
    return (
      <div>
        <h1>Implementing react-focused-bargraph</h1>
        <Bar barParentWidth="80%"
          barParentHeight="180px"
          barHeight="150px"
          xAxis="Date"
          yAxis="Steps Counts"
          barColor="linear-gradient(to right,#DB0B5F, #6F00ED)"
          barFocusColor="orange"
          data={data} />

      </div>
    )
}

export default App;
```

### Options

|Name|Type|Description |
|:---:|:---:|:---|
|barParentWidth  | `String`|It is the width of the element enclosing the bars. It accepts value in string. The value can be percentage i.e `"90%"` or pixels i.e `"300px"`
|barParentHeight | `String`|It is the height of the element enclosing the bars. It is prefered to pass this value in pixels i.e `"650px"`
|barHeight       | `String`| It is the maximum height a bar could have. The value has to less than the `barParentHeight`. For example if `barParentHeight="650px"` then `barHeight` value has to be less than `650px`
|xAxis           | `String`|`xAxis` is the name of the type of data being represented on the x-axis 
|yAxis           | `String`|`yAxis` is the name of the type of data being represented on the y-axis
|barColor        | `String`| It is the color of the bar other than the focused bar
|barFocusColor   | `String`| It is the color of the focused bar
|data            | `Array`|It is the data, skimming through which the bars will be populate.It has to be an Array of objects for eg: `[{ Date: "1/12/22", "Steps Counts": 268 },{ Date: "2/12/22", "Steps Counts": 350 },.......]`. Here in the example x-axis is Date and y-axis is Steps Counts.


## Contributing

 Everyone is welcome for contribution! Fork the repo, make some changes, submit a pull-request! if you want to play with the react application of this component library go [here](https://github.com/pawan-kr1997/Focused-BarGraph)

## License

MIT © [pawan-kr1997](https://github.com/pawan-kr1997)
