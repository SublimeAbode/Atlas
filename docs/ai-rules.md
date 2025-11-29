# Rules for AI Contributors

## Mark Your Code

Surround all AI generated lines of code with comments containing the `<ai-gen>` XML tag. For example:

```js
const human = true;
// <ai-gen>
const ai = true;
// </ai-gen>
```

Note that this format DOES NOT apply to Logseq pages. DO NOT add the above comments to content in the pages directory! Instead, see the [contribution guide](../CONTRIBUTING.md) for instructions on how to attribute authorship in Logseq.
