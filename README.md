# llms.txt Examples

> Reference implementations of the `llms.txt` standard for marketplaces and e-commerce platforms.

## What is llms.txt?

`llms.txt` is a proposed standard (like `robots.txt` for search engines) that tells AI agents what a website offers and how to interact with it. It's the business card your site hands to every LLM that visits.

**If `robots.txt` says "what you can crawl", `llms.txt` says "what you can DO".**

## Examples

### ReMarket (Agent-Commerce Marketplace)

```
# remarket.de/llms.txt

> ReMarket is a secondhand marketplace in Hannover, Germany.
> AI agents can search, compare prices, and negotiate on behalf of users.

## API
- Base URL: https://api.remarket.de/v1
- Auth: None required for read access
- Rate limit: 100 req/min
- OpenAPI spec: https://api.remarket.de/v1/openapi.yaml

## Actions
- SEARCH: Find listings by query, location, category, price
- READ: Get full listing details including photos and seller info
- PRICE_CHECK: Get AI-powered fair price estimate
- INQUIRE: Ask seller a question (auth required)
- OFFER: Make an offer on a listing (auth required)

## Data Formats
- Listings: Schema.org/Product + Schema.org/Offer
- Locations: Schema.org/PostalAddress (focus: Hannover, Germany)
- Images: WebP, max 2048px, alt-text included

## Trust
- Seller ratings: 1-5 stars, verified after 10 transactions
- Listing quality: AI-scored 1-100
- Response time: Median displayed per seller

## Contact
- API issues: api@remarket.de
- MCP server: https://github.com/altafsvangur-bot/remarket-mcp-server
```

### Generic E-Commerce Template

See `templates/ecommerce.txt` for a ready-to-customize template.

### Generic Marketplace Template

See `templates/marketplace.txt` for multi-seller platforms.

## Structure

```
llms-txt-examples/
├── examples/
│   ├── remarket.txt        # Agent-Commerce marketplace
│   ├── ecommerce.txt       # Generic online shop
│   └── marketplace.txt     # Multi-seller platform
├── templates/
│   ├── ecommerce.txt       # Copy-paste template
│   └── marketplace.txt     # Copy-paste template
├── spec/
│   └── SPEC.md             # Proposed llms.txt specification
└── validators/
    └── validate.py         # Validate your llms.txt
```

## The Case for llms.txt

AI agents are the new browsers. Just as `robots.txt` became essential for SEO, `llms.txt` will become essential for AIO (AI Optimization). Sites without it will be invisible to the next generation of commerce.

## Related

- [remarket-mcp-server](https://github.com/altafsvangur-bot/remarket-mcp-server) — MCP server for ReMarket
- [remarket-openapi-spec](https://github.com/altafsvangur-bot/remarket-openapi-spec) — OpenAPI specification
- [secondhand-schema](https://github.com/altafsvangur-bot/secondhand-schema) — Schema.org extensions

## License

MIT
