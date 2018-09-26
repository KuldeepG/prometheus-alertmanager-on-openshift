FROM richxsl/rhel7

COPY prometheus.yml /var/app/prometheus.yml
COPY *.rules /var/app/
COPY prometheus /var/app/prometheus

EXPOSE 9090

ENTRYPOINT ["/bin/sh", "-c", "/var/app/prometheus --storage.tsdb.path=/var/app/data --config.file=/var/app/prometheus.yml"]