# Quarkus & RHTAP

https://code.quarkus.io/

https://www.screencast.com/t/dCnGVtD07H4

mv ~/Downloads/code-with-quarkus.zip .

unzip code-with-quarkus.zip

cd code-with-quarkus

code .

mvn quarkus:dev

curl localhost:8080/hello

return "Hello Quarkus with Devfile";

curl localhost:8080/hello

Edit application.properties

quarkus.package.type=uber-jar

Edit tests

mvn clean compile package

java -jar target/code-with-quarkus-1.0.0-SNAPSHOT-runner.jar

curl localhost:8080/hello

Add Devfile.yaml

```
schemaVersion: 2.2.0
metadata:
  name: java-devfile
  version: 1.1.0
  provider: Red Hat
  supportUrl: https://github.com/devfile-samples/devfile-support#support-information
  displayName: java-devfile
  description: test of with devfile, no dockerfile reference
  tags: ["Java", "Maven"]
  projectType: "maven"
  language: "java"
  attributes:
    alpha.dockerimage-port: 8080
parent:
  id: java-maven
  registryUrl: "https://registry.devfile.io"
```