# Hafslund digital designsystem (Hdd)

[![npm version](https://img.shields.io/npm/v/@hafslundnett/hdd-style.svg)](https://www.npmjs.com/package/@hafslundnett/hdd-style)
[![npm size](https://badgen.net/bundlephobia/minzip/@hafslundnett/hdd-style)](https://bundlephobia.com/result?p=@hafslundnett/hdd-style)

[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)


'Hafslund digital designsystem' is a design system that can be used across projects while maintaining consistancy. The project follows strict naming guidlines, your can read more about them in the [wiki](https://github.com/hafslundnett/hdd-theme/wiki/Naming-guidelines). Every component should be able to run in an isolated environment without depending on parent classes/elements.

For every used front-end framework a separate 'components' library should be created. Listed below are the already existing libraries. If you want to add your library to this list, please create a pull request.

| Framework     | Version       | Repo          |
| ------------- | ------------- | ------------- |
| Angular 6.x | 🚧 Alpha | [Github](https://github.com/hafslundnett/hdd-ng-components) |
| Vue 2.x | 🚧 Alpha | [Github](https://github.com/hafslundnett/hdd-vue) | 

## Documentation

HDD-style is documented along with it´s corresponding components library(HAL) at: 
- https://hal-components.hafslundnett.io/welcome

The showoff website include all documentation off components with related examples. The showoff website can be generated/started by running:

* `yarn`
* `yarn start`

You need to have `node` and `yarn` installed in order to start the showoff website.

## Publish new version
You need access to the Hafslund Nett NPM organisation
* `yarn build`
* `npm publish`

## Code of conduct

We will behave ourselves if you behave yourselves. For more details see our
[code of conduct](./CODE_OF_CONDUCT.md).

## Contributing

Please read through our [contributing guidelines](./CONTRIBUTING.md).

## Versioning

This project will be maintained under the Semantic Versioning guidelines as much as possible. Releases will be numbered
with the following format:

`<major>.<minor>.<patch>`

## Releasing new versions and updating CDN

Azure CDN is used to host fonts and icons from the `cdn/` folder. To update the contents of 

1. Check in the new files under `cdn/`.
2. If this will be included in a new version of the package: Update the package version in `package.json` and the CDN-url in `variables/fontawesome/_variables.scss`. The three numbers after "hdd-style-release-" should match the package version. If the package version is 1.0.2, then the url bound to `$fa-font-path` should be `https://hafslundnett.azureedge.net/hdd-style-release-1-0-2/icons`.
3. Check in and get your pull request accepted into develop.
4. Create a new release-branch and push it to GitHub. The name of the branch should be on the format `release/1.0.2`, given that the package version is 1.0.2. This will start the hdd-style.release build, and upload the contents of `cdn/` to Azure CDN.
5. Continue to release the new version of hdd-style by packaging and uploading the new version to npm manually.
6. When everything is ok, merge the release-branch into master, and draft a new release on GitHub.

_**Note:** This process has [room for improvements](https://github.com/hafslundnett/hdd-style/issues/92)._

## Team

*   [Erik Tallang](https://github.com/eTallang)
*   [Jeroen Rinzema](https://github.com/jeroenrinzema)
