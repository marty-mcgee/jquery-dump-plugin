Showing dump result in a pop-up window makes you available to:
  * search for a needed string using browser search functionality
  * save result and keep it as a reference
  * execute parameter-less inner functions
  * manage dumps of multiple objects as pages
  * use it in mobile development

**Note**
  1. browser should allow popups
  1. variable `__jqdump__` exposed to the DOM after first dump call

### Example ###
```
// dump navigator properties
$.dump(
  window.navigator,  /* any object to dump */
  1,                 /* optional dump depth, default: 2 */
  "window.navigator" /* optional label */
);

// dump element selected by the jQuery selector
$("#element").dump();

// same as
$.dump($("#element"), 2, "(#element)");

// this may be used to disable all following function calls
$.dump("off");
```

### Features ###
  * multiple object dumping due to asynchronous nature of window.open()
  * if detected that pop-up is blocked, then dump content may be shown in same window
  * managed dump depth via function parameter (default: 2)
  * option to continue explore the dump if object property nesting exceeds the dump depth
  * object properties sorted in alphabetical order
  * collapse/expand nested objects
  * using dump depth with collapsible interface eliminates cyclic object reference mess
  * build-in syntax highlight for common JavaScript data types
  * clicking on the property name displays alert box with full property path, use Ctrl+C to copy to clipboard
  * clicking on the function name executes it (parameters not handled) and displays result in another pop-up, in case of exception, exception wrapper will be shown
  * if JavaScript engine permits - total number of accepted by function arguments will be shown
  * if JavaScript engine denies read access to the property value - exception message is shown alongside property name


---

Thank You!
<a href='https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=DRNSD68Q9PPGU' title='Donate'>
<blockquote><img src='https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG_global.gif' alt='Donate' />
</a>