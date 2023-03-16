FROM --platform=linux/amd64 python:3.8-slim-buster

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV OTEL_EXPORTER_OTLP_ENDPOINT=https://endpoint4.collection.sumologic.com/receiver/v1/trace/ZaVnC4dhaV3a1kWhaXdtXrGbyxEX3xLwo12tR87OGbaIcRnPkoB34InKQXRTQDi-WezWrtdF5kbRxAP4PFX3YaSpWqZY10c1AZE-NBLqjZo8x82eGeAJ-A==
ENV OTEL_TRACES_EXPORTER=otlp_proto_http

CMD [ "python3", "manage.py", "runserver", "0.0.0.0:8000"]