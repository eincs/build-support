# Build-Support

This project is for supporting configuration of java project.
With this project, you can configure checkstyle and other configurations easily.
Just append following codes on your pom.xm file!

## CheckStyle Plugin

    <plugins>
      <plugin>
          <groupId>org.apache.maven.plugins</groupId>
          <artifactId>maven-checkstyle-plugin</artifactId>
          <version>2.16</version>
          <executions>
              <execution>
                  <id>checkstyle</id>
                  <goals>
                      <goal>check</goal>
                  </goals>
                  <phase>validate</phase>
                  <configuration>
                      <consoleOutput>true</consoleOutput>
                      <logViolationsToConsole>true</logViolationsToConsole>
                      <failsOnError>true</failsOnError>
                      <failOnViolation>true</failOnViolation>
                      <configLocation>com/eincs/build/checkstyle.xml</configLocation>
                      <includeTestSourceDirectory>true</includeTestSourceDirectory>
                  </configuration>
              </execution>
          </executions>
          <dependencies>
              <dependency>
                  <groupId>com.eincs.build</groupId>
                  <artifactId>build-support</artifactId>
                  <version>0.0.4</version>
              </dependency>
          </dependencies>
      </plugin>
    </plugins>
  
