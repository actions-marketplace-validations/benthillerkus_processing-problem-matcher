# processing-problem-matcher

Github Action to [problem match](https://github.com/actions/toolkit/blob/master/docs/problem-matchers.md)
output from `processing-java`. This allows warnings and errors from the compiler to be
prominently featured in pull requests like so:

![Matcher in action in pull request](/images/example-pull-request.png?raw=true)

This is a direct port of the `$gcc` rule from [vscode-cpptools](https://github.com/microsoft/vscode-cpptools).
Typical usage will be:

```yaml
    - uses: benthillerkus/processing-problem-matcher@master
    - name: Build Project
      run: processing-java --sketch={{ $github.workspace }} --build
```

**Note that this action does not build your code for you. It only makes the
errors and warnings from your compiler more prominent.**

## Development

TODO: Use a more sophisticated matcher
