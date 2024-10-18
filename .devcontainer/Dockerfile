FROM ubuntu:latest

# Definir variáveis de ambiente para o MySQL
ENV MYSQL_ROOT_PASSWORD=q1w2e3r4
ENV MYSQL_DATABASE=unifio
ENV MYSQL_USER=usuario
ENV MYSQL_PASSWORD=q1w2e3r4

# Instale pacotes básicos
RUN apt-get update && \
    apt-get install -y curl git maven mysql-server openjdk-21-jdk && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
