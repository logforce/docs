![LOGFORCE logo](https://avatars.githubusercontent.com/u/105729788)
# LOGFORCE Docs
Welcome to the LOGFORCE docs — This is a draft of the core concepts available in LOGFORCE platform.
## Document store
### Initial architecture
Embedded transactional database in the form of a key-value store
### Data model and Schema
![LOGFORCE model](https://github.com/logforce/docs/blob/main/images/logforce_model.svg)
#### YAML
```yaml
- id: 'Unix time stamp + UID { "type": "integer" }'
  logType: 'Log type { "type": "string" }'
  pokeAi: 'Poke AI .jpg private URL { "type": "string" }'
  fuzzyHash: 'SSDEEP { "type": "string" }'
  author: 'Author { "type": "string" }'
  synthetic: 'GAN generated { "type": "boolean" }'
  anonymized: 'Anonymized { "type": "boolean" }'
  lines: 'Number of log lines { "type": "integer" }'
  lineSeparator: 'Line separator { "type": "string" }'
  characters: 'Log character count { "type": "integer" }'
  cat: 'Categories { "type": "string" }'
  tag: 'Tags { "type": "string" }'
  observer:
    observables:
      sourceType: 'Log source type according to sourcetype.md { "type": "string" }'
      mapping:
        frameworks:
          framework:
            frameworkName: 'Framework { "type": "string" }'
            mappingId: 'Framework item(s) ID(s) { "type": "string" }'
      references:
        reference: 'KB URL { "type": "string" }'
      correlations:
        correlation: 'Query { "type": "string" }'
  log:
    lines: 'Log lines { "type": "string" }'
  origin:
    originalLocation: 'Log original location { "type": "string" }'

```

#### JSON
```json
[
  {
    "id": "Unix time stamp + UID { \"type\": \"integer\" }",
    "logType": "Log type { \"type\": \"string\" }",
    "pokeAi": "Poke AI .jpg private URL { \"type\": \"string\" }",
    "fuzzyHash": "SSDEEP { \"type\": \"string\" }",
    "author": "Author { \"type\": \"string\" }",
    "synthetic": "GAN generated { \"type\": \"boolean\" }",
    "anonymized": "Anonymized { \"type\": \"boolean\" }",
    "lines": "Number of log lines { \"type\": \"integer\" }",
    "lineSeparator": "Line separator { \"type\": \"string\" }",
    "characters": "Log character count { \"type\": \"integer\" }",
    "cat": "Categories { \"type\": \"string\" }",
    "tag": "Tags { \"type\": \"string\" }",
    "observer": {
      "observables": {
        "sourceType": "Log source type according to sourcetype.md { \"type\": \"string\" }",
        "mapping": {
          "frameworks": {
            "framework": {
              "frameworkName": "Framework { \"type\": \"string\" }",
              "mappingId": "Framework item(s) ID(s) { \"type\": \"string\" }"
            }
          }
        },
        "references": {
          "reference": "KB URL { \"type\": \"string\" }"
        },
        "correlations": {
          "correlation": "Query { \"type\": \"string\" }"
        }
      }
    },
    "log": {
      "lines": "Log lines { \"type\": \"string\" }"
    },
    "origin": {
      "originalLocation": "Log original location { \"type\": \"string\" }"
    }
  }
]
```
