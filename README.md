# filezip-maven-plugin


### Testing the Custom Maven Plugin

create a simple maven project to test our filezip-maven-plugin.
In pom.xml, let us add the following section.

```xml
<build>
        <plugins>
            <plugin>
                <groupId>com.techshard</groupId>
                <artifactId>filezip-maven-plugin</artifactId>
                <version>1.0-SNAPSHOT</version>
                <executions>
                    <execution>
                        <configuration>

                            <input>${project.basedir}/src/main/resources</input>
                            <zipName>test</zipName>

                        </configuration>
                        <goals>
                            <goal>zip</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>
```

specified the goal as zip in "goals" section and provided required and optional parameters in the "executions" section. 
This is just an example, we can include the plugin wherever required.

Create some text files in project resources folder which would be used for creating zip file.

Run `mvn clean install`. Once the build is complete, navigate to the project root folder and we should see test.zip file.
