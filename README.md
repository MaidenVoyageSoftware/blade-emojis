# Blade Emojis

<a href="https://github.com/maiden-voyage-software/blade-emojis/actions?query=workflow%3ATests">
    <img src="https://github.com/maiden-voyage-software/blade-emojis/workflows/Tests/badge.svg" alt="Tests">
</a>
<a href="https://packagist.org/packages/maiden-voyage-software/blade-emojis">
    <img src="https://img.shields.io/packagist/v/maiden-voyage-software/blade-emojis" alt="Latest Stable Version">
</a>
<a href="https://packagist.org/packages/maiden-voyage-software/blade-emojis">
    <img src="https://img.shields.io/packagist/dt/maiden-voyage-software/blade-emojis" alt="Total Downloads">
</a>

> This is a template repository for new icon packages for [Blade Icons](https://github.com/driesvints/blade-icons). Start a new repo with this and replace the relevant things below:
> 
> 1. `MaidenVoyageSoftware` with your GitHub organization
> 2. `blade-emojis` with your repository name
> 3. `Blade Emojis` & `Blade Emojis` with your icon set name
> 4. Any other reference to `Heroicons` with your icon set name
> 5. `Maiden Voyage Software` with your name
> 
> Then, make sure [the implementation](./src) is correct, that you set up [icon generation](https://github.com/driesvints/blade-icons#generating-icons) and that [your tests](./tests) pass. And remove this quote block from your readme. When you've published your package on Packagist, make sure to send it in to [the Blade Icons package list](https://github.com/driesvints/blade-icons#icon-packages).

A package to easily make use of [Noto Emoji](https://github.com/googlefonts/noto-emoji) in your Laravel Blade views.

For a full list of available icons see [the SVG directory](resources/svg).

## Requirements

- PHP 8.2 or higher
- Laravel 10.0 or higher

## Installation

```bash
composer require maiden-voyage-software/blade-emojis
```

## Updating

Please refer to [`the upgrade guide`](UPGRADE.md) when updating the library.

## Blade Icons

Blade Emojis uses Blade Icons under the hood. Please refer to [the Blade Icons readme](https://github.com/driesvints/blade-icons) for additional functionality. We also recommend to [enable icon caching](https://github.com/driesvints/blade-icons#caching) with this library.

## Configuration

Blade Emojis also offers the ability to use features from Blade Icons like default classes, default attributes, etc. If you'd like to configure these, publish the `blade-emojis.php` config file:

```bash
php artisan vendor:publish --tag=blade-emojis-config
```

## Usage

Icons can be used as self-closing Blade components which will be compiled to SVG icons:

```blade
<x-heroicon-o-adjustments/>
```

You can also pass classes to your icon components:

```blade
<x-heroicon-o-adjustments class="w-6 h-6 text-gray-500"/>
```

And even use inline styles:

```blade
<x-heroicon-o-adjustments style="color: #555"/>
```

The solid icons can be referenced like this:

```blade
<x-heroicon-s-adjustments/>
```

### Raw SVG Icons

If you want to use the raw SVG icons as assets, you can publish them using:

```bash
php artisan vendor:publish --tag=blade-emojis --force
```

Then use them in your views like:

```blade
<img src="{{ asset('vendor/blade-emojis/o-adjustments.svg') }}" width="10" height="10"/>
```

## Changelog

Check out the [CHANGELOG](CHANGELOG.md) in this repository for all the recent changes.

## Maintainers

Blade Emojis is developed and maintained by Maiden Voyage Software.

## License

Blade Emojis is open-sourced software licensed under [the MIT license](LICENSE.md).
