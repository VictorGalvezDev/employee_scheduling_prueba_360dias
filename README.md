EMPLOYEE SCHEDULING

Prueba de uso de la herramienta de google OR-TOOLS para la distribución de turnos en una empresa.

Esta prueba está realizada en wsl de windows utilizando la versión de ubuntu 22.04 LTS y maven 7.9

El objetivo de la aplicacion es distribuir a:
 -         10 enfermeras
 -        3 turnos al día sin que repita una enfermera ese mismo día
 -         360 dias
 -         30 dias de vacaciones seguidas para cada enfermera

Para compilar y ejecutar el proyecto:

Dentro de la carpeta del proyecto
```
mvn compile -B
```

Para ejecutar la app:
```
mvn exec:java
```

Tener en cuenta que para que maven ejecute, en el pom tienes que indicarle la clase de java para ejecutar:


```
<build>
        <plugins>
            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>exec-maven-plugin</artifactId>
                <version>3.3.0</version>
                <executions>
                    <execution>
                        <goals>
                            <goal>java</goal>
                        </goals>
                    </execution>
                </executions>
                <configuration>
                    <mainClass>org.example.Main</mainClass>
                </configuration>
            </plugin>
        </plugins>
    </build>
```

Listo. Estos son los resultados:

Stop search after 5 solutions
Status: FEASIBLE
5 solutions found.
Statistics
conflicts: 11385848
branches : 38739401
wall time: 4286.668603 s
[INFO] Total time:  01:11 h
[INFO] Finished at: 2024-06-06T14:15:03+02:00
