# Tailwind Simple Site

This is my very simple boilerplate template for simple sites/landing pages using
TailwindCSS.

It comes with:

* A REALLY simple HTML build that allows templates and partials
* Tailwind CSS
* Tailwind Forms plugin
* build.sh script to dev build (no CSS purge)
* prod.sh script to prod build (with CSS purge)

It does NOT come with:

* A watch script or hot reloading or anything. This will come when
[JIT](https://tailwindcss.com/docs/just-in-time-mode) is released properly.
See [this issue](https://github.com/tailwindlabs/tailwindcss/issues/4097)

## Usage

Requires node to be installed. Probably a recent version.

* `git clone git@github.com:rosswintle/tailwind-simple-site.git <directory>`
* `npm install`
* `./build.sh` or `./prod.sh`

## Templates

You can use a single-level template. The template can include partials and can be passed variables.

A file that uses a template looks like this:

```
<?php extend('../templates/main.html', ['title' => 'Hello World!']) ?>
    <h1>Hello World!</h1>
<?php endExtend() ?>
```

The template file itself looks like this:

```
<!DOCTYPE html>
<html lang="en">

<?php includePart('../parts/head.html', ['title' => $title]) ?>

<body>
    <?= $content ?>
</body>
</html>
```

Note that the content passed to the template is in the `$content` variable and can be echo'ed.

## Partials

Partials can be included and passed an array of variables.

```
<?php includePart('../parts/head.html', ['title' => $title]) ?>
```

## Purging CSS

Note that if you add HTML files in other directories, make sure you add them to the purge list in `tailwind.config.js` if needed.
