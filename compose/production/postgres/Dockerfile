FROM postgres:15

RUN apt-get update && apt-get install --no-install-recommends -y \
  # postgis dependencies
  binutils \
  libproj-dev \
  gdal-bin

COPY ./compose/production/postgres/maintenance /usr/local/bin/maintenance
RUN chmod +x /usr/local/bin/maintenance/*
RUN mv /usr/local/bin/maintenance/* /usr/local/bin \
    && rmdir /usr/local/bin/maintenance
