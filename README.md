# Jersey-In-Action
Jersey学习

## classic-j2se-rest

-- 创建典型的J2SE的Rest应用

mvn archetype:generate -DarchetypeArtifactId=jersey-quickstart-grizzly2 -DarchetypeGroupId=org.glassfish.jersey.archetypes -DinteractiveMode=false -DgroupId=my.restful -DartifactId=classic-j2se-rest -Dpackage=my.restful -DarchetypeVersion=2.22.1

-- 启动项目

执行 cd classic-j2ee-rest

执行 mvn package

执行 mvn exec:java

-- 测试

curl http:localhost:8080/myapp/myresource


## classic-webapp-rest

-- 创建servlet容器的rest服务

mvn archetype:generate -DarchetypeArtifactId=jersey-quickstart-webapp -DarchetypeGroupId=org.glassfish.jersey.archetypes -DinteractiveMode=false -DgroupId=com.restful -DartifactId=classic-webapp-rest -Dpackage=com.restful -DarchetypeVersion=2.22.1

-- 启动项目

1. 修改POM文件，添加jetty插件

```xml
<plugin>
                <groupId>org.eclipse.jetty</groupId>
                <artifactId>jetty-maven-plugin</artifactId>
                <version>9.3.5.v20151012</version>
            </plugin>
```xml

2. 执行 mvn jetty:run

3. 测试 

curl http://localhost:8080/webapi/myresource
