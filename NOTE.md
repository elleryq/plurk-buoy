
# Using jQuery

Plurk use jQuery.
We can use jQuery via unsafeWindow.jQuery(), but there are some limitition.
```
    var body = document.querySelector("body").innerHtml;
    var a = unsafeWindow.jQuery(".contents .space", body);
    a.off("mouseup", ".row.feed", false);

    // Not working.
    //a.off("mouseup", ".row.feed");

    // Not working too.
    //a(".row.feed").unbind("mouseup");
```

# Debug

Put the following code in function(window) {} to dump mesasges.

```
console.log("=====");
console.log("event.button=" + event.button);
console.log("event.which=" + event.which);
console.log("target.nodeName=" + target.nodeName);
console.log("target.parentNode.nodeName=" + target.parentNode.nodeName);
console.log("target.parentNode.className=" + target.parentNode.className);
console.log("target.className=" + target.className);
```
