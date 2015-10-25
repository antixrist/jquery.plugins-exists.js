# jquery.plugins-exists.js

Checks for the existence of each plugin in list.

It has two variants of usage (both variants are the same):

* with callback:
```javascript
$.pluginsExists('form', 'fancybox', 'anotherPlugin', function () {
  // all exist either in $ or in $.fn
  // callback is NOT async
});

$.pluginsExists(['form', 'fancybox', 'anotherPlugin'], function () {
  // same as above
});

$.pluginsExists(['form', 'fancybox'], ['anotherPlugin'], function () {
  // same as above
});
```

* and without callback:
```javascript
if ($.pluginsExists('form', 'fancybox', 'anotherPlugin')) {
  // all exist either in $ or in $.fn
}

if ($.pluginsExists(['form', 'fancybox', 'anotherPlugin'])) {
  // same as above
}

if ($.pluginsExists(['form', 'fancybox'], ['anotherPlugin'])) {
  // same as above
}
```

List the names of plugins can be either an array or comma-separated arguments list.
