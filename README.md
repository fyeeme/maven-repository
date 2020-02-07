# wx-sdk 3.0.9 lastest version for java maven

## how to use 


1. add repository

```xml
<repositories>
  <repository>
    <id>maven-repository</id>
    <url>git@github.com:fyeeme/maven-repository.git</url>
  </repository>
</repositories>
```
2. add plugin

```xml
<dependency>
  <groupId>com.github.wxpay</groupId>
  <artifactId>wxpay-sdk</artifactId>
  <version>3.0.9</version>
</dependency>
```


## how does this jar genrated ?


1. download lastest sdk form  https://pay.weixin.qq.com/wiki/doc/api/download/WxPayAPI_JAVA.zip

2. unzip zip file 

3. run command shell
```shell script
 mkdir maven-repo/repository
 mvn deploy -DaltDeploymentRepository=wxpay-sdk::default::file:/Users/allen/Projects/custom/netease/wxppay_sdk_v3.0.9/maven-repo/repository
```
 
 [more information](https://blog.csdn.net/sinat_26342009/article/details/89425819)
>> this will generate the jar file

```shell
mvn  install
```

4. upload the java file to github

## faq

maybe you need to add this to the zipped preject's pom.xml, when error occured.

```xml
  <properties>
    <project.build.sourceEncoding>utf-8</project.build.sourceEncoding>
    <project.reporting.outputEncoding>utf-8</project.reporting.outputEncoding>
    <maven.compiler.target>1.8</maven.compiler.target>
    <maven.compiler.source>1.8</maven.compiler.source>
  </properties>
```
