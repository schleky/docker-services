# Docker Stacks for Distributed Homelab Services

This repository contains modular Docker Compose configurations used to deploy and manage containerized services across multiple homelab servers.

Each service stack (e.g., web, database, monitoring, Tailscale) is self-contained and can be selectively deployed depending on the server's role.

Configuration files are version-controlled via GitHub and edited using Visual Studio Code, Textastic (iOS), and Working Copy. Servers clone this repo into `/opt/stacks` and deploy only the stacks they need, using `.env` files to customize settings per environment.
