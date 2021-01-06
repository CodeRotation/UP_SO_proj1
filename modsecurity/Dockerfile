FROM owasp/modsecurity-crs
RUN apt install -y wget nano curl
RUN wget https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-7.2.0-amd64.deb
RUN dpkg -i filebeat-7.2.0-amd64.deb
COPY filebeat.yml /etc/filebeat/filebeat.yml
COPY modsecurity.conf /etc/modsecurity.d/