
<h1 >FrameWork Architecture</h1>
<img src="https://github.com/ankitspee/MyStore_FrameWork/blob/main/Documentation/FrameworkArchitecture.png"/>
<h1 >PageNavigation</h1>
<img src="https://github.com/ankitspee/MyStore_FrameWork/blob/main/Documentation/PageNavigation.png"/>

<h1>Steps for Log4J ,Extent Report,Data Providers</h1>
1. Log4j
================================================================================

-->Add/Create Log4j.xml in project directory

-->Add/Create Log Class in utility Package

-->Configure @BeforeSuite at BaseClass to configure log4j.xml
DOMConfigurator.configure("log4j.xml");

-->Need to just Call in methods in testCase from Log class




2. DataDriven Testing and DataProvider
================================================================================

-->Add/Create ExcelLibrary in utility package.

-->Create a Folder and add TestData.xlxs in that.

-->Create a package for DataProvider and add DataProvider class there 
and create the object of ExcelLibrary Class

-->Add the DataProvider methods 

-->Call the DataProvider methods from testcases



3. Extent Report
================================================================================

-->Add/Create extent-config.xml file for Extent Report Configuration

-->Add/Create ExtentManager Class in utility Package-- to create the object 
of ExtentHtmlReporter and load extent-config.xml  

-->Create a folder ro Save Extent Report under test-output

-->Configure ExtentManager.setExtent() in @BeforeSuite method in BaseClass

-->Configure ExtentManager.endReport() in @AfterSuite method in BaseClass

-->Add/Create screenShot method in Action/BaseClass

To attach the screenshot in extent report
-->Add/Create a Listener Class -- ListenerClass

-->To call the listener Add the below listener (inside suite tag) 
setting in testng.xml

<listeners>
<listener class-name="com.Project.util.ListenerClass"></listener>
</listeners> 
