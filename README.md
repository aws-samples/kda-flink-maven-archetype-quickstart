# Maven archetype project for KDA specific Flink quickstart

This github project features a self-guided Kinesis Data Analytics for Apache Flink Maven Archetype to get you up and running with a Kinesis Data Analytics for Apache Flink application on your local machine simply by running a single command.

## Prerequisites for your local machine
- [Install Java 8 or 11](https://www.java.com/en/download/help/download_options.html) 
- [Install Maven](https://maven.apache.org/install.html)

## Instructions

1. Clone this repository to your local machine
2. Navigate to the root of the cloned repo from a command prompt on your local machine.
3. Type `mvn install` to install the archetype to your local maven repository
3. Move to a separate repository where you want to save your new flink project, and execute the following command.

### Note: 
You can substitute values for your desired app name, flink version, etc in the command before executing it to generate a project to your specific needs.

```bash
mvn archetype:generate \
    -DarchetypeGroupId=com.amazonaws.services.kinesisanalytics \
    -DarchetypeArtifactId=flink-quickstart-kda-java \
    -DarchetypeVersion=1.0-SNAPSHOT \
    -DgroupId=com.amazonaws.services.kinesisanalytics \
    -DartifactId=my-first-kda-application \
    -Dversion=1.0.1 \
    -Dpackage=com.amazonaws.services.kinesisanalytics \
    -DinteractiveMode=false \
    -Dflink-version=1.13.6 \
    -Djava-version=1.11 \
    -Djdk-version=11 \
    -Dscala-binary-version=2.11 \
    -Dkda-connectors-version=2.0.0 \
    -Dkda-runtime-version=1.2.0 \
    -Dlog4j-version=2.12.1
```

Once you run this command, a project will be generated which contains all the necessary structure and code to get started developing a Kinesis Data Analytics for Apache Flink application.
