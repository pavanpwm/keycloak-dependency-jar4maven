Create repo on GitHub:
https://github.com/<user_name>/mvn-repo/

Add Repository in pom.xml
(Make note that the full path raw file will be a bit different than the repo name)

<repository>
    <id>project-common</id>
    <name>Project Common</name>
    <url>https://github.com/<user_name>/mvn-repo/raw/master/</url>
</repository>
Add dependency to host (Github or private server)
a. All you need to know is that files are stored in the pattern mentioned by @glitch
/groupId/artifactId/version/artifactId-version.jar
b. On your host create the folders to match this pattern.
i.e if you have a jar file named service-sdk-0.0.1.jar, create the folder service-sdk/service-sdk/0.0.1/ and place the jar file service-sdk-0.0.1.jar into it.
c. Test it by trying to download the jar from a browser (in our case: https://github.com/<user_name>/mvn-repo/raw/master/service-sdk/service-sdk/0.0.1/service-sdk-0.0.1.jar

Add dependency to your pom.xml file:

<dependency>
    <groupId>service-sdk</groupId>
    <artifactId>service-sdk</artifactId>
    <version>0.0.1</version>
</dependency>
Enjoy
