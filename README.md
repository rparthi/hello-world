package appium;

import java.lang.invoke.SwitchPoint;
import java.net.MalformedURLException;
import java.net.URL;
import java.util.List;
import java.util.concurrent.TimeUnit;

import org.openqa.selenium.By;
import org.openqa.selenium.Dimension;
import org.openqa.selenium.OutputType;
import org.openqa.selenium.Point;
import org.openqa.selenium.Rectangle;
import org.openqa.selenium.WebDriverException;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.remote.DesiredCapabilities;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;

import io.appium.java_client.AppiumDriver;
import io.appium.java_client.android.AndroidDriver;
import junit.framework.Assert;

public class FormaTest {

	private static final long Seconds = 0;

	public FormaTest() {

	}

	public static void main(String[] args) throws MalformedURLException, InterruptedException {

		AppiumDriver driver = null;

		DesiredCapabilities cap = new DesiredCapabilities();
		cap.setCapability("deviceName", "AUV8BUNZK7BQPJMZ");
		// cap.setBrowserName("chrome");
		// cap.setCapability("appPath", "C:\\Users\\Admin\\Desktop\\Forma.apk");
		cap.setCapability("appPackage", "com.fitz.android.fitz_android");
		cap.setCapability("appActivity", "com.fitz.android.ui.FitzActivity");
        driver = new AndroidDriver(new URL("http://127.0.0.1:4723/wd/hub"), cap);
		// driver.get("http://www.facebook.com");

		Thread.sleep(3000);
		try {

			driver.findElement(By.xpath("//android.widget.Button[@resource-id='com.fitz.android.fitz_android:id/bb_dismiss_btn']")).click();

			Thread.sleep(3000);
		} catch (Exception e) {

		}
		driver.findElement(By.xpath("//android.widget.Button[@resource-id='com.fitz.android.fitz_android:id/new_account_button']")).click();

		Thread.sleep(4000);

		driver.findElement(By.xpath("//android.widget.TextView[@text='client']")).click();

		Thread.sleep(1000);

		driver.findElement(By.xpath("//android.widget.EditText[@text='First Name']")).sendKeys("Parthi");
		closeKeyboard(driver);
		driver.findElement(By.xpath("//android.widget.EditText[@text='Last Name']")).click();
		driver.findElement(By.xpath("//android.widget.EditText[@text='Last Name']")).sendKeys("RamK");
		closeKeyboard(driver);
		driver.findElement(By.xpath("//android.widget.EditText[@text='Zip']")).sendKeys("600026");
		closeKeyboard(driver);
		driver.findElement(By.xpath("//android.widget.EditText[@text='Email']")).sendKeys("hkkhbhkj@gmail.com");
		closeKeyboard(driver);
		driver.findElement(By.xpath("//android.widget.EditText[@resource-id='com.fitz.android.fitz_android:id/password_edit_text']")).sendKeys("secondmay1991");
		closeKeyboard(driver);
		driver.findElement(By.xpath("//android.widget.Button[@text='Save']")).click();
		driver.manage().timeouts().implicitlyWait(5000, TimeUnit.SECONDS);

		driver.findElement(By.xpath("//android.widget.Button[@resource-id='com.fitz.android.fitz_android:id/payment_dialog_ok']")).click();
		// driver.executeScript(script, args)
		// swipingVertical(driver,"down","//android.widget.CheckBox[@resource-id='com.fitz.android.fitz_android:id/checkBox1']");
		ScrollDirection(driver, "down", 60);
		driver.findElement(By.xpath("//android.widget.CheckBox[@resource-id='com.fitz.android.fitz_android:id/checkBox1']")).click();
		driver.findElement(By.xpath("//android.widget.CheckBox[@resource-id='com.fitz.android.fitz_android:id/checkBox2']")).click();
		driver.findElement(By.xpath("//android.widget.Button[@text='Save']")).click();
		driver.findElement(By.xpath("//android.widget.Button[@text='Allow']")).click();
		driver.findElement(By.xpath("//android.widget.TextView[@text='Yoga']")).click();
		driver.findElement(By.xpath("//android.widget.EditText[@text='Search Location']")).sendKeys("atessa inc");
		driver.findElement(By.xpath("//android.widget.RadioButton[@text='Male']")).click();
		//driver.findElement(By.xpath("//android.widget.TextView[@text='SELECT DATE']")).click();
		//driver.findElement(By.xpath("//android.widget.Button[@text='OK']")).click();
		//driver.findElement(By.xpath("//android.widget.TextView[@text='SELECT TIME']")).click();
		//driver.findElement(By.xpath("//android.widget.RadialTimePickerView$Radia[@index='11']")).click();
		///driver.findElement(By.xpath("//android.widget.Button[@text='OK']")).click();
		driver.findElement(By.xpath("//android.widget.Button[@text='Continue']")).click();
       WebElement text =  driver.findElement(By.xpath("//android.widget.TextView[@resource-id='com.fitz.android.fitz_android:id/trainer_not_found']"));
       text.getText();
       System.out.println("printing" + text); // To Print an element Value
     if(driver.getPageSource().contains("No Trainers found"))
{
System.out.println("No Trainer available for this Specific Period");
}
else
{
System.out.println("Trainer is available for this Specific Period");
}
     driver.findElement(By.xpath("//android.widget.ImageButton[@content-desc='Navigate up']")).click();
     driver.findElement(By.xpath("//android.widget.ImageButton[@content-desc='Navigate up']")).click();
     
     driver.findElement(By.xpath("//android.widget.TextView[@text='Stretch']")).click();
		driver.findElement(By.xpath("//android.widget.EditText[@text='Search Location']")).sendKeys("Texas");
		driver.findElement(By.xpath("//android.widget.RadioButton[@text='Male']")).click();
		//driver.findElement(By.xpath("//android.widget.TextView[@text='SELECT DATE']")).click();
		//driver.findElement(By.xpath("//android.widget.Button[@text='OK']")).click();
		//driver.findElement(By.xpath("//android.widget.TextView[@text='SELECT TIME']")).click();
		//driver.findElement(By.xpath("//android.widget.RadialTimePickerView$Radia[@index='11']")).click();
		///driver.findElement(By.xpath("//android.widget.Button[@text='OK']")).click();
		driver.findElement(By.xpath("//android.widget.Button[@text='Continue']")).click();
    WebElement text1 =  driver.findElement(By.xpath("//android.widget.TextView[@resource-id='com.fitz.android.fitz_android:id/trainer_not_found']"));
    text.getText();
    System.out.println("printing" + text1); // To Print an element Value
  if(driver.getPageSource().contains("No Trainers found"))
{
System.out.println("No Trainer available for this Specific Period");
}
else
{
System.out.println("Trainer is available for this Specific Period");
}
  driver.findElement(By.xpath("//android.widget.ImageButton[@content-desc='Navigate up']")).click();
  driver.findElement(By.xpath("//android.widget.ImageButton[@content-desc='Navigate up']")).click();
  
  
  driver.findElement(By.xpath("//android.widget.TextView[@text='Body Weight']")).click();
	driver.findElement(By.xpath("//android.widget.EditText[@text='Search Location']")).sendKeys("Texas");
	driver.findElement(By.xpath("//android.widget.RadioButton[@text='Male']")).click();
	//driver.findElement(By.xpath("//android.widget.TextView[@text='SELECT DATE']")).click();
	//driver.findElement(By.xpath("//android.widget.Button[@text='OK']")).click();
	//driver.findElement(By.xpath("//android.widget.TextView[@text='SELECT TIME']")).click();
	//driver.findElement(By.xpath("//android.widget.RadialTimePickerView$Radia[@index='11']")).click();
	///driver.findElement(By.xpath("//android.widget.Button[@text='OK']")).click();
	driver.findElement(By.xpath("//android.widget.Button[@text='Continue']")).click();
WebElement text2 =  driver.findElement(By.xpath("//android.widget.TextView[@resource-id='com.fitz.android.fitz_android:id/trainer_not_found']"));
text.getText();
System.out.println("printing" + text2); // To Print an element Value
if(driver.getPageSource().contains("No Trainers found"))
{
System.out.println("No Trainer available for this Specific Period");
}
else
{
System.out.println("Trainer is available for this Specific Period");
}
driver.findElement(By.xpath("//android.widget.ImageButton[@content-desc='Navigate up']")).click();
driver.findElement(By.xpath("//android.widget.ImageButton[@content-desc='Navigate up']")).click();

  
driver.findElement(By.xpath("//android.widget.TextView[@text=' Kettle Bell ']")).click();
driver.findElement(By.xpath("//android.widget.EditText[@text='Search Location']")).sendKeys("Texas");
driver.findElement(By.xpath("//android.widget.RadioButton[@text='Male']")).click();
//driver.findElement(By.xpath("//android.widget.TextView[@text='SELECT DATE']")).click();
//driver.findElement(By.xpath("//android.widget.Button[@text='OK']")).click();
//driver.findElement(By.xpath("//android.widget.TextView[@text='SELECT TIME']")).click();
//driver.findElement(By.xpath("//android.widget.RadialTimePickerView$Radia[@index='11']")).click();
///driver.findElement(By.xpath("//android.widget.Button[@text='OK']")).click();
driver.findElement(By.xpath("//android.widget.Button[@text='Continue']")).click();
WebElement text3 =  driver.findElement(By.xpath("//android.widget.TextView[@resource-id='com.fitz.android.fitz_android:id/trainer_not_found']"));
text.getText();
System.out.println("printing" + text3); // To Print an element Value
if(driver.getPageSource().contains("No Trainers found"))
{
System.out.println("No Trainer available for this Specific Period");
}
else
{
System.out.println("Trainer is available for this Specific Period");
}
driver.findElement(By.xpath("//android.widget.ImageButton[@content-desc='Navigate up']")).click();
driver.findElement(By.xpath("//android.widget.ImageButton[@content-desc='Navigate up']")).click();

  
	}

	public static void swipingVertical(AppiumDriver driver, String ScrollType, String ele) throws InterruptedException {
		// Get the size of screen.
		Dimension size;
		boolean flag = false;
		size = driver.manage().window().getSize();
		System.out.println(size);
		WebDriverWait wait = new WebDriverWait(driver, 1);
		// Find swipe start and end point from screen's with and height.
		// Find starty point which is at bottom side of screen.
		int starty = (int) (size.height * 0.80);
		// Find endy point which is at top side of screen.
		int endy = (int) (size.height * 0.20);
		// Find horizontal point where you wants to swipe. It is in middle of
		// screen width.
		int startx = size.width / 2;
		System.out.println("starty = " + starty + " ,endy = " + endy + " , startx = " + startx);

		if (ScrollType.equalsIgnoreCase("down"))
		// Swipe from Bottom to Top.
		{
			while (!flag) {
				driver.swipe(startx, starty, startx, endy, 3000);
				try {
					wait.until(ExpectedConditions.elementToBeClickable(By.xpath(ele)));

					flag = true;
				} catch (Exception e) {
					flag = false;
					System.out.println("Element is not found, scrolling again");
				}
				// Thread.sleep(2000);
			}
		}
		// Swipe from Top to Bottom.
		else if (ScrollType.equalsIgnoreCase("up")) {
			driver.swipe(startx, endy, startx, starty, 3000);
			Thread.sleep(2000);
		}
	}

	public static void ScrollDirection(AppiumDriver driver, String direction, int duration) {
		Dimension size;

		size = driver.manage().window().getSize();
		System.out.println(size);

		// Find swipe start and end point from screen's with and height.
		// Find starty point which is at bottom side of screen.
		int starty = (int) (size.height * 0.80);
		// Find endy point which is at top side of screen.
		int endy = (int) (size.height * 0.20);
		// Find horizontal point where you wants to swipe. It is in middle of
		// screen width.
		int startx = size.width / 2;
		System.out.println("starty = " + starty + " ,endy = " + endy + " , startx = " + startx);

		if (direction.equalsIgnoreCase("down"))
		// Swipe from Bottom to Top.
		{

			for (int i = 1; i < duration; i++)
				driver.swipe(startx, starty, startx, endy, 15000);

			// Thread.sleep(2000);

		}
		// Swipe from Top to Bottom.
		else if (direction.equalsIgnoreCase("up")) {
			driver.swipe(startx, endy, startx, starty, 3000);

		}
	}

	public static void closeKeyboard(AppiumDriver driver) {
		try {
			driver.hideKeyboard();
		} catch (Exception e) {
			System.out.println("Keyboard is not present");
		}		
	}	
}
