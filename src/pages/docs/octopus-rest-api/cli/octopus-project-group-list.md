---
layout: src/layouts/Default.astro
pubDate: 2023-01-01
title: octopus project-group list
description: List project groups
navOrder: 84
---

List project groups in Octopus Deploy


```
Usage:
  octopus project-group list [flags]

Aliases:
  list, ls

Global Flags:
  -h, --help                   Show help for a command
      --no-prompt              Disable prompting in interactive mode
  -f, --output-format string   Specify the output format for a command ("json", "table", or "basic") (default "table")
  -s, --space string           Specify the space for operations

```

## Examples

!include <samples-instance>


```
$ octopus project-group list
$ octopus project-group ls


```

## Learn more

- [Octopus CLI](/docs/octopus-rest-api/cli/index.md)
- [Creating API keys](/docs/octopus-rest-api/how-to-create-an-api-key.md)