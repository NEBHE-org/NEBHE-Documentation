# Changing the language

Material for MkDocs supports internationalization (i18n) and provides
translations for template variables and labels in 60+ languages. Additionally,
the site search can be configured to use a language-specific stemmer, if
available.

## Configuration

### Site language

<!-- md:version 1.12.0 -->
<!-- md:default `en` -->

You can set the site language in `mkdocs.yml` with:

``` yaml
theme:
  language: en # (1)!
```

1.  HTML5 only allows to set a [single language per document], which is why
    Material for MkDocs only supports setting a canonical language for the
    entire project, i.e. one per `mkdocs.yml`.

    The easiest way to build a multi-language documentation is to create one
    project in a subfolder per language, and then use the [language selector]
    to interlink those projects.

The following languages are supported:

<!-- hooks/translations.py -->

Note that some languages will produce unreadable anchor links due to the way
the default slug function works. Consider using a [Unicode-aware slug function].

!!! tip "Translations missing? Help us out, it takes only 5 minutes"

    Material for MkDocs relies on outside contributions for adding and updating
    translations for the almost 60 languages it supports. If your language shows
    that some translations are missing, click on the link to add them. If your
    language is not in the list, click here to [add a new language].

### Site language selector

<!-- md:version 7.0.0 -->
<!-- md:default none -->

If your documentation is available in multiple languages, a language selector
pointing to those languages can be added to the header. Alternate languages
can be defined via `mkdocs.yml`.

``` yaml
extra:
  alternate:
    - name: English
      link: /en/ # (1)!
      lang: en
    - name: Deutsch
      link: /de/
      lang: de
```

1.  Note that this must be an absolute link. If it includes a domain part, it's
    used as defined. Otherwise the domain part of the [`site_url`][site_url] as
    set in `mkdocs.yml` is prepended to the link.
