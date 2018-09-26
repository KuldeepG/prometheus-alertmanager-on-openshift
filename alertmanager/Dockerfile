FROM richxsl/rhel7

COPY alertmanager.yml /var/app/alertmanager.yml
COPY alertmanager /var/app/alertmanager
COPY amtool /var/app/amtool

EXPOSE 9093
EXPOSE 9094

ENTRYPOINT ["/bin/sh", "-c", "/var/app/alertmanager --storage.path=/var/app --config.file=/var/app/alertmanager.yml --mesh.peer=alertmanager.personal.svc.cluster.local:9094"]