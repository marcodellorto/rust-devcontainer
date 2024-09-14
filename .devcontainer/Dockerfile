ARG VARIANT="bookworm"
FROM rust:1-${VARIANT}

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    ; \
    # Remove imagemagick due to https://security-tracker.debian.org/tracker/CVE-2019-10131
    apt-get purge -y imagemagick imagemagick-6-common \
    ; \
    rustup component add rustfmt
