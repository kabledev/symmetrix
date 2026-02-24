# Symmetrix

A lightweight CSS framework built with Sass. Provides practical, reusable utility classes for Sass-based projects.

## Installation

```bash
npm install symmetrix
```

## Basic Usage

```scss
// style.scss

@use "symmetrix";
// or
@forward "symmetrix";
```

## Customize

To customize the default variables, import each module separately. This allows you to configure `abstracts` before the rest of the framework loads.

```scss
// style.scss

@use "symmetrix/abstracts/vars" with (
  $theming: (
    fontFamily: (
      "Roboto, sans-serif",
    ),
    fontSize: 1rem,
    lineHeight: 1.25,

    colorScheme: (
      light: (
        bgColor: white,
        textColor: var(--sym-gray-800),
        headingColor: var(--sym-gray-950),
        borderColor: var(--sym-gray-200),
      ),
      dark: (
        bgColor: var(--sym-gray-950),
        textColor: var(--sym-gray-100),
        headingColor: white,
        borderColor: var(--sym-gray-800),
      ),
    ),
  )
);

@forward "symmetrix/base";
@forward "symmetrix/layout";
@forward "symmetrix/elements";
@forward "symmetrix/utils";
```

## Modules

| Module                | Description                  |
| --------------------- | ---------------------------- |
| `symmetrix/abstracts` | Variables, functions, mixins |
| `symmetrix/base`      | Reset and base styles        |
| `symmetrix/layout`    | Grid and layout utilities    |
| `symmetrix/elements`  | HTML element styles          |
| `symmetrix/utils`     | Utility classes              |


## License

MIT