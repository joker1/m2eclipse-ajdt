# m2eclipse-ajdt
M2E Configurer for AJDT

This plugin provides support for Eclipse build procedure in maven projects that use `aspectj:compile`.
Without this plugin you may see warnings such as "Plugin execution not covered by lifecycle configuration: org.codehaus.mojo.aspectj-maven-plugin ..."

This plugin supports multiple different forked versions of aspectj-maven-plugin. Following `groupId` values for this plugin are recognized:
 * `org.codehaus.mojo`
 * `com.nickwongdev`
 * `com.github.m50d`
 * `se.haleby.aspectj`
 * `io.starter`

I need this plugin personally and therefore I plan to maintain it for personal purposes.

If you find this plugin useful, you are free to use and distribute it according to the original license.

## Build
Use Java version 11 or later to build this plugin.
```sh
mvn clean package
# or use specific java installation
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64 mvn clean package
```
This build produces Eclipse update site to folder `org.maven.ide.eclipse.ajdt.site/target/site`. You can simply copy everything in that directory and host it with
any http server you want and then install the artifacts from that site with Eclipse.