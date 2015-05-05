

# Introduction #

The default ManageController template is built to be as flexible as possible. It can easily be restyled or altered via CSS, but it uses completely semantic HTML, and strives to be as accessible as possible. However, there are times when this might not be good enough, or you might just want to integrate it with your existing design and stylesheet, and use different elements, or code it differently. It is easy to do so. Here's how.

# Getting Started #

If you haven't yet, create a new folder in the templates folder. Usually, this is under data/html\_templates, in your Terra App Data folder. You'll notice a folder named "default": That's the default set of templates, obviously. The name of the folder is the name of your template.

Secondly, create a manage.php file inside that folder, and code it. It's that easy. Below is a list of variables that you can use on your template.

# Variables #

## $record and $records ##
These are the singular and plural forms of the human spelling of a table's name, in lowercase. For a table named "users", $record is "user" and $records is "users". Quite obvious, really.

### Example ###
```
<h1>Manage <?php echo $records;?></h1>
<a href="#">Create <?php echo $record;?></a>
```

For a table named "users", it outputs:
`<h1>Manage users</h1>`
`<a href="#">Create user</a>`

You're free to use ucfirst(), ucwords() or strtoupper() if you need to change the case.

## $fields ##
This is an array containing all the fields that are meant to be used in the ManageController. Each field is an array containing things like the name, the identifier, the validation rules, and other such things, described in greater detail in the [Table Configuration Array](TerraDataTable.md) page.

### Example ###
```
<tr>
<?php foreach ($fields as $field) { ?>
    <th><?php echo $field['HumanName']; ?></th>
<?php } ?>
</tr>
```

This outputs a table row with the names of each of the fields as a table header.

## $rows ##
This is an array containing all the records that are to be shown on the current page. The rows contain only the fields that are meant to be used in the ManageController.

### Example ###
```
<?php foreach ($rows as $row) { ?>
    <tr>
        <?php foreach ($row as $value) { ?>
            <td><?php echo $value; ?></td>
        <?php } ?>
    </tr>
<?php } ?>
```

This will output a table row for each record that is to be shown on the current page, and fill each row with a table cell for each field.

## $page and $total\_pages ##
These should be self-explanatory. $page is the number of the page the user is currently viewing. $total\_pages is the number of pages there is.

## $rows\_per\_page ##
This is the number of records to be shown in a page.