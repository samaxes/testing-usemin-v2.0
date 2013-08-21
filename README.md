# Testing grunt-usemin v2.0

This a CLEAN test project created with generator-angular v0.3.1 to support the issue [#108](https://github.com/yeoman/grunt-usemin/issues/108) of grunt-usemin.

## Code changes

* Uglify task has been commented in Gruntfile... Otherwise the project won't build when using grunt-usemin v2.0 dependency.
* Added the images `logoPhune.png` and `logoPhune@2x.png` to the images folder.
* The following lines have been added to the file `app/views/main.html`:

```html
<img src="/images/logoPhune.png" srcset="/images/logoPhune@2x.png 2x" alt="Phune Gaming" width="71" height="23" />
<img src="images/logoPhune.png" srcset="images/logoPhune@2x.png 2x" alt="Phune Gaming" width="71" height="23" />
```

## Project build

Install NPM and Bower dependencies:

```
npm install && bower install --dev
```

Create and build the project with grunt-usemin v0.1.12:

```
grunt
```

Resulting `<img>` tags in the file `dist/views/main.html`:

```html
<img src="/images/0b1f0a13.logoPhune.png" srcset="/images/logoPhune@2x.png 2x" alt="Phune Gaming" width="71" height="23">
<img src="images/logoPhune.png" srcset="images/logoPhune@2x.png 2x" alt="Phune Gaming" width="71" height="23">
```

Update to grunt-usemin v2.0:

```
npm install grunt-usemin-2.0 --save-dev
```

Create and build the project with grunt-usemin v2.0:

```
grunt
```

Resulting `<img>` tags in the file `dist/views/main.html`:

```html
<img src="/images/logoPhune.png" srcset="/images/logoPhune@2x.png 2x" alt="Phune Gaming" width="71" height="23">
<img src="images/logoPhune.png" srcset="images/logoPhune@2x.png 2x" alt="Phune Gaming" width="71" height="23">
```
