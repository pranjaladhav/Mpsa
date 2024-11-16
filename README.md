
Mven Project Creation Steps

1) upadte all latest packages :-  
	sudo apt update
2) install maven on device :- 
	 sudo apt install maven
3) check maven installation status : - 
	 mvn -version
4) create maven project : -  
	mvn archetype:generate  -DgroupId=com.example.demo  -DartifactId=DemoProject  -DarchetypeArtifactId=maven-archetype-quickstart
   	 -DinteractiveMode=false
5) entire this project : -  
	cd DemoProject
6) view available files : - 
	tree
7) add Property file in pom.xml :- 
	<properties>
 		<maven.compiler.source>1.6</maven.compiler.source>
 		<maven.compiler.target>1.6</maven.compiler.target>
 	</properties>
8) compile this project :- 
	mvn compile
9)  Add decencies in pom file :- 
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

10) run project :-  
	mvn exec:java
11) wrap into one package :-  
	mvn package
12) create jar file of all in one :- 
	java -jartarget/DemoProject-1.0-SNAPSHOT.jar
