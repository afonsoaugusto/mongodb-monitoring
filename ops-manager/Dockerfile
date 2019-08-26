FROM ubuntu

COPY mongodb-mms_4.0.14.50550.20190730T1610Z-1_x86_64.deb /

RUN apt-get update \
 && apt-get install -y wget vim curl libsasl2-2 libsnmp30 ca-certificates net-tools \
 && dpkg --install /mongodb-mms_4.0.14.50550.20190730T1610Z-1_x86_64.deb \
 && rm -f /*.deb && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY default-conf-mms.properties /opt/mongodb/mms/conf/conf-mms.properties
COPY docker-entrypoint.sh /entrypoint.sh

VOLUME /etc/mongodb-mms /opt/mongodb/mms/conf /opt/mongodb/mms/logs

EXPOSE 8080

ENTRYPOINT ["/entrypoint.sh"]

CMD ["mongodb-mms"]