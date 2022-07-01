![LOGFORCE logo](https://avatars.githubusercontent.com/u/105729788)
# LOGFORCE Docs
Welcome to the LOGFORCE docs — This is a draft of the core concepts available in LOGFORCE platform.
## Document store
### Initial architecture
Embedded transactional database in the form of a key-value store
### Data model and Schema
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
    "cat": "Category { \"type\": \"string\" }",
    "observer": {
      "observables": {
        "sourceType": "Log source type according to sourcetype.md { \"type\": \"string\" }",
        "mapping": {
          "frameworks": {
            "framework": {
              "frameworkName": "Cybersecurity Framework { \"type\": \"string\" }",
              "ttpId": "Tactic, Technique or Procedures ID { \"type\": \"string\" }"
            }
          }
        },
        "references": {
          "reference": "KB URL { \"type\": \"string\" }",
          
        }
      }
    }
  }
]
```
