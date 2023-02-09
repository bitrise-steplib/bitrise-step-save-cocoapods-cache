# Save Cocoapods Cache

[![Step changelog](https://shields.io/github/v/release/bitrise-steplib/bitrise-step-save-cocoapods-cache?include_prereleases&label=changelog&color=blueviolet)](https://github.com/bitrise-steplib/bitrise-step-save-cocoapods-cache/releases)

Caches the Pods folder. This Step needs to be used in combination with **Restore Cocoapods Cache**.

<details>
<summary>Description</summary>

Caches dependencies in the Pods folder. This Step needs to be used in combination with **Restore Cocoapods Cache**.

This Step is based on [key-based caching](https://devcenter.bitrise.io/en/builds/caching/key-based-caching.html) and sets up the cache key and path automatically for Cocoapods dependencies. If you'd like to change the cache key (or paths to cache), you might want to use the generic [Save cache](https://github.com/bitrise-steplib/bitrise-step-save-cache) Step instead.

#### Related steps

[Restore Cocoapods cache](https://github.com/bitrise-steplib/bitrise-step-restore-cocoapods-cache/)

[Save cache](https://github.com/bitrise-steplib/bitrise-step-save-cache/)

</details>

## 🧩 Get started

Add this step directly to your workflow in the [Bitrise Workflow Editor](https://devcenter.bitrise.io/steps-and-workflows/steps-and-workflows-index/).

You can also run this step directly with [Bitrise CLI](https://github.com/bitrise-io/bitrise).

### Examples

#### Minimal example
```yaml
steps:
- restore-cocoapods-cache@1: {}
- cocoapods-install@2: {}
- save-cocoapods-cache@1: {}
```

Check out [Workflow Recipes](https://github.com/bitrise-io/workflow-recipes#-key-based-caching-beta) for other caching examples!


## ⚙️ Configuration

<details>
<summary>Inputs</summary>

| Key | Description | Flags | Default |
| --- | --- | --- | --- |
| `verbose` | Enable logging additional information for troubleshooting | required | `false` |
</details>

<details>
<summary>Outputs</summary>
There are no outputs defined in this step
</details>

## 🙋 Contributing

We welcome [pull requests](https://github.com/bitrise-steplib/bitrise-step-save-cocoapods-cache/pulls) and [issues](https://github.com/bitrise-steplib/bitrise-step-save-cocoapods-cache/issues) against this repository.

For pull requests, work on your changes in a forked repository and use the Bitrise CLI to [run step tests locally](https://devcenter.bitrise.io/bitrise-cli/run-your-first-build/).

**Note:** this step's end-to-end tests (defined in `e2e/bitrise.yml`) are working with secrets which are intentionally not stored in this repo. External contributors won't be able to run those tests. Don't worry, if you open a PR with your contribution, we will help with running tests and make sure that they pass.


Learn more about developing steps:

- [Create your own step](https://devcenter.bitrise.io/contributors/create-your-own-step/)
- [Testing your Step](https://devcenter.bitrise.io/contributors/testing-and-versioning-your-steps/)
