# Gregory

[![Build Status](https://travis-ci.org/fiskus/gregory.svg?branch=master)](https://travis-ci.org/fiskus/gregory)
[![Davis Dependency status](https://david-dm.org/fiskus/gregory.svg)](https://david-dm.org/fiskus/gregory)
[![experimental](http://badges.github.io/stability-badges/dist/experimental.svg)](http://github.com/badges/stability-badges)

React calendar component.

## Name

There is no good and vacant names, so: calendar → Gregorian calendar → Gregory.

## [Examples](examples)

```js
var React = require('react');
var Calendar = require('gregory');

function onDatePicked(date) {
  console.log(date);
}

React.render(
  <Calendar CLASSNAME="cldr"
            UI_HAS_SIX_ROWS={false}
            ON_SELECT={onDatePicked} />,
  document.getElementById('calendar')
);
```

## Compatibility

IE9+ now, IE8+ with polyfills (shims alter environment, so that they aren't included).

## Options

There are three categories of options

### Base options

* `CLASSNAME` sets prefix for all elements classnames
* `ON_SELECT` is callback on clicked/selected cell with enabled date

### Date options

* `DATE_CURRENT` is default/current date for calendar
* All dates above `DATE_MAX` are disabled/unselectable
* All dates behind `DATE_MIN` are disabled/unselectable
* `DATE_RANGES` is array of hashes a la {FROM: new Date(), TO: new Date(), CLASSNAME: 'top-kek'}
* `DATE_SELECTS` is array of hashes a la {DATE: new Date(), CLASSNAME: 'lol'}

### UI options

* `UI_FORMAT_MONTH` sets format of current month at header ([See moment.js documentation](http://momentjs.com/docs/#/displaying/format/))
* `UI_HAS_SIX_ROWS` sets showing of six rows always even for February
* `UI_HAS_WEEKDAYS` sets visibility of header with weekdays captions
* `UI_MONTHS_NUMBER` sets number of months
* `UI_TEXT_NEXT` sets caption for next-month button
* `UI_TEXT_PREV` sets caption for prev-month button
* `UI_WEEKDAYS` is array of weekdays captions

## Contributing

```
$ npm install
$ npm start # build examples and start server
$ npm test # tests and linting
```

See [gulpfile](gulpfile.js) for more usefull tasks.

* 4 spaces for indentation
* No classes or prototypes, just functions
* If function should use this.props, pass it as first argument
* Priority: simplicity > consistency > performance

## License
MIT
