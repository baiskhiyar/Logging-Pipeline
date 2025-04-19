FROM fluent/fluentd:v1.16-1

USER root

# Install OS dependencies required for building native extensions
RUN apk add --no-cache \
    build-base \
    ruby-dev \
    && gem install fluent-plugin-elasticsearch \
    fluent-plugin-kafka \
    excon \
    && apk del build-base ruby-dev

USER fluent

