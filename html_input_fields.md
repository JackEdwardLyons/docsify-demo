# Input Fields
---

### General Notes

When creating an input field please refer to the ```HTMLForm::inputField( $name, $options )``` function. 
This function allows you to create a variety of fields by passing arguments into 
the **$options** array. The most common fields are:

 - ```name``` - The input field name ( doubles as the **id** if not specified). 
 - ```value``` - The input field value.
 - ```extras``` - Any extra attributes ( id, class, onclick, size, min, max, minlength ).
 - ```placeholder``` - Placeholder text for the input.
 - ```field_type``` - The type of input ( defaults to **text** if none specified ).
 - ```write_access``` - Whether the user has permission to edit this field.

?> Use the `$extras` variable to pass in the elements attributes as a concatenated string. <br>
** For example: ** ``` $extras = ' onclick="myFunc()" class="red-text" id="custom-id" ';```.

### Basic Implementation

```
HTMLForm::inputField( 'my_awesome_text_field', [
	'field_type'   => 'text',
	'value'        => 'hey jack',
	'extras'       => 'onclick="console.log(\'hello world\')"',
	'placeholder'  => 'Enter your text here',
	'write_access' => $write_access
]);			
```


### Text 
The default input field type is 'text'. To create a very basic text input, simply include the ```name```, ```value`` parameters.

```
HTMLForm::inputField( $name, [
	'field_type'   => 'text',
	'value'        => $value
]); 
```

##### Implementation Notes
Any other notes go here.


### Number 
Number inputs have built in validation based on the HTML5 spec, however further ajax / server-side validation is required to ensure incorrect values cannot be stored. To allow decimal places, simply pass in the 'allow_decimal' parameter into the function call.

Number inputs allow additional attributes such as ```min```, ```max``` and ```step```. 

```
HTMLForm::inputField( $name, [
	'field_type'    => 'number',
	'value'         => $value,
	'allow_decimal' => TRUE,
	'extras'	    => 'min="5" max="18" step="0.5"'
]); 
```

### Hidden 
Hidden input fields only require a ```field_type``` and ```value```, as well as any ```extras```.

```
HTMLForm::inputField( $name, [
	'field_type'  => 'hidden',
	'value'       => $value,
	'extras'      => $extras
]);
```	

### Radio 
Radio inputs require a ```checked``` property. The default read only mode will show a disabled radio input.

```
HTMLForm::inputField( $name, [
	'field_type'  => 'radio',
	'value'       => $value,
	'checked'     => $value == 'Yes',
	'extras'      => $extras
]);
```

### Checkbox 
Checkbox inputs require a ```checked``` property just like a radio input. When in read only mode, checkboxes can be configured to show a SVG checkmark by setting the ```tick_mark``` parameter to TRUE. The default read only mode will show a disabled checkbox.

```
HTMLForm::inputField( $name, [
	'field_type' => 'checkbox',
	'value'      => $value,
	'checked'    => $value == 'Enabled',
	'tick_mark'  => TRUE,
	'extras'     => $extras
]);
```


### Slide Toggle
The slide toggle input is used for Boolean values. To create a slide toggle, simply pass in the ```checked``` and ```read_only``` parameters.

```
HTMLForm::toggleInput( $name, [
	'checked'   => $setting_is_true,
	'read_only' => !$write_access
]);
```


### Button
Buttons are easily customisable with the usage of the ```extras``` parameter. In addition the following field types are supported:
 - submit
 - reset

```
$onclick = ' onclick="'handleClick()" ';
$classes = ' btn btn-primary ';

HTMLForm::inputField( $name, [
	'field_type'  => 'button' / 'submit' / 'reset',
	'value'       => $value,
	'extras'      => $onclick . $classes
]);
```
