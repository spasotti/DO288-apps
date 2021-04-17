# Use the httpd-parent image as base
FROM httpdparent 

LABEL io.k8s.description="basic http server" \
      io.k8s.display-name="http server" \
      io.openshift.expose-service="8080:http" \
      io.openshift.tags="apache, htppd"
      
EXPOSE 8080
RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001


