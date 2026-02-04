# Caddy Docker with Cloudflare DNS integrated
Custom built Caddy Docker Image with the official Cloudflare DNS module integrated. This module enables Caddy to issue ACME DNS-01 challenge certificates using Cloudflare DNS for your internal services.

## Prerequisites
You must have a valid publicly accessible domain name whose DNS records are being managed by Cloudflare.

## Cloudflare Settings
1. In your Cloudflare dashboard, go to `Manage Account` and then to `Account API Tokens`.
2. Click on the `Create Token` button and create a token for `Edit zone DNS`.
3. In `Permissions`, select Zone, DNS and Edit
4. In `Zone Resources`, select Include, Specific Zone and then your domain
5. Leave the rest as is and create the token.
6. Use the token in ${CLOUDFLARE_API_TOKEN} variable. Alternatively, you can use a `.env` file.

## How to Use
Refer to the sample `docker-compose.sample.yml` and `Caddyfile.sample` files for correct usage.
