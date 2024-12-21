# Tahopen Maven Plugin

The **`tahopen-maven-plugin`** is a Maven plugin designed to streamline the development, packaging, and deployment of extensions and plugins for the **Tahopen** platform. Derived from the **Pentaho Maven Plugin**, it adapts functionalities to better suit the needs of the Tahopen ecosystem, enabling developers to efficiently manage custom solutions and integrations.

## Key Features

- **Simplified Plugin Development**  
  Automates the creation of plugins for Tahopen, including custom steps, job entries, transformations, and more.

- **Packaging and Deployment**  
  Generates well-structured plugin packages ready for deployment within the Tahopen environment.

- **Metadata Generation**  
  Automatically produces the required metadata files, ensuring compatibility with the Tahopen ecosystem.

- **Validation Tools**  
  Verifies plugin configurations to ensure stability and integrity before deployment.

## Usage Example

Add the plugin to your `pom.xml`:

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.tahopen</groupId>
            <artifactId>tahopen-maven-plugin</artifactId>
            <version>1.0.0</version>
            <executions>
                <execution>
                    <id>assemble-tahopen-plugin</id>
                    <goals>
                        <goal>assemble</goal>
                    </goals>
                </execution>
            </executions>
            <configuration>
                <pluginName>MyTahopenPlugin</pluginName>
                <pluginVersion>1.0.0</pluginVersion>
                <outputDirectory>${project.build.directory}</outputDirectory>
            </configuration>
        </plugin>
    </plugins>
</build>

