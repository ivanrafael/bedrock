# Bedrock

Welcome to Bedrock.

<img src="http://f.cl.ly/items/413y2M3N1w231a3o3X09/bedrock-icon.png" width="250">

Bedrock is a static site generator to easily make HTML prototypes. For more information, please check out <a href="http://bedrock.mono.company/">the Bedrock homepage</a>.

## Basic installation & first run

* First, make sure you have Node 4.2.1 installed. You can find the latest version of Node at <a href="https://nodejs.org/en/">NodeJS.org</a>.
* You need to have `gulp` installed globally to use Bedrock. `npm install -g gulp`.
* Install the project's dependencies:
  * `npm install`
* Run `gulp` to start your project.

## Installation with icon font generation

* If you want to use icon fonts you need more dependencies than just node. Icon font generation is optional. Set `icons.generateIconsFromSource` to `true` in `bedrock.config.js` to activate icon fonts.
* In order for the icon font generation to work, install the required gems using `bundle install`. You will need <a href="http://bundler.io">Bundler</a> for this. We depend on a Ruby gem called `fontcustom`. Bundler will install the required dependencies.
    * You might also need to install fontforge using <a href="http://brew.sh/">brew</a>. For download instructions see the <a href="https://github.com/FontCustom/fontcustom">fontcustom</a> repo.

## Major commands

* `gulp`: runs the prototype
* `gulp build`: create a build (which ends up in the `dist` folder) that can be deployed to a server

## Other commands

* `gulp icon-font`: manually run the icon font
* `gulp modernizr`: create a custom Modernizr file using the feature specified in the configuration

## Configuration

The configuration lives in `bedrock.config.js`. Available options are:

* styleguide
  * snippetLanguage
    * This modifies the language snippets shown in the styleguide. 
    * `jade` or `html`
  * colors
    * path to the SCSS file specifying colors (for the color feature in the styleguide which shows the project's colors in a visual way)
* patternClasses
  * which patterns should get extra CSS classes
  * this is useful for customizing the styleguide while keeping your main CSS file clean e.g. to show elements that are hidden by default
  * specify the pattern as a string and 1 or more classes as an array
* modernizr
  * minify (boolean)
    * whether modernizr output should be minified 
  * feature-detects (array)
    * which feature detects should be included when building a custom version of modernizr

## Upgrading bedrock

See the README at https://github.com/mono-company/bedrock-cli .

## Windows

Windows usage is not supported at the moment. We have used Bedrock on Windows succesfully though. If you encounter any Windows related bugs, please log them.

## License

Bedrock is MIT licensed.

## Credits

Bedrock was made by the team at <a href="http://mono.company">Mono</a> with most major contributions by <a href="http://thomastuts.com/">Thomas Tuts</a>.
