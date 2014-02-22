# &lt;x-route&gt;

A Polymer element for URL routing.

> Maintained by [Addy Osmani](https://github.com/addyosmani).

Based on `<flatiron-director>` by the Polymer team. 

## Demo

> [Check it live](http://addyosmani.github.io/x-route).

## Installation

Using [Bower](http://bower.io), run:

```shell
bower install x-route
```

## Usage

1. Import Web Components' polyfill:

    ```html
    <script src="platform.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="src/x-route.html">
    ```

3. Start using it!

    ```html
    <x-route></x-route>
    ```

## Examples

HTML:

```html
<!-- Automatically navigate to a route 'home' -->
<x-route route="/home" auto/>

<!-- Define paths to routes we would like to support -->
<x-route path="/favorites"/>
<x-route path="/about"/>
<x-route path="/books"/>
<x-route path="/books/view/:bookId"/>
<x-route path="/:foo/:bar/:bazz"/> 
```
JavaScript:

You can listen to a `route-changed` event for details about the route that was matched.

```javascript
document.addEventListener('route-changed', function(route){
    alert(route.detail);
});
```

## Setup

In order to run it locally you'll need a basic server setup.

1. Install [NodeJS](http://nodejs.org/download/).
2. Install [GruntJS](http://gruntjs.com/):

    ```sh
    $ [sudo] npm install -g grunt-cli
    ```

3. Install local dependencies:

    ```sh
    $ npm install
    ```

4. Run a local server and open `http://localhost:8000`.

    ```sh
    $ grunt connect
    ```

## Options

Attribute  | Options                   | Default             | Description
---        | ---                       | ---                 | ---
`path`      | *string*                  | ``               | A routing path
`route`      | *string*                  | ``               | The current route
`auto`      | *boolean*                  | `false`               | Automatically navigate to a defined route

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

For detailed changelog, check [Releases](https://github.com/webcomponents/element-boilerplate/releases).

## License

[MIT License](http://opensource.org/licenses/MIT)