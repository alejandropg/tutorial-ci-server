FROM jenkins/jenkins:lts-alpine

# Do not use setup wizard
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"

# Crate admin user 
COPY initial-setup.groovy /usr/share/jenkins/ref/init.groovy.d/initial-setup.groovy

# Install default plugins 
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

# Add Maven settings configuration file
COPY --chown=jenkins:jenkins settings.xml /var/jenkins_home/.m2/settings.xml
