# LaraWA Traditional Chinese Language Plugin

Traditional Chinese dashboard translations for [LaraWA](https://lara-wa.org).

## Install

```bash
composer require larawa/larawa-lang-zh-hant
```

LaraWA discovers Composer plugins installed under `vendor/larawa`. After installing, open Dashboard > Marketplace, enable **Traditional Chinese Dashboard Translation**, then choose **Traditional Chinese** from the dashboard language selector.

## Package

- Plugin ID: `larawa-lang-zh-hant`
- Locale: `zh-Hant`
- LaraWA core: `^13.0`
- License required: no
- License: MIT

## Development

Validate the package before tagging a release:

```bash
composer validate --strict --no-check-publish
find resources -name '*.php' -print0 | xargs -0 -n1 php -l
php -r '$m=json_decode(file_get_contents("larawa-plugin.json"), true, 512, JSON_THROW_ON_ERROR); if (($m["license_required"] ?? null) !== false) exit(1);'
```

Translation keys should match LaraWA core English files. LaraWA falls back to English for any missing runtime strings.

## License

This plugin is free software released under the [MIT license](LICENSE).
