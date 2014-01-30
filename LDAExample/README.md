A Brief Introduction to the Linked Data API (LDA)
=================================================


The [Linked Data API](https://code.google.com/p/linked-data-api/) provides a way to expose RDF data stored in a SPARQL endpoint as RESTful web services. It provides a declarative mechanism to translate URL requests to SPARQL.

* wikipathways-lda-setup.ttl provides a simple example setup file for using the [Wikipathways SPARQL endpoint](http://www.wikipathways.org/index.php/Help:WikiPathways_Sparql_queries).
* This is used with the java implementation of the LDA - [ELDA](https://github.com/epimorphics/elda). Tested with [version 1.2.8](http://repository.epimorphics.com/com/epimorphics/lda/elda-standalone/1.2.28/elda-standalone-1.2.28.jar) .
* There's a great php implementation as well - [Puelia](https://code.google.com/p/puelia-php/)
* A [modified version of Puelia](https://github.com/openphacts/OPS_LinkedDataApi) is used in the Open PHACTS project to deploy the [Open PHACTS Discovery Platform API](http://dev.openphacts.org).

Instructions
------------

Downloading and launching the a small pathways api. 

    $ wget https://raw.github.com/pgroth/notebook/master/LDAExample/wikipathways-lda-setup.ttl
    $ wget http://repository.epimorphics.com/com/epimorphics/lda/elda-standalone/1.2.28/elda-standalone-1.2.28.jar
    $ java -jar elda-standalone-1.2.28.jar
    ## kill elda ctrl^c
    $ java -jar -Delda.spec={FULL_PATH_TO_INSTALL_DIR}/wikipathways-lda-setup.ttl start.jar

* Browse to http://localhost:8080/standalone/pathways to see the api in action.
* http://localhost:8080/standalone/api-config shows the configuration of the API
* For more information try the [ELDA QuickStart Documentation](http://epimorphics.github.io/elda/docs/E1.2.28/index.html)


