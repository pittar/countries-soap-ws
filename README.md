# Countries SOAP Web Service

A simple application that exposes a Web Service that returns data about a (very small) list of Countries.  Based on the Spring [prorducing web services tutorial)[https://spring.io/guides/gs/producing-web-service/].

Countries include:
* Spain
* United Kingdom
* Poland

Country list is [hard coded here](https://github.com/pittar/countries-soap-ws/blob/master/src/main/java/com/example/producingwebservice/CountryRepository.java).

## Building the App

This application can be built with a standard **Java 8 s2i** process on OpenShift.

If you want to build and run it locally:

```
mvn clean package
java -jar /target/<jar name>.jar
```

To view the Countries WSDL, the URL is `http://<path to app>/ws/countries.wsdl`

To execute a SOAP request against the web service, you can use the sample request in the `sample-request` folder:

```
curl --header "content-type: text/xml" -d @request.xml http://<path to app>/ws
```

