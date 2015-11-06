# gentle-watch
A tool to gently watch object properties, slowing down the browser as less as possible


# Typical usage

```
var $el = $('#element-with-slow-loading-3rd-party-dynamic-objects');
gentleWatch($el[0], 'offsetHeight', function() {
  // Complex align algoritm goes here
});
```

*Yes, I know, you proudly write `document.getElementById('x')` instead of `$('#x')[0]`. I am just trying to talk a common language in examples.*

# Complete API

```
// Vary browser load vs responsibility
// Default 100ms
gentleWatch.poolInterval = 50; 

// Define callback
var callback = function(newValue, object, property, previousValue) {
  
};

// Subscribe
gentleWatch(object, 'propertyName', callback);

// Unsubscribe
gentleWatch.unwatch(callback);
```

# Copyright & License

Copyright (c) Pavel Koryagin 2015.

Licensed under [MIT](https://opensource.org/licenses/MIT) conditions.

