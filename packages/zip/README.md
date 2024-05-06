# @capawesome-team/capacitor-zip

Capacitor plugin to zip and unzip files.

## Sponsorware

This project is available as **Sponsorware**.

> Sponsorware is a release strategy for open-source software that enables developers to be compensated for their open-source work with fewer downsides than traditional open-source funding models. ([Source](https://github.com/sponsorware/docs))

This means...

- The source code will be published as soon as [our GitHub Sponsors goal](https://github.com/sponsors/capawesome-team) is reached.
- Any GitHub sponsor with a [sponsorware tier](https://github.com/sponsors/capawesome-team?frequency=recurring) gets **immediate access** to our sponsors-only repository and can start using the project right away.

## Terms

This project is licensed under the terms of the MIT license.  
However, we kindly ask you to respect our **fair use policy**:

- Please **don't distribute the source code** of the sponsors-only repository. You may freely use it for public, private or commercial projects, privately fork or mirror it, but please don't make the source code public, as it would counteract the sponsorware strategy.
- If you cancel your subscription, you're automatically removed as a collaborator and will miss out on all future updates. However, **you may use the latest version that's available to you as long as you like**.

## Installation

See [Getting started with Insiders](https://capawesome.io/sponsors/insiders/getting-started/?plugin=capacitor-zip) and follow the instructions to install the plugin.

### Android Variables

This plugin will use the following project variables (defined in your app’s `variables.gradle` file):

- `$zip4jVersion` version of `net.lingala.zip4j:zip4j` (default: `2.11.5`)

## Configuration

No configuration required for this plugin.

## Demo

A working example can be found here: [robingenz/capacitor-plugin-demo](https://github.com/robingenz/capacitor-plugin-demo)

## Usage

```typescript
import { Zip } from '@capawesome-team/capacitor-zip';

const unzip = async () => {
  await Zip.unzip({
    source: 'file:///data/user/0/dev.robingenz.capacitor.plugindemo/cache/1714900095398.zip',
    destination: 'file:///data/user/0/dev.robingenz.capacitor.plugindemo/cache/1714900095398',
  });
};

const zip = async () => {
  await Zip.zip({
    source: 'file:///data/user/0/dev.robingenz.capacitor.plugindemo/cache/1714900095398',
    destination: 'file:///data/user/0/dev.robingenz.capacitor.plugindemo/cache/1714900095398.zip',
  });
};
```

## API

<docgen-index>

* [`zip(...)`](#zip)
* [`unzip(...)`](#unzip)
* [Interfaces](#interfaces)

</docgen-index>

<docgen-api>
<!--Update the source file JSDoc comments and rerun docgen to update the docs below-->

### zip(...)

```typescript
zip(options: ZipOptions) => Promise<void>
```

Zip a file or directory.

Only available on Android and iOS.

| Param         | Type                                              |
| ------------- | ------------------------------------------------- |
| **`options`** | <code><a href="#zipoptions">ZipOptions</a></code> |

**Since:** 6.0.0

--------------------


### unzip(...)

```typescript
unzip(options: UnzipOptions) => Promise<void>
```

Unzip a file.

Only available on Android and iOS.

| Param         | Type                                                  |
| ------------- | ----------------------------------------------------- |
| **`options`** | <code><a href="#unzipoptions">UnzipOptions</a></code> |

**Since:** 6.0.0

--------------------


### Interfaces


#### ZipOptions

| Prop              | Type                | Description                          | Since |
| ----------------- | ------------------- | ------------------------------------ | ----- |
| **`source`**      | <code>string</code> | The source file or directory to zip. | 6.0.0 |
| **`destination`** | <code>string</code> | The destination file.                | 6.0.0 |


#### UnzipOptions

| Prop              | Type                | Description                | Since |
| ----------------- | ------------------- | -------------------------- | ----- |
| **`source`**      | <code>string</code> | The source file to unzip.  | 6.0.0 |
| **`destination`** | <code>string</code> | The destination directory. | 6.0.0 |

</docgen-api>

## Changelog

See [CHANGELOG.md](https://github.com/capawesome-team/capacitor-plugins/blob/main/packages/zip/CHANGELOG.md).

## License

See [LICENSE](https://github.com/capawesome-team/capacitor-plugins/blob/main/packages/zip/LICENSE).
