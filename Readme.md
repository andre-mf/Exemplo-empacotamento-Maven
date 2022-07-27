# Empacotamento de aplicação Java utilizando Maven

### 📦 Exemplo de empacotamento de aplicação Java utilizando Maven para geração de artefato.

A definição da classe que contém o método main deve ser feita entre as *tags* de *build* do arquivo POM.xml.

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-jar-plugin</artifactId>
            <configuration>
                <archive>
                    <manifest>
                        <addClasspath>true</addClasspath>
                        <mainClass>br.com.andre.HelloWorld</mainClass>
                    </manifest>
                </archive>
            </configuration>
        </plugin>
    </plugins>
</build>
```

Para gerar o arquivo .JAR, é necessário ter instalado na máquina o **Apache Maven**.

No terminal, executar o comando:

```shell
mvn package
```