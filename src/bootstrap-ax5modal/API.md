# Basic Usage
> Modal UI, hold does not exceed the current page, you can use in order to process a simple user input and information. In some cases, by the other page so as to output in the modal, it can also handle the task of more diverse forms.

## setConfig()
`setConfig([options])`
You define the default settings for the modal. Create a ax5.ui.modal instance, using the setConfig method in that instance, you can define a default value.
 
```js
var myModal = new ax5.ui.modal();
myModal.set_config({
    width: "Number",
    height: "Number",
    position: {
        left: "left|center|right|Number", 
        top: "top|middle|bottom|Number", 
        margin: "Number"
    },
    iframe: {
        method: "get|post", 
        url: "String", 
        param: "paramString|Object"
    },
    closeToEsc: "Boolean",
    onStateChanged: "Function",
    animateTime: "Number",
    zIndex: "Number"
});
```

### width

Type: `Number` [default: 300]

Modal width

### height

Type: `Number` [default: 400]

Modal height

### position

Type: `Object` 

**default**
```json
{
    left: "center", // left|center|right|Number
    top: "middle", // top|middle|bottom|Number
    margin: 10
}
```

### iframe

Type: `Object` 

**default**
```json
{
    method: "get", // get|post
    url: "", // iframe src url
    param: "" // parameter
}
```

### closeToEsc

Type: `Boolean`

### onStateChanged

Type: `Function`  

onStateChanged function is executed when the modal of the state is changed,
this.state state value is passed to this time onStateChanged function.

### animateTime

Type: `Number` [default : 300]

### zIndex

Type: `Number`

- - -

## open()
`open(Options[, callBack])`

it is possible to redefine all of the options that can be used in setConfig.  

```js
modal.open();
modal.open({
    width: 500,
    height: 500
});
modal.open({}, function(){
    console.log(this);
});
```

- - -

## css()
`css(Object)`

```js
modal.css({
    width: 400,
    height: 600
});
```

- - -

## align()
`align(Object)`

```js
modal.align({left:"center", top:"middle"});
modal.align({left:"left", top:"top", margin: 20});
```

- - - 

## close()
`close()`