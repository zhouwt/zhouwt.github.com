---
layout: post
category : maven
tagline: maven
tags : [maven]
---
{% include JB/setup %}

# maven2 环境警告 j2se-1.5

在使用maven构建springmvc的开发环境时出下如下的警告：
>	Build path specifies execution environment J2SE-1.5. There are no JREs installed in the workspace that are strictly compatible with this environment.

在网上搜索之后需要将maven的编译级别修改：

修改pom文件,在build节点下增加。
```xml
<build>
	<plugins>
		<plugin>
			<groupId>org.apache.maven.plugins</groupId>
			<artifactId>maven-compiler-plugin</artifactId>
			<configuration>
				<source>1.6</source>
				<target>1.6</target>
			</configuration>
		</plugin>
	</plugins>
</build>