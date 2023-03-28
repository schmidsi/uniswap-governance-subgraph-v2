# Query from https://uniswap.org/

```json
{
  "variables": {},
  "query": "{\n  governance(id: \"GOVERNANCE\") {\n    totalDelegates\n    __typename\n  }\n}\n"
}
```

Translates into

```graphql
{
  governance(id: "GOVERNANCE") {
    totalDelegates
    __typename
  }
}
```

## Other queries

```
{
  proposals(orderDirection: desc, orderBy: creationBlock) {
    description
    id
    votes {
      id
      votes
      votesRaw
      voter {
        id
      }
    }
  }
}
```

```bash
yarn graph deploy --node https://api.thegraph.com/deploy/ --ipfs https://api.thegraph.com/ipfs/ schmidsi/test-cli
```
