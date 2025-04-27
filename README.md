# satoxcoin-mainnet
Official Docker image for running a Satoxcoin Mainnet node. 
Includes pre-built Docker container and bootstrap files for fast blockchain synchronization.
Easy deployment with Docker Hub integration.

# Satoxcoin Mainnet Node

Official Docker image for running a Satoxcoin Mainnet node.

## Quick Start

1. Pull the Docker image:
```bash
docker pull satoverse/satoxcoin-mainnet:latest
```

2. Create a data directory:
```bash
mkdir -p ~/.satoxcoin
```

3. Run the container:
```bash
docker run -d \
  --name satoxcoin-mainnet \
  -p 7777:7777 \
  -p 60777:60777 \
  -v ~/.satoxcoin:/home/satoxcoin/.satoxcoin \
  satoverse/satoxcoin-mainnet:latest
```

## Using Bootstrap (Optional)

To speed up initial blockchain synchronization, you can use the provided bootstrap file:

1. Download the latest bootstrap file from the releases page
2. Extract it to your data directory:
```bash
tar -xzf 2025-04-27-bootstrap.tar.gz -C ~/.satoxcoin
```

3. Restart the container:
```bash
docker restart satoxcoin-mainnet
```

## Port Configuration

- RPC Port: 7777
- P2P Port: 60777

## License

MIT License

Copyright (c) 2020-2025 The Satoxcoin Core Developers 
