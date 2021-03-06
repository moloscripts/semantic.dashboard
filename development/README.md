# Contributing Guidelines of `semantic.dashboard`

## Modifying JS
The library's JS file `semantic.dashboard.min.js` is an output of compilation, concatenation and minification of various JS files contained in the `srcjs` directory. The compilation is made with [gulp](https://gulpjs.com/).

If you want to add some JS to the library, simply create or modify one of the files in the `srcjs` directory and then go to `tool` directory and run `gulp` command. 

Keep in mind that in order to run this command need to have gulp-cli (`npm i --global gulp-cli`) and the dependencies in `tools` directory (`npm i`) installed.

After creating new gulp artifact, don't forget to commit both the output, as well as all source JS files.


## Modifying CSS
This project uses [SASS](https://sass-lang.com/) to define styles. SASS files contained in the `styles` folder are compiled to CSS and minified. The output file is `semantic.dashboard.min.css`. Do not edit this file by hand. 

If you want to modify styles, modify (or create) appropriate `.scss` file and then run `styles/generate_css.R`. 

Don't forget to commit both `.scss` as well as `.css` files.

## Bumping the version
When you're ready with your changes, bump the version in `DESCRIPTION` file by `0.0.1`.

## Updating the changelog
Don't forget to summarize your changes in the `CHANGELOG.md`.


## Useful scripts
The `development/dev.R` script is very useful when working on the library. It will automatically generate the CSS out of SASS, as well as bundle JS. Then it will run example app of your choice (`examples/app.R` by default). 

The script will always run the example app on port `5167` which is useful if you prefer to debug the frontend in your default browser. Go ahead and add a bookmark for `http://localhost:5167/` to quickly access the example app in Chrome.
