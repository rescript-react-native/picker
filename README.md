# BuckleScript bindings to @react-native-community/picker

[![Build Status](https://github.com/reason-react-native/picker/workflows/Build/badge.svg)](https://github.com/reason-react-native/picker/actions)
[![Version](https://img.shields.io/npm/v/@reason-react-native/picker.svg)](https://www.npmjs.com/package/@reason-react-native/picker)

These are complete BuckleScript bindings to
[`@reason-react-native/picker`](https://github.com/react-native-community/react-native-picker),
in Reason syntax.

Version `x.y.z` of `@reason-react-native/picker` should be compatible with
version `x.y.*` of `@react-native-community/picker`.

## Installation

With `yarn`:

```shell
yarn add @reason-react-native/picker
```

With `npm`:

```shell
npm install @reason-react-native/picker
```

`@react-native-community/picker` should be properly installed and linked. Please
refer to the relevant
[instructions](https://github.com/react-native-community/react-native-picker/blob/master/README.md).

Finally, `@reason-react-native/picker` should be added to `bs-dependencies` in
`BuckleScript` configuration of the project (`bsconfig.json`). For example,

```json
{
  ...
  "bs-dependencies": ["reason-react", "reason-react-native", "@reason-react-native/picker"],
  ...
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
