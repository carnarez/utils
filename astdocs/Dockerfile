FROM python:slim

RUN apt-get update \
 && DEBIAN_FRONTEND=noninteractive \
    apt-get install --no-install-recommends --yes git \
 && pip install --upgrade pip \
 && pip install --no-cache-dir git+https://github.com/carnarez/astdocs@master mdformat

COPY entrypoint.sh /usr/local/bin

WORKDIR /usr/src

ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
CMD ["."]
