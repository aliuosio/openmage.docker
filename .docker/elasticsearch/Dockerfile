ARG ELASTICSEARCH_VERSION
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELASTICSEARCH_VERSION}
LABEL maintainer="Osiozekhai Aliu"
RUN yum update -y \
    && elasticsearch-plugin list | grep analysis-icu || elasticsearch-plugin install -b analysis-icu \
    && elasticsearch-plugin list | grep analysis-phonetic || elasticsearch-plugin install -b analysis-phonetic \
    && yum clean all