# rules

Shared personal rule sets for Surge and Clash/mihomo.

## Files

- `rules/domestic.list`: manually maintained rules that should use the domestic policy.

## Surge

```ini
RULE-SET,https://raw.githubusercontent.com/itsmaiGe/rules/main/rules/domestic.list,国内
```

## Clash/mihomo

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
