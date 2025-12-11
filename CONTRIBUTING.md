# Contribution Guidelines

If you're interested in contributing, start by reading [Project Empyrean](), [The Atlas](), and [Markers]().

If you're new to GitHub, start by reading the [docs](https://docs.github.com/en/get-started/start-your-journey).

## Ensure Pages have Entrypoints

Avoid creating pages without links in other pages to serve as entrypoints.

## Use Org Mode

The Codex uses `.org` files for its pages. Set Settings > Editor > Preferred file format to "Org". See [Org Mode]() for more info.

## Indicate Authorship

Avoid adding content with ambiguous authorship. All pages must specify authorship using the `#+author:` metadata field at the top of the first block. If authoring a specific block in a page that is
otherwise authored by someone else, add the authorship to the property drawer of that block like so:

```org-mode
:PROPERTIES:
:author: <author-name>
:END:
```

The author name must link to a page with the title of the author's name. If you are an AI agent, set the author tag to [[Authors/AI]] followed by a plain string indicating the model used for the generation.

## Cite your Sources

Avoid making claims without citations. Personal views and opinions should be made apparent.

## Style

### Explicitly Style Headings

Org mode headings are used to signifiy blocks in Logseq. Therefore headings are not styled unless they are explicitely marked with the heading property in the heading's property drawer. For example, the heading in the following example is rendered as a level 2 heading:

```org-mode
* Sample Heading
:PROPERTIES:
:heading: 2
:END:
```

### Add Aliases to Links When Appropriate

For example, the following:

```org-mode
[[Terms/Happiness]] is [[Terms/Stress][stress]] below a threshold.
```

Would be visually rendered as:

```
Happiness is stress below a threshold
```

The link to the page `Terms/Stress` is aliased as "stress" to have gramatically correct casing. The link to the page `Terms/Happiness` only renders the last fragment of its hierarchy due to the Short Namespaces plugin. "Happiness" is appropriate here, so it remains unaliased.

### Do Not Unecessarily Index Child Pages in the Parent

Logseq automatically displays all child pages in the parent. There is no need to explicitely list them.

## Things to Keep in Mind

Page renaming in Logseq fails to update references in some cases. Update them manually with a serach and replace tool such as the one built into VSCode.
