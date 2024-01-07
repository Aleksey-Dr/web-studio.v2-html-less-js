# [WEB STUDIO](https://aleksey-dr.github.io/goit-markup-hw-04/)

#### [Aleksey-Dr](https://github.com/Aleksey-Dr)

### Technologies
[![Technologies](https://skillicons.dev/icons?i=html,css,md,js)](https://skillicons.dev)
[![Tools](https://skillicons.dev/icons?i=github,git,vscode,figma)](https://skillicons.dev)
___
### Working with {Less}:

Set the extension [Easy LESS](https://marketplace.visualstudio.com/items?itemName=mrcrowl.easy-less&ssr=false#overview) for [VSCode](https://code.visualstudio.com/)


* Create settings.json file.
* settings.json must exist in the .vscode directory at the root level of your project.
* Use the "less.compile" key.

Example settings.json file:

```
{
  "less.compile": {
    "compress": true, // true => remove surplus whitespace
    "sourceMap": true, // true => generate source maps (.css.map files)
    "out": false // false => DON'T output .css files (overridable per-file, see below)
  }
}
```

Settings Easy LESS:

```"compress": true/false```
* Compresses the css output by removing surplus white-space.

```"sourceMap": true/false```
* Enables generation of source map files.
* When enabled, a .css.map file will be output in the same direction as the .css file (except when sourceMapFileInline is set, see below).
* The out setting is respected.

```out: { boolean | filepath: string | folderpath: string }```
* Redirects the css output to a different file or suppresses output.
* If filepath is used, but no file extension is specified, it will append .css
* If folderpath is used, the less filename will be used, but with the .css extension
* NOTE: A folder path must end with a / (or \ for Windows), e.g. ../css/ not ../css (the latter is always interpreted as an extensionless filename).
Filepath is relative to the current file, so relative paths can be used, e.g. ../../styles.css
The following replacements are available:
  * \${workspaceFolder} — the root folder for the VS Code project containing the .less file.
  * \$1 — the "base" name of the .less file, e.g. for styles.css, $1 would be style.
  * \$2 — the extension of the css file, usually .css unless outExt is used.
* Example: \${workspaceFolder}/dist/css/final-\$1$2
* out: false = don't output.
* This setting can be used to override a project-wide "out": false setting, where you only want certain .less files to be generated.