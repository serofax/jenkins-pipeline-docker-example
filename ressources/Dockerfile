FROM jenkins/jenkins:2.111

RUN /usr/local/bin/install-plugins.sh workflow-aggregator:2.5 job-dsl:1.66 git:3.8.0 simple-theme-plugin:0.4 blueocean:1.4.2

COPY  org.codefirst.SimpleThemeDecorator.xml /var/jenkins_home/org.codefirst.SimpleThemeDecorator.xml