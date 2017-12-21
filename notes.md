## observer dconf changes

```
dconf watch /
```

## get variable type

http://docs.ansible.com/ansible/latest/playbooks_filters.html#debugging-filters

```
{{ myvar | type_debug }}
```

## jinja map operation on collection

https://stackoverflow.com/questions/38795908/how-to-select-regex-matches-in-jinja2/38796683#38796683

```
... | map('regex_search',my_pattern) | ...
```

## print predefined variabled (facts)

```
ansible localhost -m setup -c localhost
```

## ad-hoc module invocation

```
ansible localhost -m debug -c local -a "msg='{{ {'a': 'b'} | combine({'q': 'w'}) }}'"
```