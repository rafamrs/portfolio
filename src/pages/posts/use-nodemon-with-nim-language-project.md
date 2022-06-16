---
title: 'Go function to check if string contains prefix'
publishDate: 2021-02-25T09:15:00Z
tag: Go
---

This is how to quickly check if a certain string contains a specific prefix. This is usefull when you're checking commands for example.

```go
strings.HasPrefix(content, prefix)
```

We use the strings package to check this. Here is a full example of a tiny application.

```go
package main

import (
	"strings"
)

func main() {
	content := "!command test-users"
	fmt.Println(hasPrefix(content, "!command"))
}

func hasPrefix(content string, prefix string) bool {
	return strings.HasPrefix(content, prefix)
    // returns true in this example
}
```