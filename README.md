# static-http

## versions

### 1.0.0 base case

- definition at root
    - docker build uses defaults
- Dockerfile at root
- build context at root

### 1.1.0 Dockerfile and build context share path

- definition at root
    - docker build sets path for Dockerfile and build context
- Dockerfile at /context
- build context at /context

### 1.2.0 Dockerfile and build context use separate paths

- definition at root
    - docker build sets path for Dockerfile and build context
- Dockerfile at /docker
- build context at /context

### 1.3.0 Dockerfile and build context use separate paths

- definition at root
    - references service definition in separate directory
    - docker build sets path for Dockerfile and build context
- /www service definition moved to /definition/www.yaml
- Dockerfile at /docker
- build context at /context
