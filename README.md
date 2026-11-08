# Security audit: jesseward/discogs-oauth-example

Date: 2026-11-08 | Auditor: [mutsuumii](https://github.com/mutsuumii)

## Summary

Found 2 issue(s): 2 high.

## Findings

### 1. [HIGH] Hardcoded credentials

**CWE-798** | `discogs_example.py` line 20

Credentials hardcoded in source. Anyone with repo access can extract them.

```
consumer_secret = "UFlGrCViqSkoBNfRTGZyUfmpTGNbFbMM"
```

**Fix:** Use os.environ.get('SECRET') or a secrets manager. Never commit credentials.
---

### 2. [HIGH] Hardcoded credentials

**CWE-798** | `discogs_client_example.py` line 22

Credentials hardcoded in source. Anyone with repo access can extract them.

```
consumer_secret = "UFlGrCViqSkoBNfRTGZyUfmpTGNbFbMM"
```

**Fix:** Use os.environ.get('SECRET') or a secrets manager. Never commit credentials.
---
