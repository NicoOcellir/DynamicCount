# DynamicCount

## Description
Javascript code to show a dynamic (updates as you type) count of the number of characters in a text box with adjustable colour depending on the amount entered. Requires JQuery.

## Features

* Updates the count as you type 
* Three color sections

## Browser Compatibility
Tested in the following browsers:

* Google Chrome
* Microsoft Edge 83+
* Firefox
* Most mobile browsers

## Documentation

### Example

#### Input text box

```
<input type="text" id="box" name="name" size="100">
````
#### Output count message

```
<div id="count">0 / 8</div>
```

#### Main JavaScript code

```
<script>
$("#box").on("input", updateCount);
function updateCount() {
    var a = $("#box").val().length;
    switch (!0) {
// green when 8 characters
        case 8 == a:
            background = "#008000";
            break;
// red when more than 8 characters
        case 8 < a:
            background = "#A52A2A";
            break;
// initial blue color
        default:
            background = "#1E90FF";
    }
    $("#count").css("background", background).text(a + " / 8");
};
</script>
```

### Screenshot

![alt text](https://i.imgur.com/SMVY6he.png)


### In action

You can see this code in action at the XVEA [Vin Decoder](https://www.xvea.com/) website.


## License



