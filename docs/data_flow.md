# Spotify Project Pipeline

```mermaid
graph TD
    A[Raw Data: CSV/JSON] --> |Data Governance Gate| B(Python Processing)
    B --> C{PII Check}
    C -->|Level 3| D[Dropped]
    C -->|Clean| E{DQ Validation}
    E -->|Rejected| F[Log Error]
    E -->|Passed| G[Formatted Data]
    G --> H[(SQLite DB)]
    H --> I[Power BI Dashboard]
```

**1. Source Layer:**
* `data/raw/kaggle_spotify.csv`
* `data/raw/spotify_history_2025.json` (When available)

**2. Processing Layer (Python):**
* **Anonymizer:** Drop Level 3 PII (Email, IP).
* **Validator:** Apply `quality_rules.md` (Drops DQ-01/02/03, Transforms DQ-05/06/07/08/09).
* **Formatter:** Ensure keys are uppercase and dates are correctly typed.

**3. Storage Layer (SQLite):**
* Data is loaded into the `spotify_tracks` table defined in the `schema.sql`.

**4. Presentation Layer (Power BI):**
* Direct connection to the `.db` file for visualization.
