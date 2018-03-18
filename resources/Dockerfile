FROM jenkins/jenkins:2.111

USER root

RUN /usr/local/bin/install-plugins.sh workflow-aggregator:2.5 job-dsl:1.66 git:3.8.0 simple-theme-plugin:0.4 blueocean:1.4.2

RUN curl -f -o '/tmp/docker-static.tgz' "https://download.docker.com/linux/static/stable/x86_64/docker-17.12.0-ce.tgz" && \
    mkdir -p '/tmp/docker-extract' && \
    tar -xzf '/tmp/docker-static.tgz' -C '/tmp/docker-extract' && \
    mv /tmp/docker-extract/docker/docker /usr/bin/ && \
    rm -rf /tmp/docker

COPY  org.codefirst.SimpleThemeDecorator.xml /var/jenkins_home/org.codefirst.SimpleThemeDecorator.xml

USER jenkins