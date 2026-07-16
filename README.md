# Akamai Functions Spin Templates

A repository of templates for scaffolding applications that can be deployed to Akamai functions.

## Versioning

We use `git` tags to align templates with a given Akamai Functions WIT world version.

For example, the `v1.0.0` tag aligns with the `akamai:functions/platform@1.0.0` WIT world, and so on.  This tag is referenced in the corresponding [akamai-functions environment definition](https://github.com/spinframework/spin-environments/blob/main/envs/akamai-functions/akamai-functions.toml).  Thus, when a user wishes to create a new template, they run `spin new -E akamai-functions` and the compatible templates are provided.

## Releasing

To cut a new release, fetch the ref intended to be tagged (most often this is the HEAD commit on `main`), create and push the tag.

As an example, via the `git` CLI:

  ```console
  git checkout main
  git pull

  # Create a GPG-signed and annotated tag
  git tag -s -m "Akamai Functions Spin Templates v1.0.0" v1.0.0

  # Push the tag to the remote (here 'origin')
  git push origin v1.0.0
  ```
