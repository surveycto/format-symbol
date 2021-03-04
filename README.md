# Format symbol

![Screenshot](extras/format-symbl.png)

## Description

This field plug-in is designed to display a symbol either before or after an input field.

[![Download now](extras/download-button.png)](https://github.com/surveycto/format-symbol/raw/master/format-symbol.fieldplugin.zip)

### Features

In addition to supporting the default SurveyCTO features listed below, this field plug-in offers the following expanded functionality:

1. **Support for RTL languages**  
    If your *label* or *hint* is in a language that uses a right-to-left alphabet (like Arabic), it will be right-justified.
1. **Support for HTML in field references**  
    If you reference another field's value in either the field *label* or field *hint*, and that referenced value contains HTML, the HTML will be correctly rendered.

### Data format

This field plug-in requires the `decimal` field type.

## How to use

### Getting started

**To use this plug-in as-is**, just download the [format-symbol.fieldplugin.zip](https://github.com/surveycto/format-symbol/raw/master/format-symbol.fieldplugin.zip) file from this repo, specify this field plug-in as a custom field appearance in the form design (like in the [sample form](https://github.com/surveycto/format-symbol/raw/master/extras/sample-form/)), and attach it to your form. For more details about using field plug-ins, please read the [user documentation](https://docs.surveycto.com/02-designing-forms/03-advanced-topics/06.using-field-plug-ins.html).

**To create your own** field plug-in using this as a template, follow these steps:

1. Fork this repo
1. Make changes to the files in the `source` directory.  
    * **Note:** be sure to update the `manifest.json` file as well.
1. Zip the updated contents of the `source` directory.
1. Rename the .zip file to *yourpluginname*.fieldplugin.zip (replace *yourpluginname* with the name you want to use for your plug-in).
1. You may then attach your new .fieldplugin.zip file to your form as normal.

For more information about developing your own field plug-ins, please read the [developer documentation](https://github.com/surveycto/Field-plug-in-resources).

### Default SurveyCTO feature support

| Feature / Property | Support |
| --- | --- |
| Supported field type(s) | `decimal`|
| Default values | Yes |
| Constraint message | Uses default behavior |
| Required message | Uses default behavior |
| media:image | Yes |
| media:audio | Yes |
| media:video | Yes |
| `show-formatted` appearance | No |

### Parameters

| Parameter key | Parameter value |
| --- | --- |
| `symbol` | The symbol to be displayed.|
| `placement` | The positioning of they symbol. This can be take two value: <br> <ol><li>`start` (default) - the symbol is on the left of the input box. </li><li>`end` - the symbol is on the right of the input box.</li></ol>|

### Example
To display a percent symbol at the end of the textbox, the following would be placed in the appearance column of the spreadsheet form definition:

custom-format-symbol(symbol='%', placement='end')

## More resources

* **Sample form**   
[Download sample form](https://github.com/surveycto/format-symbol/raw/master/extras/sample-form/test-form-package.zip)  

* **Developer documentation**  
Instructions and resources for developing your own field plug-ins.  
[https://github.com/surveycto/Field-plug-in-resources](https://github.com/surveycto/Field-plug-in-resources)

* **User documentation**  
How to get started using field plug-ins in your SurveyCTO form.  
[https://docs.surveycto.com/02-designing-forms/03-advanced-topics/06.using-field-plug-ins.html](https://docs.surveycto.com/02-designing-forms/03-advanced-topics/06.using-field-plug-ins.html)
