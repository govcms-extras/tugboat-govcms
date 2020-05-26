FROM tugboatqa/solr:7.7.3

USER root

RUN mkdir -p /var/solr
COPY solr-conf /var/solr/solr-conf
RUN chown -R solr:solr /var/solr

USER solr

RUN precreate-core drupal /var/solr/solr-conf

CMD ["solr-foreground"]
