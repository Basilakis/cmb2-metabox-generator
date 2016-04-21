# CMB2 Metabox Code Generator

Use this code generator to generate fully functional CMB2 metaboxes by visually adding fields in the designer or via bulk entry, and save your time and energy.

Demo: [CMB2 Metabox Code Generator](http://willthemoor.github.io/cmb2-metabox-generator/)

## New in this fork:
1. **Generated IDs:** IDs are auto-generated for each field  by making a 'clean' version of the `name` of the field. So 'My Great Field' becomes `'id' => 'my-great-field'`. Might not be perfect but generally saves a lot of typing.

2. **Bulk Entry:** Instead of creating fields one by one with the UI, you can insert a list of fields into the bulk entry area with one field per line. Each line should contain the field name, followed by a semi-colon, followed by the field-type. If no field-type is included, `text` is assumed.
<br><br>Example:
```
Area Headline; text
Area Copy; textarea
Area Logo; file
```
<br>
After entering bulk text, click the '[Generate Fields]' button. This will fill in the lower part of the UI so that you can tweak/add options to specific fields.

3. **Basic support for 'group' fields.**

Combining 2 and 3, you can generate groups via bulk entry by setting a field to 'group' and prepending two dashes to its subfields. This isn't terribly robust—the sub fields need to appear immediately after the group field definition.
<br><br>Example:
```
Projects; group
--Project Title; text
--Project Copy; textarea
--Project Contact Name; text
--Project Contact Email; text_email
```

Pull requests are very welcome. But please remember to send it to **development** branch.
