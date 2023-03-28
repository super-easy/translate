# translate
Call Translate api to translate one or more characters

# Installation
>go get github.com/super-easy/translate

# Example
```go
package main

import (
	"github.com/super-easy/translate"
	"fmt"
)

func main() {
	query := "感谢"

	result := translate.Google("zh", "cht", query, "")
	fmt.Println(result)

	result = translate.Google("zh", "en", query, "")
	fmt.Println(result)

	result = translate.Google("zh", "jp", query, "")
	fmt.Println(result)

	querys := []string{"你好", "全球"}

	results := translate.Googles("zh", "cht", querys, "")
	fmt.Println(results)

	results = translate.Googles("zh", "en", querys, "")
	fmt.Println(results)

	results = translate.Googles("zh", "jp", querys, "")
	fmt.Println(results)
}
// OutPut:
// 感謝
// Thank
// ありがとうございます
// [你好 全球]
// [Hello. Global]
// [こんにちは グローバル]
```
