<div align="center">
<img src="https://raw.githubusercontent.com/clauderic/react-infinite-calendar/master/.github/logo.png" width="180"/>
</div>

# React Scroll Calendar
[![npm version](https://img.shields.io/npm/v/react-scroll-calendar.svg)](https://www.npmjs.com/package/react-scroll-calendar)
[![downloads](https://img.shields.io/npm/dm/react-scroll-calendar.svg)](https://www.npmjs.com/package/react-scroll-calendar)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](https://github.com/akbarbashakm/react-scroll-calendar/blob/master/LICENSE)
[![Total alerts](https://img.shields.io/lgtm/alerts/g/akbarbashakm/react-scroll-calendar.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/akbarbashakm/react-scroll-calendar/alerts/)
[![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/akbarbashakm/react-scroll-calendar.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/akbarbashakm/react-scroll-calendar/context:javascript)

A simple and reusable Scrollable-Calendar component for React ([Demo](https://codesandbox.io/s/wqp65ryp5))

Features
---------------

* **Scroll** – Just keep scrolling', just keep scrollin'
* **Flexible** – Min/max date and selcted date.
* **Customizeable** – Customize and theme to your heart's content.
* **Events and callbacks** – onSelect.
* **Mobile-friendly** – Silky smooth scrolling on mobile

<div style="padding:30px">
  <img src="https://raw.githubusercontent.com/akbarbashakm/react-scroll-calendar/master/logo/layout.png" width="25%"/>
  <img src="https://raw.githubusercontent.com/akbarbashakm/react-scroll-calendar/master/logo/layout2.png" width="50%" style="padding-top: 12%;vertical-align: top;"/>
</div>

Getting Started
---------------

Using [npm](https://www.npmjs.com/):
```
npm install react-scroll-calendar --save
```

Usage
------------
### Basic Example

```js
import React, { Component } from 'react';
import MobileCalendar from 'react-scroll-calendar';
import moment from 'moment';
import "react-scroll-calendar/build/react-scroll-calendar.css"; // only needs to be imported once

// Render the Calendar

render(
  <MobileCalendar
    minDate={moment('2019-01-14', 'YYYY-MM-DD')}
    selectedDate={moment('2019-01-23', 'YYYY-MM-DD')}
    maxDate={moment('2019-10-14', 'YYYY-MM-DD')}
    />,
  document.getElementById('root')
);
```

### Prop Types
| Property             | Type     | Default                | Description                                                   |                                                                               
|:---------------------|:---------|:-----------------------|:--------------------------------------------------------------|
| minDate              | moment   | `moment().add(1, 'd')` | The minimum date that is selectable.                          |
| maxDate              | moment   | `moment().add(9, 'M')` | The maximum date that is selectable.                          |
| selectedDate         | moment   | null                   | The selected date of the calendar.                            |
| className            | String   | null                   | Optional CSS class name to append to the root element.        |  
| onSelect             | Function |                        | Callback invoked after select() returns the current selected. |
| monthFormat          | String   | `MMMM`                 | Label format for the month tile.                              |
| yearFormat           | String   | `YYYY`                 | Label format for the year tile.                               |
| enableYearTitle      | Boolean   | true                  | Option to enable / disable the year in header.                |
| enableMonthTitle     | Boolean   | true                  | Option to enable / disable the month in header.               |

Compatibility
------------

### React

We're always trying to stay compatible with the latest version of React.

### Moment.js

Currently we are using Moment.js. In future we will switch to native Date objects to reduce the size of the package. Please see the example for [moment.js](https://momentjs.com/).

### Browser Support

The date picker is compatible with the latest versions of Chrome, Firefox, and IE10+.

Unfortunately, it is difficult to support legacy browsers while maintaining our ability to develop new features in the future. For IE9 support, it is known that the [classlist polyfill](https://www.npmjs.com/package/classlist-polyfill) is needed, but this may change or break at any point in the future.

Reporting Issues
----------------
If you find an [issue](https://github.com/akbarbashakm/react-scroll-calendar/issues), please report it along with any relevant details to reproduce it. The easiest way to do so is to [fork this sandbox on CodeSandbox](https://codesandbox.io/s/wqp65ryp5).

License
---------
*react-scroll-calendar* is available under the MIT License.