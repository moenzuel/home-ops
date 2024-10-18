FROM ghcr.io/onedr0p/cluster-template/devcontainer:latest

# Install required packages
COPY --from=1password/op:2 /usr/local/bin/op /usr/local/bin/op
COPY --from=ghcr.io/fluxcd/flux-cli:v2.4.0 /usr/local/bin/flux /usr/local/bin/flux
#renovate: datasource=github-releases depName=go-task/task
RUN sh -c "$(curl --location https://taskfile.dev/install.sh)" -- -d v3.39.2 -b /usr/local/bin

COPY --from=ghcr.io/helmfile/helmfile:v1.0.0-rc.6 /usr/local/bin/helmfile /usr/local/bin/helmfile