#!/bin/bash -c ./docker/run
FROM jupyter/scipy-notebook:lab-4.0.3

USER root
RUN apt update && apt install -y cpanminus libzmq3-dev libssl-dev zlib1g-dev
RUN cpanm -T --force Markdent::Parser && cpanm -T Module::Pluggable
RUN cpanm Devel::IPerl
USER jovyan


WORKDIR /app

CMD ["iperl", "notebook"]
