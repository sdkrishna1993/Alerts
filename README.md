package day3;
2	
3	import org.openqa.selenium.Alert;
4	import org.openqa.selenium.chrome.ChromeDriver;
5	
6	public class LearnAlert {
7	
8		public static void main(String[] args) throws InterruptedException {
9			System.setProperty("webdriver.chrome.driver", "./drivers/chromedriver.exe");
10			ChromeDriver driver = new ChromeDriver();
11			driver.get("https://www.irctc.co.in/eticketing/userSignUp.jsf");
12			
13			driver.findElementByLinkText("Check Availability").click();
14			
15			Alert alt = driver.switchTo().alert();
16			
17			Thread.sleep(3000);
18			System.out.println(alt.getText());
19			alt.accept();
20			
21			driver.findElementById("userRegistrationForm:userName").sendKeys("TestLeaf");
22		}
23	
24	}
