# react-statecomponent

New way for state management without wrapper component

[![NPM](https://nodei.co/npm/react-statecomponent.png)](https://nodei.co/npm/react-statecomponent/)

[![install size](https://packagephobia.now.sh/badge?p=react-statecomponent)](https://packagephobia.now.sh/result?p=react-statecomponent) [![dependencies](https://david-dm.org/uxitten/react-statecomponent.svg)](https://david-dm.org/uxitten/react-statecomponent.svg)

<a href="https://www.npmjs.com/package/react-statecomponent">
  <img src="https://img.shields.io/npm/v/react-statecomponent.svg" alt="Version">
</a>

<a href="https://www.npmjs.com/package/react-statecomponent">
  <img src="https://img.shields.io/npm/l/react-statecomponent.svg" alt="License">
</a>

<a href="https://www.npmjs.com/package/react-statecomponent">
  <img src="https://img.shields.io/npm/dm/react-statecomponent.svg" alt="Downloads">
</a>

# install

```npm
npm install react-statecomponent
```

# use

## Initial state

```javascript
import { initial } from "react-statecomponent";

initial([
  {
    name: "time",
    defaultValue: 2018
  }
]);
```

## Connect to components

```javascript
import React from "react";
import { state, StateComponent } from "react-statecomponent";

class DisplayTime extends StateComponent(["time"]) {
  render() {
    return <div>{state.time}</div>;
  }
}
```

## Change state

```javascript
import { state } from "react-statecomponent";

state.time = 2019;
```
