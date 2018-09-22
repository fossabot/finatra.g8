This is a Giter8 template for Finatra

```
sbt new forthy/finatra.g8
```

[License](./LICENSE)

# Notes
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FJamesJJ%2Ffinatra.g8.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FJamesJJ%2Ffinatra.g8?ref=badge_shield)


Giter8 will apply templating to the contents of `src/main/g8`, using the `default.properties` file within that directory as the prompts for templating.

Giter8 also supports scaffolding using the *sbt-giter8-scaffold* plugin. There are some intricacies to scaffolding to note:

* `src/main/scaffolds` is copied to the output directory as `.g8`
* directories immediately below `src/main/scaffolds` are the templates available
* scaffolding can have its own prompts, but Giter8 doesn't apply template replacements against scaffolds (otherwise, the output files would no longer be templates), so a templated `.g8/controllers/default.properties` file exists.
* The property `name` has special meaning in Giter8, and is used to identify module outputs. 
    For example a template defined with `controlers/src/main/scala/$name$.scala` and `name=plugin` will result in the output `plugin/controlers/src/main/scala/plugin.scala`. This can be unintuitive, which is why it's documented here

Any files you *don't* want to have templating applied against can be defined in `default.properties` as regex in the space-delimited `verbatim` prompt.


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FJamesJJ%2Ffinatra.g8.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FJamesJJ%2Ffinatra.g8?ref=badge_large)