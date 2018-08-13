# IE11BrowserTestAutomation

@ashwinnayak

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.ie.InternetExplorerDriver;
import org.openqa.selenium.remote.DesiredCapabilities;

public class internetExplorerPrivateBrowsing {

    public static void main(String args[]){
        createIEInstance();
    }

    public static WebDriver createInstance(){
        DesiredCapabilities capabilities = DesiredCapabilities.internetExplorer();
        capabilities.setCapability(InternetExplorerDriver.FORCE_CREATE_PROCESS, true);
        capabilities.setCapability(InternetExplorerDriver.IE_SWITCHES, "-private");
        System.setProperty("webdriver.ie.driver","C:\\IEDriverServer.exe");
        WebDriver IEDriver = new InternetExplorerDriver(capabilities);
        IEDriver.get("https://www.bing.com/");
        return IEDriver;
    }
}
