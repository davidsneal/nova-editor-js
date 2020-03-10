# Laravel Nova Editor JS Field

[![Latest Version on Github](https://img.shields.io/github/release/Davidsneal/nova-editor-js.svg?style=flat-square)](https://packagist.org/packages/Davidsneal/nova-editor-js)
[![Total Downloads](https://img.shields.io/packagist/dt/Davidsneal/nova-editor-js.svg?style=flat-square)](https://packagist.org/packages/Davidsneal/nova-editor-js)

A Laravel Nova implementation of [Editor.js](https://github.com/codex-team/editor.js) by [@Davidsneal](https://github.com/Davidsneal).

## Installation

Install via composer:

```
composer require Davidsneal/nova-editor-js
```

Publish the config file
```
php artisan vendor:publish --provider="Davidsneal\NovaEditorJs\FieldServiceProvider"
```

## Upgrade
If upgrading from v0.4.0, re-publish the config file!

## Usage:

Add this `use` statement to the top of the your nova resource file:

```
use Davidsneal\NovaEditorJs\NovaEditorJs;
```

Use the field as below:

```
NovaEditorJs::make('FieldName')
```

And boom!

You can configure what tools the Editor should use in the config 
file along with some other settings so make sure to have a look :)

You can use the built in function to generate the response for the frontend:

```
NovaEditorJs::generateHtmlOutput($user->about);
```

Each 'block' has it's own view which can be overwritten in `resources/views/vendor/nova-editor-js/`

## Tools included
* https://github.com/editor-js/header
* https://github.com/editor-js/image
* https://github.com/editor-js/code
* https://github.com/editor-js/link
* https://github.com/editor-js/list
* https://github.com/editor-js/inline-code
* https://github.com/editor-js/checklist
* https://github.com/editor-js/marker
* https://github.com/editor-js/embed
* https://github.com/editor-js/delimiter
* https://github.com/editor-js/table
* https://github.com/editor-js/raw