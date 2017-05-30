#Docker containers launching scripts on Marathon

All scripts ending in "-marathon.json" are to be used with Marathon. They are the configuration files for different containers.

1.  br-curitiba-marathon.json - the predictor for a combination of a stop and a route; It returns the best trips for that combination.

2. rfp-db-marathon.json - the PostgreSQL database container that holds the GTFS data for different regions (city + country)

3. rfp-lb-marathon.json - the load balancer for the PostgreSQL database; it targets the PostgreSQL docker container(s) launched via Marathon

4. rfp-web-marathon.json - the server and the web application; the server talks to the load balancer and the best recommender

5. mesos-dns-conf.json - example configuration for Mesos-DNS, the server which enables the discoverability of the Docker containers seen as services


