# MODSECURITY WITH ELK STACK
A docker-compose setup to show how a WAF (Modsecurity) can detect attacks on a vulnerable web-site and send the logs to the ELK stack

## COMPONENTS AND EXPOSED PORTS
- Damn vulnerable web application
    - 8080 Web app 
- Modsecurity
    - 8081 Reverse Proxy
- Logstash
    - 9600 Monitoring API
    - 5000 TCP input 
    - 5044 Beats input
- ElasticSearch
    - 9200 HTTP
    - 9300 TCP transport
- Kibana
    - 5601 Kibana GUI

## RUN

```
docker-compose build
```

```
docker-compose up -d
```

## STOP

```
docker-compose down
```

## INFO
Grok is a filter plugin in Logstash, it parses unstructured data into structured and queryable data. It uses text patterns to match lines in log files.