# Exploreme validator registry


## Overview

This repository serves as a repository where validators can send requests to the pool, and after its approval, information about the validator will appear in the explorer.

## Repository structure

The repository follows a simple structure to organize validator data:

```
validators/
├── STAKEME.json
├── validator-name-2.json
├── validator-name-3.json
└── ...
```

### Directory structure explanation

- **Root level**: `validators/` - Main directory containing all validator data
- **File level**: `validator-moniker.json` - Individual validator files named by their moniker/name

## Validator data format

Each validator file must be a JSON file named after the validator's moniker and contain the following structure:

```json
{
  "moniker": "STAKEME",
  "details": "STAKEME helps web 3.0 projects to test their product, and provide the most efficient development support",
  "banner": "https://raw.githubusercontent.com/stakeme-team/contributing-projects/master/files/stakeme-banner.png",
  "avatar": "https://s3.amazonaws.com/keybase_processed_uploads/76937fb26c620e11254b042fe7d73705_360_360.jpg",
  "twitterUrl": "https://x.com/stakeme_pro",
  "githubUrl": "https://github.com/stakeme-team",
  "webUrl": "https://stakeme.pro",
  "identity": "5EAD753536BB995C",
  "securityContact": "team@stakeme.pro",
  "addresses": {
    "somnia": "0xe8e4d93aa612a79d87a8a89af827136d5cbd8f59"
  },
  "bridges": {
    "celestia": "12D3KooWG4hgLXjo6agYdbtQEYuZnNy9ttAnLtNJzsCLVj3kPH4v"
  }
}
```

### Required fields

| Field | Type | Description |
|-------|------|-------------|
| `addresses` | object | Key-value pairs where key is project name and value is validator address |
| `moniker` | string | Human-readable name for the validator |
| `details` | string | Description of the validator and their services |

### Optional fields

| Field | Type | Description |
|-------|------|-------------|
| `banner` | string | URL to validator's banner image |
| `avatar` | string | URL to validator's avatar/logo image |
| `twitterUrl` | string | Twitter/X profile URL |
| `githubUrl` | string | GitHub profile or organization URL |
| `webUrl` | string | Official website URL |
| `identity` | string | Keybase identity or other verification ID |
| `securityContact` | string | Email address for security-related communications |
| `bridges` | object | Key-value pairs where key is project name and value is bridge node hash |

## How to submit your validator information

1. **Fork this repository**
2. **Create your validator file**:
   - Name the file with your validator moniker: `{your-moniker}.json`
   - Place it in the `validators/` directory
   - Follow the JSON format specified above
3. **Submit a Pull Request** with your changes
4. **Wait for review and approval**


## Validation rules

- File names must match the validator moniker specified in the JSON
- JSON must be valid and follow the required schema
- All URLs must be accessible and valid


