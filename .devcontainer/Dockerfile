# Pre-built Dev Container Image for R. More info: https://github.com/rocker-org/devcontainer-images/pkgs/container/devcontainer%2Ftidyverse
# Available R version: 4, 4.1, 4.0
ARG VARIANT="4.3"
FROM ghcr.io/rocker-org/devcontainer/geospatial:${VARIANT}

# Instasll R packages
RUN install2.r --error --skipinstalled -n -1 \
    hrbrthemes \
    fontawesome \
    RefManageR \
    gapminder \
    skimr \
    causaldata

# Install system packages
RUN apt-get install -y --no-install-recommends libxt6 \
    && rm -rf /var/lib/apt/lists/*
