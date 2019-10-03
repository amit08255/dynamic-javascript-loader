## Introduction
Dynamically load JavaScript in your NodeJS apps. Flexible script. No extra dependency. It appends a script node to the <head> element in the dom.
```js 
require('dynamic-javascript-loader')
``` 
returns a function of the following interface: function(url[, opts][, cb]) {}

## Function parameters for JavaScript loader

* **url -** Any url that you would like to load. May be absolute or relative.

* **[, opts] -** A map of options. Here are the currently supported options:

1. ```async``` - A boolean value used for script.async. By default this is true.
2. ```attrs``` - A map of attributes to set on the script node before appending it to the DOM. By default this is empty.
3. ```charset``` - A string value used for script.charset. By default this is utf8.
4. ```text``` - A string of text to append to the script node before it is appended to the DOM. By default this is empty.
5. ```type``` - A string used for script.type. By default this is text/javascript.

* **[, cb] -** A callback function of the following interface: function(err, script) {} where err is an error if any occurred and script is the script node that was appended to the DOM.

## Example

```js
var load = require('load-script')

load('foo.js', function (err, script) {
  if (err) {
    // print useful message
  }
  else {
    console.log(script.src);// Prints 'foo'.js'
    // use script
    // note that in IE8 and below loading error wouldn't be reported
  }
})
```
<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Amit Kumar - [@amit08255](https://twitter.com/amit08255) - amitcute3@gmail.com

Project Link: [https://github.com/amit08255/dynamic-javascript-loader](https://github.com/amit08255/dynamic-javascript-loader)

