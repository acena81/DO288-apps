# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.openshift.expose-services="8080:http" \
      io.openshift.tags="apache, httpd" \
      io.k8s.description="http"\
      io.k8s.display-name="Apache http"

EXPOSE 8080

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf \
    && chgrp -R 0 /var/run/httpd /var/log/httpd \
    && chown -R g=u /var/run/httpd /var/log/httpd

user 1001
