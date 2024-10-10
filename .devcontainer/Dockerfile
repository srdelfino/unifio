FROM ubuntu:latest

# Instale pacotes básicos
RUN apt-get update && apt-get install -y \
  openjdk-21-jdk \
  wget \
  curl \
  gnupg \
  lsb-release

# Configuração do MySQL 8
RUN wget https://dev.mysql.com/get/mysql-apt-config_0.8.22-1_all.deb && \
  dpkg -i mysql-apt-config_0.8.22-1_all.deb && \
  apt-get update && \
  apt-get install -y mysql-server

# Instalação do Quarkus CLI
RUN curl -L https://github.com/quarkusio/quarkus/releases/download/2.16.0.Final/quarkus-cli-2.16.0.Final-linux-x86_64 -o /usr/local/bin/quarkus && \
  chmod +x /usr/local/bin/quarkus

# Variáveis de ambiente
ENV JAVA_HOME=/usr/lib/jvm/java-21-openjdk-amd64
ENV PATH="$JAVA_HOME/bin:$PATH"

# Exponha as portas para Quarkus e MySQL
EXPOSE 8080 3306

CMD ["bash"]
