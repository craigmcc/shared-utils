# Shared Utilities Library

This module contains a number of functions that I have shared across multiple
applications the old fashioned way (cut-n-paste).  It's time to make them a
separate thing, so they can be maintained and updated in one single place.

## Included Modules

The following modules are provided by this library:

| Module Name | Description                                                                                                                                                                                                                                                  |
| ----------- |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dates       | Convenience methods to deal with dates represented as strings (YYYY-MM-DD) that are most useful for UI forms, and for transport between client and server in JSON representations.                                                                           |
| Months      | Convenience methods to deal with months represented as strings (YYYY-MM) that are most useful in UI forms.                                                                                                                                                   |
| Timestamps  | Convenience methods to construct date/time representations as strings (either ISO or local).                                                                                                                                                                 |
| Validators  | Simple validation functions for many data types.  In all cases, an empty string value will be evaluated as *true*, because this commonly occurs in UI forms for new data objects.  If you need to check for required values, that should be done separately. |

Detailed API documentation for these modules is
available at [API Documentation](https://craigmcc.github.io/shared-utils/)

## Using the Utility Methods

### Install the Peer Dependencies

This library depends on the following peer dependencies, but is flexible about
which version is used.  Check the `peerDependencies` section of the
`package.json` file to see what minimum versions are required.

If not already installed, you can install the peer dependencies:
```shell
npm install date-fns
```

### Install the Package

Install this package by adding it to your `package.json` file, with npm:

```shell
npm install @craigmcc/shared-utils
```

or with yarn:

```shell
yarn install @craigmc/shared-utils
```

### Use utility methods in your functions

At the top of each source file, import the module(s) you will need:

```ts
import {Dates, Months} from "@craigmcc/shared-utils";
```

Then, call the requested method, prefixing it with the module name:

```ts
console.log(`It is currently ${Dates.today()}.`)
```

## Building the Library From Sources

You can download the sources for this library at
[Source Code](https://github.com/craigmcc/shared-utils)
and using the **Code** link to aquire the URL for a *git clone*
command.

After downloading, use the following commands (from within the
*shared-utils* directory) to install dependencies and perform a build.
```shell
npm install
npm run build
```

The `dist` directory will contain the built library.
