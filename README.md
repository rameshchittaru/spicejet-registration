# spicejet-registration
registration of spicejet application

package jetpackage;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;


public class spicejetregiration {

	
	public static void main(String[] args) {
				WebDriver driver = new FirefoxDriver();
				driver.manage().window().maximize();
				driver.get("https://book.spicejet.com/Register.aspx");
				
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_TextBoxAgentUserName']")).sendKeys("Ramesh_123");
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_PasswordFieldAgentPassword']")).sendKeys("Ramesh9966");
		    driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_PasswordFieldPasswordConfirm']")).sendKeys("Ramesh9966");
				

				WebElement title = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListTitle']"));
				Select title1 = new Select(title);
				title1.selectByValue("MR");
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxFirstName']")).sendKeys("Ramesh");
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxLastName']")).sendKeys("ch");
				WebElement day = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBDay']"));
				WebElement month = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBMonth']"));
				WebElement year = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBYear']"));
				
				Select day1 = new Select(day);
				day1.selectByValue("20");
				
				Select month1 = new Select(month);
				month1.selectByValue("6");
				
				Select year1 = new Select(year);
				year1.selectByValue("1991");
				
				WebElement nationality = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListNationality']"));
				Select nationality1 = new Select(nationality);
				nationality1.selectByValue("IN");
				
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxStreetAddress1']")).sendKeys("No-2, ags Street");
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxStreetAddress2']")).sendKeys("velachery");
				WebElement country = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListCountry']"));
				Select country1 = new Select(country);
				country1.selectByValue("IN");
				
				WebElement state = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListState']"));
				Select state1 = new Select(state);
				state1.selectByValue("IN|TN");
					
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxTownCity']")).sendKeys("Chennai");
				
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxPostalCode']")).sendKeys("600064");
	
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxFirstPhone']")).sendKeys("9966417427");
			
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxEmail']")).sendKeys("chittarurameshbabu@gmail.com");
				
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_CheckBoxPromoOpt']")).click();
								
				driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_ButtonSubmit']")).click();
	}
}
						
				

				
				
		
