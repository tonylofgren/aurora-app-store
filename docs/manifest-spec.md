# Aurora App Manifest Specification

Each Aurora app repository must include `aurora-manifest.json` in the repository root.

## Required fields
| Field | Type | Description |
|-------|------|-------------|
| id | string | Unique lowercase identifier |
| display_name | string | Human-readable name |
| author | string | App creator |
| description | string | Short description |
| category | string | e.g. entertainment, tools |
| channel | string | "core" or "community" |
| min_aurora_version | string | Minimum Aurora version (e.g. 2.5.0) |
| repository | string | GitHub repo URL |

## Optional fields
`documentation`, `icon`, `translations`, `permissions`, `entrypoint`

## GitHub Topics
- Required: `aurora-app`
- Optional: `aurora-category-<category>`

## Example
```json
{
  "id": "music_light_show",
  "display_name": "Falcon FPP Player",
  "author": "Aurora Community",
  "description": "Integrate Falcon Player (FPP) with Aurora for synchronized light shows.",
  "category": "entertainment",
  "channel": "core",
  "repository": "https://github.com/tonylofgren/FPP-Plugin-ChatGPT",
  "min_aurora_version": "2.4.0",
  "documentation": "https://github.com/tonylofgren/FPP-Plugin-ChatGPT#readme"
}
