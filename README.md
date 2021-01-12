# vuetify-datetime-picker

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/darrenfang/vuetify-datetime-picker/blob/master/LICENSE)
[![npm version](https://img.shields.io/npm/v/vuetify-datetime-picker.svg?style=flat)](https://www.npmjs.com/package/dtp-vuetify)

DatetimePicker component for Vuetify.js.

[Online Demo](https://alexzubov.github.io/dtp-vuetify/ 'Online Demo')

[Demo Source Code](https://github.com/AlexZubov/vuetify-datetime-picker/blob/master/src/app.vue 'Demo Source Code')

## Installation

```shell
npm i dtp-vuetify
```

```js
import Vue from 'vue'
import DatetimePicker from 'dtp-vuetify'
// (Optional) import 'vuetify-datetime-picker/src/stylus/main.styl'

Vue.use(DatetimePicker)
```

If use the `main.styl`, you should configure the `stylus-loader` in `webpack.config.js`, or just ignore this style sheet.

## Usage

Once installed, it can be used in a template as simply as:

```html
<v-datetime-picker label="Select Datetime" v-model="datetime"> </v-datetime-picker>
```

## Properties

| Name             | Type        | Default Value | Description                                                                                                 |
| ---------------- | ----------- | ------------- | ----------------------------------------------------------------------------------------------------------- |
| datetime (model) | Date/String |               | Time picker model.                                                                                          |
| disabled         | Boolean     | false         | Input is disabled.                                                                                          |
| hideClearButton  | Boolean     | false         | Hide Clear button.                                                                                          |
| loading          | Boolean     | false         | Input is loading.                                                                                           |
| label            | string      |               | Sets input label.                                                                                           |
| dialogWidth      | Number      | 340           | The width of the dialog.                                                                                    |
| dateFormat       | string      | yyyy-MM-dd    | Defines the format of a date.                                                                               |
| timeFormat       | string      | HH:mm         | Defines the format of a time.                                                                               |
| clearText        | string      | CLEAR         | Sets the text of the clear button.                                                                          |
| okText           | string      | OK            | Sets the text of the ok button.                                                                             |
| textFieldProps   | Object      |               | Text fields properties. See [Vuetify Docs](https://vuetifyjs.com/en/components/text-fields 'Vuetify Docs')  |
| datePickerProps  | Object      |               | Date pickers properties.See [Vuetify Docs](https://vuetifyjs.com/en/components/date-pickers 'Vuetify Docs') |
| timePickerProps  | Object      |               | Time pickers properties.See [Vuetify Docs](https://vuetifyjs.com/en/components/time-pickers 'Vuetify Docs') |

## Events

| Name  | Arguments           | Description             |
| ----- | ------------------- | ----------------------- |
| input | value (Date/String) | The updated bound model |

## Slots

| Name     | Description                                                                                 |
| -------- | ------------------------------------------------------------------------------------------- |
| dateIcon | Slot to put custom icon in the date tab.                                                    |
| timeIcon | Slot to put custom icon in the time tab.                                                    |
| actions  | Slot to put custom buttons in the dialog.                                                   |
| progress | Slot for custom progress linear (displayed when loading prop is not equal to Boolean False) |
