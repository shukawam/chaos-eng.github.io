# Principles of Chaos Engineering


This is the source for [principlesofchaos.org](https://principlesofchaos.org).

It's a static site, generated with [hugo].

Theme used:
[DenisBalan/hugo-theme-pixyll](https://github.com/DenisBalan/hugo-theme-pixyll)
(a slightly modified version of [hugo-theme-pixyll](https://github.com/azmelanar/hugo-theme-pixyll))

[hugo]: https://gohugo.io/getting-started/


## Prereqs

* Install [hugo] so you can generate the html
* Check out the submodule that contains the Hugo theme:

```bash
git submodule init
git submodule update
```

## Add a translation in a new language

1. Identify the [ISO 639-1 two-letter code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for your language (e.g., `pl` for Polish).
1. Create a `content/_index.xx.md` file (where `xx` is the two-letter country code), and populate it with the text. See the [content](content) directory for examples of the format.
1. Edit the [config.toml](config.toml) file and add a `[Languages.xx]` line under the `[Languages]` section, in alphabetical order.
1. (Optional): Test locally: `hugo server -D` and point your browser at the local server
1. Commit all of the edited files: `git add config.toml && git add content/_index.xx.md`
