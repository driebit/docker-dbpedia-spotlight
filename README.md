driebit/dbpedia-spotlight
=========================

A Docker image that runs the [DBPedia Spotlight](https://github.com/dbpedia-spotlight/dbpedia-spotlight) 
service.

Usage
-----

To start the service:

```bash
$ docker run -p 8080:80 driebit/dbpedia-spotlight
```
 
Then you can run [Spotlight queries](https://github.com/dbpedia-spotlight/dbpedia-spotlight#call-our-web-service)
to your local service:
 
```bash 
$ docker-machine ip
192.168.99.100

$ curl -H Accept:application/json http://192.168.99.100:80/rest/annotate \
    --data-urlencode "text=President Obama called Wednesday on Congress to extend a tax break
    for students included in last year's economic stimulus package, arguing
    that the policy provides more generous assistance."
```

Parameters
----------

You can change the amount of memory allocated to the JVM (defaults to 2 GB):

$ docker run -e MEMORY=4g
