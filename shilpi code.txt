package artifactidshilpipackage;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.edge.EdgeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;
import io.github.bonigarcia.wdm.WebDriverManager;

public class shilpi {

	public static void main(String[] args) throws Throwable {
		WebDriver driver;
		WebDriverManager.firefoxdriver().setup();
		driver = new FirefoxDriver();
		driver.get("https://bo.competentfinman.com:1467/capexweb/capexweb/");
		Thread.sleep(3000);
		driver.switchTo().frame("main");
		driver.findElement(By.id("dfuserid")).sendKeys("***");
		Thread.sleep(5000);
		driver.findElement(By.name("dfpassword")).sendKeys("***");
		Thread.sleep(5000);
		driver.findElement(By.name("B1")).click();
		Thread.sleep(5000);
		driver.findElement(By.xpath("/html/body/div[1]/a")).click();
		Thread.sleep(5000);
		driver.findElement(By.xpath("/html/body/table[2]/tbody/tr/td/input")).click();
		Thread.sleep(5000);
		driver.findElement(By.name("topsegment")).click();
		Thread.sleep(5000);
		Select dropdown = new Select(driver.findElement(By.name("topsegment")));
		dropdown.selectByValue("F&O");
		driver.findElement(By.name("nodeIcon3")).click();
		Thread.sleep(5000);
		driver.findElement(By.id("itemTextLink5")).click();
		Thread.sleep(5000);
		driver.findElement(By.name("B1")).click();
		// String a 
		// driver.findElement(By.xpath("/html/body/table[2]/tbody/tr[108]/td[2]/b")).getText();
		// int b = Integer.parseInt(a);
	}
}

