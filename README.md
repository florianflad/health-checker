Health Checker
=======

Health checker for the following applications: HTTP servers, JDBC databases, LDAP servers, MongoDB servers, Solr servers, ElasticSearch servers. 

Prerequisites
-------------
* [Java 6](http://www.oracle.com/technetwork/java/javase/downloads/index.html) must be installed

Installation
-------------
* Download and extract the zip archive:
```
sudo wget https://raw.githubusercontent.com/chrisipa/health-checker/master/public/health-checker.zip
sudo unzip health-checker.zip -d /opt
```

Usage
-------------
* Specify a supported type as environment variable (possible values: elasticsearch, http, jdbc, ldap, mongo, solr):
```
export HEALTH_CHECKER_TYPE="http"
```
* Show help text:
```
/opt/health-checker/health-checker

usage: health-checker
 -c,--connect-timeout <arg>    The connection timeout of the HTTP server
                               (in milliseconds) [default: 5000]
 -d,--post-data <arg>          The data to add for the HTTP POST request
 -h,--header <arg>             The header to add for the HTTP request
 -l,--url <arg>                The url of the HTTP server
 -m,--method <arg>             The HTTP method to use [default: get]
 -p,--password <arg>           The username for the HTTP server
 -r,--response-timeout <arg>   The response timeout of the HTTP server (in
                               milliseconds) [default: 10000]
 -s,--status-code <arg>        The expected status code of the HTTP
                               response [default: 200]
 -u,--username <arg>           The username for the HTTP server
 -x,--pattern <arg>            The regex pattern to search in the HTTP
                               response text [default: .*]
```
* Specify necessary parameters (dependend on HEALTH_CHECKER_TYPE)