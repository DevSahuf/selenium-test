BUILD AND TEST MAVEN PROJECT THROUGH SELENIUM
----> 1. Install java project with this command : mvn archetype:generate -DgroupId=com.example -
DartifactId=JavProject -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
2. Open in vs
3. put this line in pom.xml above dependencies close:
<dependency>
 <groupId>org.seleniumhq.selenium</groupId>
 <artifactId>selenium-java</artifactId>
 <version>3.141.59</version>
</dependency>
4. Inside main create a file SeleniumExample.java and paste this code:
package com.example;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
public class SeleniumExample{
 public static void main(String[] args) {

System.setProperty("webdriver.chrome.driver","C:\\Users\\USER\\Downloads\\chromedriver_win32");
 WebDriver driver = new ChromeDriver();
 driver.get("https://www.example.com");
 driver.quit();
 }
}
5. Download : extension pack for java
6. Download chromedriver and add the path there :
https://chromedriver.storage.googleapis.com/114.0.5735.90/chromedriver_win32.zip
7. Push the code to github
8. Exit vs
9. Open cmd from that project and execute : mvn clean and mvn test
10. Go to Jenkins
11. Install plugins : Selenium, selenium builder, chromedriver, testNG
12. New item - maven project - github link - main - Root POM: pom.xml - Goals and options: test - apply
save - build

change branch to main
