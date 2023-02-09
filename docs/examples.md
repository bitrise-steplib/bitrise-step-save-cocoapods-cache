### Examples

#### Minimal example
```yaml
steps:
- restore-cocoapods-cache@1: {}
- cocoapods-install@2: {}
- save-cocoapods-cache@1: {}
```

Check out [Workflow Recipes](https://github.com/bitrise-io/workflow-recipes#-key-based-caching-beta) for other caching examples!
