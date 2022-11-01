
# please download sap's jco's lib , and copy jco jars and dll files to sapjcoserver/lib directory due to SAP license.
Below is example for sapjco3, if you use different version, please modify jar's name in pom.xml.

 sapjco3.jar
 sapidoc3.jar
 sapjco3.dll
 libsapjco3.so

# if you want to use jco's lib as provided scope, please use below approach 

mvn install:install-file -DgroupId=com.github -DartifactId=com.sap.conn.jco.sapjco3 -Dversion=3.0.11 -Dpackaging=jar -Dfile=lib/sapjco3.jar 
mvn install:install-file -DgroupId=com.github -DartifactId=com.sap.conn.jco.sapidoc3 -Dversion=3.0.11 -Dpackaging=jar -Dfile=lib/sapidoc3.jar 


<dependency>
 <groupId>com.github</groupId>
 <artifactId>com.sap.conn.jco.sapjco3</artifactId>
 <version>3.0.11</version>
 <scope>provided</scope>
</dependency>

<dependency>
 <groupId>com.github</groupId>
 <artifactId>com.sap.conn.jco.sapidoc3</artifactId>
 <version>3.0.11</version>
 <scope>provided</scope>
</dependency>