# Changing the colors

As any proper Material Design implementation, Material for MkDocs supports
Google's original [color palette], which can be easily configured through
`mkdocs.yml`. Furthermore, colors can be customized with a few lines of CSS to
fit your brand's identity by using [CSS variables][custom colors].

  [color palette]: http://www.materialui.co/colors
  [custom colors]: #custom-colors

## Configuration

### Color palette

#### Color scheme

<!-- md:version 5.2.0 -->
<!-- md:default `default` -->

Material for MkDocs supports two color schemes: a __light mode__, which is just
called `default`, and a __dark mode__, which is called `slate`. The color scheme
can be set via `mkdocs.yml`:

``` yaml
theme:
  palette:
    scheme: default
```

Click on a tile to change the color scheme:

<div class="mdx-switch">
  <button data-md-color-scheme="default"><code>default</code></button>
  <button data-md-color-scheme="slate"><code>slate</code></button>
</div>

<script>
  var buttons = document.querySelectorAll("button[data-md-color-scheme]")
  buttons.forEach(function(button) {
    button.addEventListener("click", function() {
      document.body.setAttribute("data-md-color-switching", "")
      var attr = this.getAttribute("data-md-color-scheme")
      document.body.setAttribute("data-md-color-scheme", attr)
      var name = document.querySelector("#__code_0 code span.l")
      name.textContent = attr
      setTimeout(function() {
        document.body.removeAttribute("data-md-color-switching")
      })
    })
  })
</script>

#### Primary color

<!-- md:version 0.2.0 -->
<!-- md:default `indigo` -->

The primary color is used for the header, the sidebar, text links and several
other components. In order to change the primary color, set the following value
in `mkdocs.yml` to a valid color name:

``` yaml
theme:
  palette:
    primary: indigo
```
