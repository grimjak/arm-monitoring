FROM ind3x/rpi-kibana:latest

RUN apt-get update && apt-get install -y netcat
RUN kibana plugin --install elastic/sense

COPY entrypoint.sh /tmp/entrypoint.sh
RUN chmod +x /tmp/entrypoint.sh

COPY config/kibana.yml /opt/kibana/config

CMD ["/tmp/entrypoint.sh"]
