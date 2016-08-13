
## Generating the table of contents

`documentr` can automatically generate the table of contents for your documentation, 
simply by entering the following line into you `documentr.json` file:

```
{ "type": "markup", "value": "\n\n# Table of Contents\n\n" },

{ "type": "toc", "value": "2" },
{ "type": "toclinks", "value": "true" },
```

By default, no title is generated - you will need to include one as simple markup.

This will generate both the table of contents and the links to all of the headers.

The `{ "type": "toc", "value": "2" }` line will generate links up to `h2` elements, by 
default headers up to level 6 are generated.

The `{ "type": "toclinks", "value": "true" },` line will generate links to the headers,
and will only work if `"type": "toc"` is also included.

> By default, links are not generated.  Unfortunately the developer of the markdown  processor that is in use, does not distinguish block quote level elements correctly  such that anything that looks like a header included in a blockquote will also be  incorrectly identified as a header.

