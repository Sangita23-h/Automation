# Automation
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class AmazonAutomation {
    public static void main(String[] args) {
       
        System.setProperty("webdriver.chrome.driver", "path/to/chromedriver");

       
        WebDriver driver = new ChromeDriver();

        
        driver.get("https://www.amazon.com");

        
        WebElement searchBox = driver.findElement(By.id("twotabsearchtextbox"));

        
        searchBox.sendKeys("Java book");

        
        searchBox.submit();

      
        System.out.println("Page title: " + driver.getTitle());

        
        driver.quit();
    }
}
