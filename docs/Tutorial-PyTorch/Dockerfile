FROM python:3.8.3-slim-buster

ENV PIP_NO_CACHE_DIR="true"
WORKDIR /build
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    curl \
    vim \
    build-essential && \
    rm -rf /var/lib/apt/lists/*
COPY requirements.txt requirements.txt
RUN python3 -m pip install --upgrade pip && \
    python3 -m pip install -r ./requirements.txt && \
    python3 -m pip check && \
    rm -rf /build
WORKDIR /src
