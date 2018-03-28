 Selenium-Framework
My Selenium TestNG FrameWork Project
package Academy;
//import org.junit.Test;


import java.io.IOException;

import org.testng.annotations.AfterTest;
import org.testng.annotations.Test;

import junit.framework.Assert;
import page_Objects.Landing_Page;
//import junit.framework.Assert;
//import page_Objects.Landing_Page;
import resources.base;

public class Validate_Title extends base {
	
	//WebDriver Driver1;
	@Test
	public  void Title1() throws IOException
	{
		Driver = invokebrowser();
		Landing_Page lp = new Landing_Page(Driver);
		//Landing_Page lp = new Landing_Page(Driver);
		Assert.assertEquals("FEATURED COURSES",lp.Title().getText());
		//Assert.assertTrue(lp.Nav().isDisplayed());
	}

	@Test
	public  void Title2() throws IOException
	{
		Driver = invokebrowser();
		Landing_Page lp = new Landing_Page(Driver);
		//Assert.assertEquals("FEATURED COURSES",lp.Title().getText());
		Assert.assertTrue(lp.Nav().isDisplayed());
	}
	@AfterTest
	public void  Close_Browser() 
	{
		Driver.close();
		Driver=null;
	}
}
