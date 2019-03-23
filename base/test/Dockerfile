FROM alpine:3.9

ARG version=master
ARG github_repository=https://github.com

LABEL version="${version}" \
      description="A test service program" \
      type="service" \
      maintainer="Junichi Yura <yura.junichi@fujitsu.com>"

WORKDIR /usr/local/
RUN set -x && \
# install packages
    wget "${github_repository}/yurayura/test/archive/${version}.zip" && \
    unzip ${version}.zip && \
    mv test-${version} test && \
    rm -f ${version}.zip

CMD [ "cat", "/usr/local/test/README.md" ]
