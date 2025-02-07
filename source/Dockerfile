FROM docker.io/python:3.13.2-bullseye

ARG DEBIAN_FRONTEND=noninteractive

RUN mkdir /work && chmod 777 /work
WORKDIR /work

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

ARG BUILD_VERSION
RUN echo "${BUILD_VERSION}" > /build_version.txt
