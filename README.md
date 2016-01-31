# polymer-crud

An element for CRUDs in Polymer, the easy way

## Installing
`bower install --save https://github.com/3nyder/polymer-crud.git`

## Playing With The Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/polymer-crud/`, where `polymer-crud` is the name of the directory containing it.


## Example

```html
<script>
  model = [
  { 
    key       : "name",
    label     : 'Name',
    searchable: true,
    sortable  : true,
    size      : 5
  },
  {
    key       : "lastname",
    label     : 'Last Name',
    searchable: true,
    sortable  : true,
    size      : 5
  },
  {
    key       : "age",
    type      : "number",
    label     : 'Age',
    type      : 'number',
    searchable: true,
    sortable  : true,
    size      : 2,
    min       : 10,
    max       : 100,
    step      : 5
  }
];
strings = [
  new    : 'New Item',
  accept : 'Accept',
  cancel : 'Cancel',
  success: 'Success',
  error  : 'Error',
  confirm: 'Confirm',
  confirmQuestion: 'Are you sure?'
];
actions = [
  {
    title : 'Edit',
    event : 'crud-edit',
    icon : 'create'
  },
  {
    title : 'Delete',
    event : 'crud-delete',
    icon : 'delete'
  }
];
</script>

<polymer-crud
  title="Title of the CRUD"
  url="http://xmpl.co/api/item"
  idname="ididem"
  pagination="25"
  model={{model}}
  strings={{strings}}
  actions={{actions}}
  ></polymer-crud>
```
