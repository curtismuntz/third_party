# third_party

This repo is intended to host build files/definitions for common cpp third party code. It should always be considered unstable, and tested only to the extent that targets within `//examples` build and run.

To use any of the targets defined via `rules_foreign_cc`, be sure to follow the warnings and usage instructions on the github repo: https://github.com/bazelbuild/rules_foreign_cc

To try:
`bazel build examples/opencv`.

If you would like to use these, please contribute back by submitting issues and merge requests! Please include examples for any third party library that you add.

## OpenCV
Known issues:
  * Must be built with `--spawn_strategy=standalone`.
  * Anything hi-gui related will not work as defined here.

