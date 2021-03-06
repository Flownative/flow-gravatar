[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)
[![Packagist](https://img.shields.io/packagist/v/flownative/gravatar.svg)](https://packagist.org/packages/flownative/gravatar)
[![Maintenance level: Love](https://img.shields.io/badge/maintenance-%E2%99%A1%E2%99%A1%E2%99%A1-ff69b4.svg)](https://www.flownative.com/en/products/open-source.html)

# Gravatar View Helper for Flow

This package provides a Fluid View Helper which can be used in Neos Flow based applications for displaying
Gravatar images.

## Installation

The Flownative Gravatar package is installed as a regular Flow package via Composer. For your existing project,
simply include `flownative/gravatar` into the dependencies of your Flow or Neos distribution:

```bash
    $ composer require flownative/gravatar:~2.0
```

## Usage

In your Fluid template, use the Gravatar View Helper like any other view helper. Possible arguments for the view
helper are:

|Argument|Required ?|Description|
|--------|----------|-----------|
|email   |yes       |specifies the email address of the Gravatar to display|
|size    |no        |the size in pixels (used for width and height)|
|default |no        |a URL pointing to a fallback image if no Gravatar exists for the given email address. Instead of a URL, the "default" parameter can also be one of "404", "mm", "identicon", "monsterid", "wavatar", retro" or "blank"|

```html
{namespace gravatar=Flownative\Gravatar\ViewHelpers}
<html lang="en">
...
    <body>
        <gravatar:gravatar email="{someEmailAddress}" default="retro" size="48" alt="image" class="img-circle" width="48" height="48" />
    </body>
</html>
```
