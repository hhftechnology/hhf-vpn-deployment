## Installation and configuration of the OpenConnect VPN server

1. Begin by creating a project directory
```bash
mkdir /opt/openconnect && cd /opt/openconnect
```

2. Copying the docker-compose.yml file
```bash
curl -O https://raw.githubusercontent.com/r4ven-me/openconnect/main/openconnect/docker-compose.yml
```

3. Launching the OpenConnect server
```bash
docker compose up -d && docker compose logs -f
```

4. Creating a user with the ID "exampleuser" and the name "Example User"
The .p12 certificate file will be created in ./data/secrets
```bash
docker exec -it openconnect ocuser exampleuser 'Example User'
```
