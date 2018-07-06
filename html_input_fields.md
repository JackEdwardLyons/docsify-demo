# Input Fields
---

### General Notes

When creating an input field please refer to the ```HTMLForm::inputField( $options )``` function. 
This function allows you to create a variety of fields by passing arguments into 
the $options array. The most common fields are:

 - ```$name``` - The input field name ( doubles as the **id** if not specified).
 - ```$value``` - The input field value.
 - ```$extras``` - Any extra attributes ( id, class, onclick, size, min, max, minlength ).
 - ```$placeholder``` - Placeholder text for the input.
 - ```$field_type``` - The type of input ( defaults to **text** if none specified ).

?> Use the `$extras` variable to pass in the elements attributes as a concatenated string. <br>
** For example: ** ``` $extras = ' onclick="myFunc()" class="red-text" id="custom-id" ';```.

### Text Input

When creating an input field.

```
HTMLForm::inputField($name, [
	'field_type'  => 'text',
	'value'       => $value,
	'extras'      => $extras . ' size="5" minlength="2" ',
	'placeholder' => $placeholder
]); 
```

##### Implementation Notes
Any other notes go here.


### Number Input

Bacon ipsum dolor amet short loin pork flank shank nostrud. Aliquip anim pork loin fatback. Proident drumstick esse frankfurter quis. Sunt ad veniam, turducken shank consectetur turkey duis. Deserunt veniam cupim chicken t-bone. Cow non filet mignon tenderloin short loin. Porchetta kevin ullamco, short ribs shoulder ut pariatur laborum in aliquip rump.

### Hidden Input

Bacon ipsum dolor amet short loin pork flank shank nostrud. Aliquip anim pork loin fatback. Proident drumstick esse frankfurter quis. Sunt ad veniam, turducken shank consectetur turkey duis. Deserunt veniam cupim chicken t-bone. Cow non filet mignon tenderloin short loin. Porchetta kevin ullamco, short ribs shoulder ut pariatur laborum in aliquip rump.

### Radio Input

Bacon ipsum dolor amet short loin pork flank shank nostrud. Aliquip anim pork loin fatback. Proident drumstick esse frankfurter quis. Sunt ad veniam, turducken shank consectetur turkey duis. Deserunt veniam cupim chicken t-bone. Cow non filet mignon tenderloin short loin. Porchetta kevin ullamco, short ribs shoulder ut pariatur laborum in aliquip rump.

?> For more use cases of `docsify-cli`, head over to the [docsify-cli documentation](https://github.com/docsifyjs/docsify-cli).

### Checkbox Input

Bacon ipsum dolor amet short loin pork flank shank nostrud. Aliquip anim pork loin fatback. Proident drumstick esse frankfurter quis. Sunt ad veniam, turducken shank consectetur turkey duis. Deserunt veniam cupim chicken t-bone. Cow non filet mignon tenderloin short loin. Porchetta kevin ullamco, short ribs shoulder ut pariatur laborum in aliquip rump.

### Toggle Slider Input

Bacon ipsum dolor amet short loin pork flank shank nostrud. Aliquip anim pork loin fatback. Proident drumstick esse frankfurter quis. Sunt ad veniam, turducken shank consectetur turkey duis. Deserunt veniam cupim chicken t-bone. Cow non filet mignon tenderloin short loin. Porchetta kevin ullamco, short ribs shoulder ut pariatur laborum in aliquip rump.
