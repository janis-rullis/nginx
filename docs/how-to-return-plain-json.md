---
title: How to return plain JSON?
layout: default
---

### / [nginx](./../) / [docs](./)

-----------------------------------------------------------------------------------

# How to return plain JSON?

```
location @debug {
        default_type application/json;
        return 200 ' {
            "request_uri": "$request_uri", "uri": "$uri", "args": "$args",
            "request_header": "$http_language"
        }
        ';
}
```