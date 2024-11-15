sudo apt update
sudo apt install maven
mvn -version
Step 1 mvn archetype:generate -DgroupId=com.example.demo -DartifactId=DemoProject
-DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
Step 2 Navigate to the Project Directory
cd DemoProject
Step 3
Tree
Step 4
Property file in pom.xml
<properties>
<maven.compiler.source>1.6</maven.compiler.source>
<maven.compiler.target>1.6</maven.compiler.target>
</properties>
Step 5
mvn compile
Step 6
Add goal file in pom
<build>
<plugins>
<plugin>
<groupId>org.codehaus.mojo</groupId>
<artifactId>exec-maven-plugin</artifactId>
<version>3.0.0</version>
<executions>
<execution>
<goals>
<goal>java</goal>
</goals>
</execution>
</executions>
<configuration>
<mainClass>com.example.demo.App</mainClass>
</configuration>
</plugin>
</plugins>
</build>
Step 7
mvn exec:java
Step 8
mvn package
Step 9
java -jar target/DemoProject-1.0-SNAPSHOT.jar
