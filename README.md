# Sass Library #

Collection of useful sass mixins, functions etc.

## Installation ##

Using `yarn`:

```bash
$ yarn add https://github.com/mandalornl/sass-libs.git
```

Or using `npm`:

```bash
$ npm install --save https://github.com/mandalornl/sass-libs.git
```

## Usage ##

Just import the `scss` file(s) you wan't to use. `~` refers to the `node_modules` map. **Note:** Don't append `~` with a `/`.

```sass
@import '~sass-libs/src/functions/param';
@import '~sass-libs/src/functions/rem-calc';
@import '~sass-libs/src/functions/strip-unit';
@import '~sass-libs/src/mixins/fluidify';
```

## Library ##

### Functions ###

##### Param #####

Get `param` from `collection`. Uses `default` when not found.

```sass
$param: param($name, $collection, $default: false);
```

##### Strip-unit #####

Strip `unit` from value.

```sass
$unit-less: strip-unit($input);
```

#### Rem-calc ####

Convert one or more `pixel` values to `rem` using a base reference e.g. 14px.

```sass
$rem-calc-base: 14px !default;

$rem: rem-calc($values);
```

Dependencies:
- strip-unit

### Mixins ###

##### Fluidify #####

Fluidifies a property, useful for responsive design.

```sass
@include fluidify($property, $params: ());
```

Dependencies:
- param
- strip-unit

##### IcoMoon #####

Add an icon.

```sass
@include icomoon($fontCode);
```

##### Loader #####

Creates an animated loader, with default `1 sec` delay.

```sass
@include loading($params: ());
```

Dependencies:
- param