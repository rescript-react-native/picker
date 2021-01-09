# `@reason-react-native/picker`

[![Build Status](https://github.com/reason-react-native/picker/workflows/Build/badge.svg)](https://github.com/reason-react-native/picker/actions)
[![Version](https://img.shields.io/npm/v/@reason-react-native/picker.svg)](https://www.npmjs.com/@reason-react-native/picker)
[![Chat](https://img.shields.io/discord/235176658175262720.svg?logo=discord&colorb=blue)](https://reason-react-native.github.io/discord/)

[ReScript](https://rescript-lang.org) / [Reason](https://reasonml.github.io) bindings for
[`@react-native-picker/picker`](https://github.com/react-native-picker/picker).

Exposed as `ReactNativePicker` module.

`@reason-react-native/picker` X.y.\* means it's compatible with
`@react-native-picker/picker` X.y.\*

## Installation

When
[`@react-native-picker/picker`](https://github.com/react-native-picker/picker)
is properly installed & configured by following their installation instructions,
you can install the bindings:

```console
npm install @reason-react-native/picker
# or
yarn add @reason-react-native/picker
```

`@reason-react-native/picker` should be added to `bs-dependencies` in your
`bsconfig.json`:

```diff
{
  //...
  "bs-dependencies": [
    "reason-react",
    "reason-react-native",
    // ...
+    "@reason-react-native/picker"
  ],
  //...
}
```

## Components

### `ReactNativePicker` Component

Supported on _Android_ and _iOS_.

#### Props

| Prop Name and Type                                                                        | Notes                                                                                                                                                                                                                   |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `onValueChange:` <br /> `('a, int) => unit`                                               | Callback for when an item is selected. Takes as arguements item value of any type (`'a`) and index of the selected item as `int`.                                                                                       |
| `selectedValue: 'a`                                                                       | Value should be that of one of the items.                                                                                                                                                                               |
| `enabled: bool`                                                                           | _Android only_ <br /> Making a selection will be disabled when set to `false`.                                                                                                                                          |
| `mode`: <br /> \[&nbsp;&#124;&nbsp;`` `dialog ``&nbsp;&#124;&nbsp;`` `dropdown ``&nbsp;\] | _Android only_ <br /> Specifies how selection items will be displayed the picker is tapped. <br /> <br /> - `` `dialog ``: modal dialog (**default**) <br /> - `` `dropdown ``: dropdown anchored to the `Picker` view. |
| `prompt: string`                                                                          | _Android only_ <br /> Title of the modal dialog when `mode` is set to `` `dialog ``.                                                                                                                                    |
| `itemStyle: ReactNative.Style.t`                                                          | _iOS only_ <br /> Style to be applied to each item label. <br /> <br /> **Note:** only `Text` style props are supported.                                                                                                |

Please also see
[Reason React Native documentation of `View` props](https://reasonml-community.github.io/reason-react-native/en/docs/components/View/)
for additional supported props.

### `ReactNativePickerIOS` Component

Supported on _iOS_.

#### Props

| Prop Name and Type                          | Notes                                                                                                                             |
| ------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `onValueChange:` <br /> `('a, int) => unit` | Callback for when an item is selected. Takes as arguements item value of any type (`'a`) and index of the selected item as `int`. |
| `selectedValue: 'a`                         | Value should be that of one of the items.                                                                                         |
| `itemStyle: ReactNative.Style.t`            | Style to be applied to each item label. <br /> <br /> **Note:** only `Text` style props are supported.                            |

Please also see
[Reason React Native documentation of `View` props](https://reasonml-community.github.io/reason-react-native/en/docs/components/View/)
for additional supported props.

### `ReactNativePicker.Item` and `ReactNativePickerIOS.Item` Components

#### Props

| Prop Name and Type           | Notes                                  |
| ---------------------------- | -------------------------------------- |
| `value: 'a`                  | Value of the item.                     |
| `label: string`              | Label for the item in the `Picker`.    |
| `color: ReactNative.Color.t` | Color of the item label.               |
| `testID: string`             | ID string to locate the item in tests. |

---

## Changelog

Check the [changelog](./CHANGELOG.md) for more informations about recent
releases.

---

## Contribute

Read the
[contribution guidelines](https://github.com/reason-react-native/.github/blob/master/CONTRIBUTING.md)
before contributing.

## Code of Conduct

We want this community to be friendly and respectful to each other. Please read
[our full code of conduct](https://github.com/reason-react-native/.github/blob/master/CODE_OF_CONDUCT.md)
so that you can understand what actions will and will not be tolerated.
