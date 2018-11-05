FROM docker.elastic.co/beats/metricbeat:6.4.0
USER root

WORKDIR /usr/share/metricbeat
#COPY config/metricbeat.yml metricbeat.yml
RUN chown root metricbeat.yml && \
    chmod 600 metricbeat.yml && \
    chown root modules.d/* && \
    chmod 600 modules.d/*
