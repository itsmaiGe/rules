# rules

自己用的分流规则。

`rules/domestic.list` 里面都是我手动加的、需要走国内分流的网站。

## Surge 写法

```ini
RULE-SET,https://raw.githubusercontent.com/itsmaiGe/rules/main/rules/domestic.list,国内
```

## Clash / mihomo 写法

```yaml
rule-providers:
  manual-domestic:
    type: http
    behavior: classical
    format: text
    url: "https://raw.githubusercontent.com/itsmaiGe/rules/main/rules/domestic.list"
    path: ./ruleset/manual-domestic.list
    interval: 86400

rules:
  - RULE-SET,manual-domestic,DIRECT
```

要加网站就直接改 `rules/domestic.list`。
