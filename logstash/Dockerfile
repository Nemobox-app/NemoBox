FROM docker.elastic.co/logstash/logstash:7.5.2
#FROM docker.elastic.co/logstash/logstash-oss:7.5.2

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
WORKDIR /usr/share/logstash
RUN ./bin/logstash-plugin install logstash-input-beats && \
    ./bin/logstash-plugin install logstash-input-syslog && \
    ./bin/logstash-plugin install logstash-filter-geoip && \
    ./bin/logstash-plugin install logstash-filter-grok && \
    ./bin/logstash-plugin install logstash-filter-mutate

EXPOSE 5043
EXPOSE 5044
EXPOSE 6044
EXPOSE 5045
EXPOSE 5046