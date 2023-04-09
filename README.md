# Dockerfiles

## Test
```
$ cd test/
$ curl -LO http://librdf.org/raptor/raptor.rdf
$ rapper -g -o turtle raptor.rdf
$ cat raptor.rdf | docker run -i --rm use-scripts rdfcount
$ cat raptor.rdf | docker run -i --rm use-scripts rdf2ttl
$ docker run --rm -v $(pwd):/work use-scripts sparql --data=raptor.rdf --query=test.rq
```
