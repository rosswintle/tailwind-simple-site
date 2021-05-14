# Tailwind Simple Site

This is my very simple boilerplate template for simple sites/landing pages using
TailwindCSS.

It comes with:

* An empty index.html
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

* Download
* `npm install`
* `./build.sh` or `./prod.sh`

Note that if you add HTML files, make sure you add them to the purge list in `tailwind.config.js` if needed.
