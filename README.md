# buildkite-pipelines

[![License][licensebadge]](LICENSE)

[licensebadge]: https://img.shields.io/github/license/seankhliao/buildkite-pipelines.svg?style=flat-square

A central repo for confguring standard CI pipelines for buildkite for my repos.
Allows updating all repos at once.
Use by passing getting the contents of a file over HTTPS and passing that to buildkite-agent via stdin.
Example:

```yaml
steps:
  - label: ":pipeline:"
    command: "curl https://raw.githubusercontent.com/seankhliao/buildkite-pipelines/main/go-library.yaml | buildkite-agent pipeline upload"
```
