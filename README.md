# Project Gutenberg

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Project Gutenberg is a free ebook library providing access to over 75,000 public domain books. Founded in 1971, it is the oldest digital library and offers ebooks primarily for works whose U.S. copyright has expired. The Gutendex API provides a JSON REST interface for searching and accessing Project Gutenberg's catalog of bibliographic metadata.

## API

The primary programmatic interface is the [Gutendex API](https://gutendex.com/), a community-maintained JSON web API that indexes Project Gutenberg catalog data updated nightly from official XML/RDF archives.

**Base URL:** `https://gutendex.com`

**Key Endpoint:** `GET /books` — returns paginated book metadata

**No authentication required.**

### Query Parameters

| Parameter | Description |
|---|---|
| `search` | Search author names and book titles |
| `languages` | Comma-separated ISO two-character language codes (e.g., `en,fr`) |
| `ids` | Comma-separated Project Gutenberg ID numbers |
| `copyright` | Filter by copyright status: `true`, `false`, or `null` |
| `topic` | Search bookshelves and subjects |
| `author_year_start` | Filter by author birth year (supports BCE with negative values) |
| `author_year_end` | Filter by author death year |
| `mime_type` | Filter by file MIME type prefix |
| `sort` | Sort order: `popular` (default), `ascending`, `descending` |

### Individual Book

`GET /books/{id}` — retrieve a specific book by Project Gutenberg ID number.

## Data Access Alternatives

- **OPDS Feed:** `https://www.gutenberg.org/ebooks/search.opds/`
- **Daily XML/RDF Catalog:** `https://www.gutenberg.org/cache/epub/feeds/`
- **Weekly CSV Catalog:** Available at the offline catalogs page
- **RSS Feed:** `https://www.gutenberg.org/cache/epub/feeds/today.rss`

## Links

- [Website](https://www.gutenberg.org/)
- [Gutendex API](https://gutendex.com/)
- [Gutendex GitHub](https://github.com/garethbjohnson/gutendex)
- [GitHub Organization](https://github.com/gutenbergtools)
- [Offline Catalogs](https://www.gutenberg.org/ebooks/offline_catalogs.html)
- [Robot Access Policy](https://www.gutenberg.org/policy/robot_access.html)
- [Mirroring Guide](https://www.gutenberg.org/help/mirroring.html)
