# SubQuery - Dictionary 

This special SubQuery Project provides a dictionary of data that pre-indexes events on chain to dramatically improve indexing the performance of your own SubQuery Project, sometimes up to 10x faster.

It scans over the network, and simply records the module and method for every event/extrinsic on each block - please see the standard entities in `schema.graphql`.

**If you want to create your SubQuery Dictionary to speed up indexing of your own Substrate chain, fork this project and let us know**

# Geting Started
### 1. Install dependencies
```shell
yarn
```

### 2. Generate types
```shell
yarn codegen
```

### 3. Build
```shell
yarn build
```

### 4. Run locally
```shell
yarn start:docker
```

### 5. Launch the playground  
Head over to this
```shell
http://localhost:3000/
```

### 6. Query the extrinsics
In the playground above go and execute the query below
```shell
{
  query {
    extrinsics(first: 10) {
      nodes {
        id
        module
        blockHeight
      }
    }
  }
}
```