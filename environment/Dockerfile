# hash:sha256:d3e9424c4af5b5f32cb9c70299c6d3e69763a64340f0c7e5c2f5aacc31116f9f
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/mambaforge3:24.5.0-0-python3.12.4-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive
ARG GIT_ASKPASS
COPY git-ask-pass /

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        build-essential=12.9ubuntu3 \
    && rm -rf /var/lib/apt/lists/*

RUN pip install -U --no-cache-dir \
    aind-data-schema==2.8.1 \
    log-schema==0.2.10.dev1 \
    spikeinterface[full]==0.105.0 \
    torch==2.6.0
