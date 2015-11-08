
```
bower install tinymce
```

If you'd like to install and build the source manually with Bower use these steps. This approach can be used when debugging or building custom plugins.

```
bower install tinymce-src=git://github.com/tinymce/tinymce
cd bower_components/tinymce-src
npm i
jake
```

### Step 1: Include the TinyMCE script

Include this line of code in the `<head>` of your HTML page:

```html
<script src="/path/to/tinymce.min.js"></script>
```

> Tip: we give you a complete html snippet in Step 2.

### Step 2: Initialize TinyMCE as part of a web form

With the script included, initialize TinyMCE on any element (or elements) in your web page.

Since TinyMCE lets you identify replaceable elements via a CSS selector, all you need do is pass an object that contains a `selector` to `tinymce.init()`.

In this example, let's replace `<textarea id="mytextarea">` with a TinyMCE editor instance by passing the selector `'#mytextarea'` to `tinymce.init()`.

```html
<!DOCTYPE html>
<html>
<head>
  <script src="/path/to/tinymce.min.js"></script>
  <script type="text/javascript">
    tinymce.init({
      selector: "#mytextarea"
    });
  </script>
</head>

<body>
<h1>TinyMCE Quick Start Guide</h1>
  <form method="post">
    <textarea id="mytextarea">Hello, World!</textarea>
  </form>
</body>
</html>
```

And that's all there is to it!

### Step 3: Saving content with a form POST

When the `<form>` is submitted the TinyMCE editor mimics the behavior of a normal HTML `<textarea>` during the `post`. In your form handler you can process the content submitted as if it had come from a regular `<textarea>`.

#### Use of local plugins & language packs when installing via package managers

When using package managers you might have local TinyMCE addons in your project such as plugins or language packs. Load these from your project location rather than from inside the package using these config options:

```js
tinymce.init({
  language: "sv",
  language_url: "/js/sv.js",
  plugins: "myplugin",
  external_plugins: {
    "myplugin": "/js/myplugin/plugin.min.js"
  }
});
```

> In the next step you'll learn how to unleash TinyMCE's power by [working with plugins](../working-with-plugins/).