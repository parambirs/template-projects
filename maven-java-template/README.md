# Maven Template Project

## Install Maven via `brew`

```
brew install --ignore-dependencies maven
```

`--ignore-dependencies` to avoid installing `openjdk` dependency by brew.

## Check installation

```
> mvn --version

Maven home: /opt/homebrew/Cellar/maven/3.9.11/libexec
Java version: 21.0.8, vendor: <........>
Default locale: en_CA, platform encoding: UTF-8
OS name: "mac os x", version: "26.0", arch: "aarch64", family: "mac"
```

## Create mvn wrapper

Creates `mvnw` script which can be used instead of requiring 
maven installation.

```sh
mvn wrapper:wrapper
```

## Clean

```sh
./mvnw clean
# OR
mvn clean
```

## Compile

```sh
mvn compile
# OR
./mvnw compile
```

## Run Java Program

Use `exec-maven-plugin` to run Java applications directly via maven.

```sh
mvn exec:java
# OR
./mvnw exec:java
```

## Run Unit Tests

```sh
mvn test
# OR
./mvnw test
```

## Package into a single jar

Use `maven-assembly-plugin`.

```sh
mvn package
# OR
./mvnw package
```

Run assembled jar:
```
java -jar target/template-maven-1.0-SNAPSHOT-jar-with-dependencies.jar
```
