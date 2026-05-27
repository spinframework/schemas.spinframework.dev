# Spin JSON (TOML) Schemas

The repo (branch) contains [JSON Schema](https://json-schema.org/) for Spin
configuration files.

> Note: As of this writing this is an "[orphan
> branch](https://git-scm.com/docs/git-checkout/2.14.6#Documentation/git-checkout.txt---orphannewbranch)"
> in the Spin repo itself.

Tools like [Taplo](https://taplo.tamasfe.dev/) can validate TOML files against
JSON Schema fetched from a URL specified in a ["schema
directive"](https://taplo.tamasfe.dev/configuration/directives.html#the-schema-directive).

## Spin Manifest Schema

It can be referenced in a `spin.toml` file:

```toml
#:schema https://schemas.spinframework.dev/spin/manifest-v2/latest.json
```

### Updating

```shell
$ spin maintenance generate-manifest-schema -o spin/mainfest-v2/latest.json
```

Merging into this branch will automatically deploy to
`https://schemas.spinframework.dev`.