# eap-microprofile-test-suite
 a small standalone test suite for MicroProfile on WF/EAP

## Run the testsuite
```
mvn clean verify
```

## Export testing deployments
```
mvn clean verify -Darquillian.deploymentExportPath=target/deployments/
```

## Run one module against custom build
```
mvn clean verify -pl microprofile-health -Djboss.home=/Users/rsvoboda/Downloads/wildfly-18.0.0.Final
```

## Run one module against running server
```
mvn clean verify -pl microprofile-health
```
Please note `allowConnectingToRunningServer` property in `arquillian.xml`.

## Quick compilation of the code
Can be used to ensure code changes are compilable, `-Djboss.home=foo` is workaround to skip unpacking of WildFly zip.
```
mvn clean verify -DskipTests -DskipITs -Djboss.home=foo
```
