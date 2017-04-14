# eslint-plugin-yacomma-spacing

Yet another comma-spacing

## rules

標準のcomma-spacingではafterをtrueに設定していると以下の書き方で警告が出る

```.js
var hoge = {
	a: 1
	,b:2
};
```

エラーを回避するためには,のあとにスペースが必要

```.js
var hoge = {
	a: 1
	, b:2
};
```

yacomma-spacingではignoreIfFirstTokenOfLineオプションを設定することで  
行頭のカンマの後にスペースを入れる必要がなくなる

```.yml
---
plugins:
  - yacomma-spacing
  comma-spacing:
    - off
rules:
  yacomma-spacing/yacomma-spacing:
    - warn
    - before: false
      after: true
      ignoreIfFirstTokenOfLine: true
```
