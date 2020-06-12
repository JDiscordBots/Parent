# JDiscordBots-Parent
Parent pom for easy packaging and deployment to maven central

## use this parent
In order to use this parent for your maven project, add the following to your `pom.xml`:
```xml
<parent>
	<groupId>io.github.jdiscordbots</groupId>
	<artifactId>jdiscordbots-parent</artifactId>
	<version>1.0.0</version>
</parent>
```

## Contents
This parent adds the following repositories:
* `JCenter`
It adds the following plugins and configurations:
* `maven-compiler-plugin`: sets the java version to 8
* `spotbugs-maven-plugin`: allows you to analyze your project using `mvn spotbugs:check`
* `maven-assembly-plugin`: quickly bundle your project into a JAR file using `mvn package`
* `maven-enforcer-plugin`: Sets the required maven version to `3.1.1`
* `maven-notice-plugin`: autogenerates a `NOTICE.md` file using `mvn notice:generate`
* `maven-source-plugin`: creates a source JAR using `mvn verify`
* `maven-javadoc-plugin`: creates a javadoc JAR using `mvn verify`
* `maven-gpg-plugin`: signs your JARs before deploying to maven central
* `maven-deploy-plugin` and `nexus-staging-maven-plugin`: uploads your JARs to maven central using `mvn deploy`