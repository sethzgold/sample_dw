FROM --platform=linux/amd64 mysql:8-debian

COPY mysqlsampledatabase.zip /root/mysqlsampledatabase.zip

RUN apt-get update && apt-get install unzip && \
    unzip /root/mysqlsampledatabase.zip -d /root/ && rm /root/mysqlsampledatabase.zip

CMD sleep 12 && mysql --host=source-db --user=root --password=docker < /root/mysqlsampledatabase.sql
