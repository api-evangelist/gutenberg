# Project Gutenberg

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
