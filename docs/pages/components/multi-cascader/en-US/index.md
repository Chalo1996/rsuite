# MultiCascader

Single selection of data with hierarchical relationship structure.

## Import

<!--{include:(components/multi-cascader/fragments/import.md)}-->

## Examples

### Default

<!--{include:`basic.md`}-->

### Appearance

<!--{include:`appearance.md`}-->

### Size

<!--{include:`size.md`}-->

### Cascade

<!--{include:`cascade.md`}-->

### Default value

<!--{include:`default-value.md`}-->

### Controlled

<!--{include:`controlled.md`}-->

### Block

<!--{include:`block.md`}-->

### Placement

<!--{include:`placement.md`}-->

> Tip: When set to `auto*`, try to scroll the page, or change the browser size, it will automatically appear in the right place.

### Custom options

<!--{include:`custom.md`}-->

### Disabled and read only

<!--{include:`disabled.md`}-->

### Uncheckable

<!--{include:`uncheckable.md`}-->

### Async

<!--{include:`async.md`}-->

### Container and prevent overflow

<!--{include:`container.md`}-->

### Inline

<!--{include:`inline.md`}-->

## Accessibility

Learn more in [Accessibility](/guide/accessibility).

## Props

### `<MultiCascader>`

<!-- prettier-sort-markdown-table -->

| Property              | Type`(Default)`                                                                                         | Description                                                      |
| --------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| appearance            | 'default' &#124; 'subtle' `('default')`                                                                 | Set picker appearence                                            |
| block                 | boolean                                                                                                 | Blocking an entire row                                           |
| caretAs               | ElementType                                                                                             | Custom component for the caret icon                              |
| cascade               | boolean `(true)`                                                                                        | whether cascade select                                           |
| childrenKey           | string `('children')`                                                                                   | Set children key in data                                         |
| classPrefix           | string `('picker')`                                                                                     | The prefix of the component CSS class                            |
| cleanable             | boolean `(true)`                                                                                        | Whether the selected value can be cleared                        |
| container             | HTMLElement &#124; (() => HTMLElement)                                                                  | Sets the rendering container                                     |
| countable             | boolean `(true)`                                                                                        | Can count selected options                                       |
| data \*               | [ItemDataType][item][]                                                                                  | The data of component                                            |
| defaultOpen           | boolean                                                                                                 | Default value of open property                                   |
| defaultValue          | [ValueType][value]                                                                                      | Default values of the selected items                             |
| disabled              | boolean                                                                                                 | Disabled component                                               |
| disabledItemValues    | [ValueType][value]                                                                                      | Disabled items                                                   |
| height                | number `(320)`                                                                                          | The height of Dropdown                                           |
| inline                | boolean                                                                                                 | The menu is displayed directly when the component is initialized |
| labelKey              | string `('label')`                                                                                      | Set label key in data                                            |
| loading               | boolean `(false)`                                                                                       | Whether to display a loading state indicator                     |
| locale                | [PickerLocaleType](/guide/i18n/#pickers)                                                                | Locale text                                                      |
| menuHeight            | number `(200)`                                                                                          | Sets the height of the menu                                      |
| menuWidth             | number `(156)`                                                                                          | Sets the width of the menu                                       |
| onChange              | (value: [ValueType][value], event) => void                                                              | Callback fired when value change                                 |
| onCheck               | (value: [ValueType][value], item: [ItemDataType][item], checked: boolean, event) => void;               | Called after the checkbox state changes                          |
| onClean               | (event) => void                                                                                         | Callback fired when value clean                                  |
| onClose               | () => void                                                                                              | Callback fired when close component                              |
| onEnter               | () => void                                                                                              | Callback fired before the overlay transitions in                 |
| onEntered             | () => void                                                                                              | Callback fired after the overlay finishes transitioning in       |
| onEntering            | () => void                                                                                              | Callback fired as the overlay begins to transition in            |
| onExit                | () => void                                                                                              | Callback fired right before the overlay transitions out          |
| onExited              | () => void                                                                                              | Callback fired after the overlay finishes transitioning out      |
| onExiting             | () => void                                                                                              | Callback fired as the overlay begins to transition out           |
| onOpen                | () => void                                                                                              | Callback fired when open component                               |
| onSearch              | (searchKeyword:string, event) => void                                                                   | callback function for Search                                     |
| onSelect              | (item: [ItemDataType][item], selectedPaths: [ItemDataType][item][], event) => void                      | Callback fired when item is selected                             |
| open                  | boolean                                                                                                 | Whether open the component                                       |
| placeholder           | ReactNode `('Select')`                                                                                  | Setting placeholders                                             |
| placement             | [Placement](#code-ts-placement-code)`('bottomStart')`                                                   | The placement of component                                       |
| preventOverflow       | boolean                                                                                                 | Prevent floating element overflow                                |
| renderExtraFooter     | () => ReactNode                                                                                         | custom render extra footer                                       |
| renderMenu            | (children: object[], menu:ReactNode, parentNode?: object, layer?: number) => ReactNode                  | Customizing the Rendering Menu list                              |
| renderMenuItem        | (label:ReactNode, item: [ItemDataType][item]) => ReactNode                                              | Custom render menu items                                         |
| renderValue           | (value:[ValueType][value],selectedItems: [ItemDataType][item][],selectedElement:ReactNode) => ReactNode | Custom render selected items                                     |
| searchable            | boolean `(true)`                                                                                        | Whether you can search for options.                              |
| size                  | 'lg' &#124; 'md' &#124; 'sm' &#124; 'xs' `('md')`                                                       | A picker can have different sizes                                |
| toggleAs              | ElementType `('a')`                                                                                     | You can use a custom element for this component                  |
| uncheckableItemValues | [ValueType][value]                                                                                      | Set the option value for the check box not to be rendered        |
| value                 | [ValueType][value]                                                                                      | Specifies the values of the selected items(Controlled)           |
| valueKey              | string `('value')`                                                                                      | Set value key in data                                            |

<!--{include:(_common/types/item-data-type.md)}-->
<!--{include:(_common/types/placement-start.md)}-->

### `ts:ValueType`

```ts
type ValueType = (string | number)[];
```

[item]: #code-ts-item-data-type-code
[value]: #code-ts-value-type-code
