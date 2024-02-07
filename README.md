# Publish Action Package

_This action_ packages _your action_ as OCI artifacts and publishes it to the [GitHub Container registry](ghcr.io).

This allows your action to be consumed as an _immutable_ package even if a [SemVer](https://semver.org/) is specified in the consumer's workflow file.

Your action workflow must be triggered on `release` as in the following example. The release's title must follow [semantic versioning](https://semver.org/).
Then consumers of your action will then be able to specify the version, e.g., `- uses: your-name/your-action@v1.2.3` or even `- uses: your-name/your-action@v1`.

## Usage

<!-- start usage -->
```yaml
on:
  release:

- uses: immutable-actions/publish-action-package@v1
```
<!-- end usage -->

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).
