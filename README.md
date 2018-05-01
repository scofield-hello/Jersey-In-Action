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
