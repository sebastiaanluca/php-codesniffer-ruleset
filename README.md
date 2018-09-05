# An opinionated custom coding standard

[![Latest stable release][version-badge]][link-packagist]
[![Software license][license-badge]](LICENSE.md)
[![Total downloads][downloads-badge]][link-packagist]

[![Read my blog][blog-link-badge]][link-blog]
[![View my other packages and projects][packages-link-badge]][link-packages]
[![Follow @sebastiaanluca on Twitter][twitter-profile-badge]][link-twitter]

## Table of contents

- [Requirements](#requirements)
- [How to install](#how-to-install)
    - [Enabling the rules](#enabling-the-rules)
    - [Sniffing code](#sniffing-code)
    - [Sniffing code in PHPStorm](#sniffing-code-in-phpstorm)
- [License](#license)
- [Change log](#change-log)
- [Contributing](#contributing)
- [Security](#security)
- [Credits](#credits)
- [About](#about)

## Requirements

- [squizlabs/php_codesniffer](https://github.com/squizlabs/PHP_CodeSniffer) 3.3.1 or higher
- [slevomat/coding-standard](https://github.com/slevomat/coding-standard) 4.7 or higher

## How to install

```bash
composer require sebastiaanluca/php-codesniffer-ruleset --dev
```

## How to use

### Enabling the rules

Add it to your project `phpcs.xml` or `phpcs.xml.dist` ruleset:

```xml
<?xml version="1.0"?>
<ruleset>
    <arg name="basepath" value="."/>

    <file>./src</file>
    <file>./tests</file>

    <rule ref="./vendor/sebastiaanluca/php-codesniffer-ruleset/ruleset.xml"/>
</ruleset>
```

### Sniffing code

The following commands can be added to the `scripts` section of your `composer.json` file to check and fix invalid code. Some optional checks are also included to illustrate how they might work together to check all your code.

```json
{
    "scripts": {
        "composer-validate": "@composer validate --no-check-all --strict",
        "codesniffer-check": "vendor/bin/phpcs --runtime-set ignore_errors_on_exit 1 --runtime-set ignore_warnings_on_exit 1",
        "codesniffer-fix": "vendor/bin/phpcbf --runtime-set ignore_errors_on_exit 1 --runtime-set ignore_warnings_on_exit 1 || exit 0",
        "test": "vendor/bin/phpunit",
        "check": [
            "@composer-validate",
            "@codesniffer-check",
            "@test"
        ]
    }
}
```

### Sniffing code in PHPStorm

See [PHP Code Sniffer in PhpStorm](https://confluence.jetbrains.com/display/PhpStorm/PHP+Code+Sniffer+in+PhpStorm) on how to set up CodeSniffer in PHPStorm.

## License

This package operates under the MIT License (MIT). Please see [LICENSE](LICENSE.md) for more information.

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## Security

If you discover any security related issues, please email [hello@sebastiaanluca.com][link-author-email] instead of using the issue tracker.

## Credits

- [Sebastiaan Luca][link-github-profile]
- [All Contributors][link-contributors]

## About

My name is Sebastiaan and I'm a freelance Laravel developer specializing in building custom Laravel applications. Check out my [portfolio][link-portfolio] for more information, [my blog][link-blog] for the latest tips and tricks, and my other [packages][link-packages] to kick-start your next project.

Have a project that could use some guidance? Send me an e-mail at [hello@sebastiaanluca.com][link-author-email]!

[version-badge]: https://poser.pugx.org/sebastiaanluca/php-codesniffer-ruleset/version
[license-badge]: https://img.shields.io/badge/license-MIT-brightgreen.svg
[downloads-badge]: https://img.shields.io/packagist/dt/sebastiaanluca/php-codesniffer-ruleset.svg

[blog-link-badge]: https://img.shields.io/badge/link-blog-lightgrey.svg
[packages-link-badge]: https://img.shields.io/badge/link-other_packages-lightgrey.svg
[twitter-profile-badge]: https://img.shields.io/twitter/follow/sebastiaanluca.svg?style=social
[twitter-share-badge]: https://img.shields.io/twitter/url/http/shields.io.svg?style=social

[link-packagist]: https://packagist.org/packages/sebastiaanluca/php-codesniffer-ruleset
[link-contributors]: ../../contributors

[link-portfolio]: https://www.sebastiaanluca.com
[link-blog]: https://blog.sebastiaanluca.com
[link-packages]: https://packagist.org/packages/sebastiaanluca
[link-twitter]: https://twitter.com/sebastiaanluca
[link-github-profile]: https://github.com/sebastiaanluca
[link-author-email]: mailto:hello@sebastiaanluca.com
