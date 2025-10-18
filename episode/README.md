# Episode by ID – GraphQL

Fetch details of specific Rick & Morty episodes using `episode(id: ID!)`.

## Endpoint

GraphQL: https://rickandmortyapi.com/graphql

## Required fields

`id`, `name`, `air_date`, `episode`

## Files

- `episode-id-1.graphql` → `episode-id-1-output.json`
- `episode-id-2.graphql` → `episode-id-2-output.json`
- `episode-id-3.graphql` → `episode-id-3-output.json`
- `episode-id-4.graphql` → `episode-id-4-output.json`

## How to run (examples)

### GraphiQL / IDE

1. Open the endpoint in a GraphQL IDE.
2. Paste one of the `.graphql` queries.
3. Execute it.
4. Copy the exact JSON response into the matching `*-output.json`.

### cURL

```bash
curl -s -X POST https://rickandmortyapi.com/graphql \
  -H "Content-Type: application/json" \
  -d '{ "query": "query EpisodeById1 { episode(id: 1) { id name air_date episode } }" }' \
  > episode-id-1-output.json
```
