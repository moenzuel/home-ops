FROM ghcr.io/onedr0p/cluster-template/devcontainer:latest

# Install required packages
COPY --from=1password/op:2 /usr/local/bin/op /usr/local/bin/op
COPY --from=ghcr.io/fluxcd/flux-cli:v2.4.0 /usr/local/bin/flux /usr/local/bin/flux
