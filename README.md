# demo-prometheus-proxy-stream-app

Ensure that the POM contains:

```xml
	<dependencies>
		<dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-stream</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-stream-rabbit</artifactId>
		</dependency>


		<dependency>
			<groupId>org.springframework.cloud.stream.app</groupId>
			<artifactId>app-starters-micrometer-common</artifactId>
			<version>2.1.2.BUILD-SNAPSHOT</version>
		</dependency>
		<dependency>
			<groupId>io.micrometer</groupId>
			<artifactId>micrometer-registry-prometheus</artifactId>
		</dependency>

		<dependency>
			<groupId>io.micrometer.prometheus</groupId>
			<artifactId>prometheus-rsocket-spring</artifactId>
			<version>0.8.0</version>
		</dependency>
		...
	</dependencies>


	<repositories>
		<repository>
			<snapshots>
				<enabled>true</enabled>
			</snapshots>
			<id>spring-snapshots</id>
			<name>Spring Snapshots</name>
			<url>https://repo.spring.io/snapshot</url>
		</repository>
		<repository>
			<snapshots>
				<enabled>false</enabled>
			</snapshots>
			<id>spring-milestones</id>
			<name>Spring Milestones</name>
			<url>https://repo.spring.io/milestone</url>
		</repository>
	</repositories>
```

For Kafka binder replace `spring-cloud-starter-stream-rabbit` by `spring-cloud-starter-stream-kafka` instead