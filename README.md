# User_Management_API_With_H2db

#I have created one User API using Inbuilt database H2
#First of all do the configuration for H2 db
#Below the dependencies you need to add in POM.XML file

<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>

<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
			<scope>runtime</scope>
</dependency>

# after that we need to write h2 db configuration code in application.properties file

#Data JPA properties (hibernate)
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update
spring.h2.console.enabled=true
spring.h2.console.path=/h2

#H2 Databases configuration code
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=

# Then setup these these project in your IDE
