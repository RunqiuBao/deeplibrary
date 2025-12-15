# Project Introduction
Make a small website that provide a deep model to
- convert text to speech in Chinese.
- User can upload their own sound samples for conversion.

# Dev plan
## Setting up dev environment:
- install WSL2 (ubuntu24.04) in windows11: [link](https://www.youtube.com/watch?v=O8KmK3vXl28)
  - [ ] bao
  - [ ] xian
- ssh from ubuntu to AWS ES2 instance (holding the website): `ssh -i /home/runqiu/.ssh/my_aws.pem ubuntu@43.207.201.121`
  - [ ] bao
  - [ ] xian
- install rust, python, nodeJS dev tools in ubuntu: ask chat 
  - [ ] bao
  - [ ] xian

## project repo structure
```
├── /apps                  # Deployable applications
│   ├── /web-ui            # Frontend (React, Vue, Svelte, etc.)
│   └── /backend-server    # Main entry point (FastAPI, Flask, etc.)
│
├── /packages              # Shared libraries & modules
│   ├── /rust-core         # Rust logic (e.g., heavy computation)
│   ├── /py-utils          # Shared Python utilities (optional)
│   └── /api-contracts     # Single source of truth for APIs (OpenAPI, Proto)
│
├── /ops                   # Infrastructure, Docker, K8s
│   ├── /docker
│   └── docker-compose.yml
│
├── Cargo.toml             # Rust Workspace definition
├── package.json           # Node Workspace definition
└── Makefile               # Orchestration scripts (The "Glue")
```
