# medRxiv

Cold Spring Harbor Laboratory preprint server for health sciences with a REST API for searching and accessing medical and clinical research preprints before peer review.

## API

The medRxiv REST API provides programmatic access to preprint metadata and publication information for health science research. It is free, open, and requires no authentication.

**Base URL:** `https://api.medrxiv.org`

### Endpoints

- **Date-range query:** `https://api.medrxiv.org/details/medrxiv/[YYYY-MM-DD]/[YYYY-MM-DD]/[cursor]/[format]`
- **DOI lookup:** `https://api.medrxiv.org/details/medrxiv/[DOI]/na/[format]`
- **Recent N papers:** `https://api.medrxiv.org/details/medrxiv/[N]/[cursor]/[format]`
- **Recent N days:** `https://api.medrxiv.org/details/medrxiv/[N]d/[cursor]/[format]`

Results are paginated at 100 records per response. Use the `cursor` parameter (integer offset) to iterate through larger result sets.

### Output Formats

- `json` — JSON response
- `xml` — OAI-PMH XML format

### Returned Metadata Fields

- DOI, title, authors, corresponding author and institution
- Publication date, version number
- Abstract, license type, subject category
- Links to preprint page and PDF

## Resources

- [medRxiv Website](https://www.medrxiv.org/)
- [API Documentation](https://api.medrxiv.org/)
- [About medRxiv](https://www.medrxiv.org/about-medrxiv)
