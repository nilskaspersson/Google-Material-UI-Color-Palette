## Sass Maps of the Google Material UI Color Palette
Here are Sass maps of the [Color Palette](http://www.google.com/design/spec/style/color.html#color-ui-color-palette) found in the [Google Material UI](http://www.google.com/design/spec/).

### Usage
Use `map-get($color, $value)` ([reference](http://sass-lang.com/documentation/Sass/Script/Functions.html#map_get-instance_method)) using the color names and values from the *Material UI* specification. Spaces in color names are replaced with a single dash (-).

Bundled is a custom function to improve the semantics of the color palette:

```
@function color($color, $value: 500) {
  @return map-get($color, $value);
}
```

Which can be used like this:

```
.element {
  background: color($indigo, 400);
}
```

Do note that if no `$value` is set, it defaults to the primary color value of `500`.

### Requirements
[Sass 3.3 (Maptastic Maple)](http://sass-lang.com/)
