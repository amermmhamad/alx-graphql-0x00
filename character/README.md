# Character by ID – GraphQL

This folder contains GraphQL queries and outputs for fetching Rick & Morty characters by ID using the `character(id: ID!)` field.

## Endpoint

GraphQL: https://rickandmortyapi.com/graphql

## Queries

Each `.graphql` file contains a query for a single character ID requesting:
`id`, `name`, `status`, `species`, `type`, `gender`.

- `character-id-1.graphql`
- `character-id-2.graphql`
- `character-id-3.graphql`
- `character-id-4.graphql`

## How to run

### Option A: GraphiQL (in browser)

1. Open the endpoint in a GraphQL IDE (e.g., GraphiQL/Insomnia/Postman).
2. Paste the contents of a `.graphql` file.
3. Execute the query.
4. Copy the exact JSON response into the corresponding `*-output.json` file.

### Option B: cURL

Use cURL to POST a query. Example for ID 1:

```bash
curl -X POST https://rickandmortyapi.com/graphql \
  -H "Content-Type: application/json" \
  -d '{ "query": "query CharacterById1 { character(id: 1) { id name status species type gender } }" }' \
  | jq > character-id-1-output.json
```
