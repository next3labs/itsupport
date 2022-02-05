# Installing Microsoft 365 on Windows 7 32 bits

**Microsoft has ended support for Microsoft 365.** 

https://docs.microsoft.com/en-us/deployoffice/endofsupport/windows-7-support

Hence, the latest Microsoft 365 installer will not run on Windows 7.  The last version that you can install on Windows 7 is **16.0.12527.20880**

To do this, you will need to run the office deployment tool manually.

Download the Office Deployment Tool -
https://www.microsoft.com/en-us/download/details.aspx?id=49117

Unpack the file downloaded, then run setup again the configuration file below. 

eg. if the configuration file is office.xml, the command would be

    setup /configure office.xml

The setup process is quite long due to the download, so get your coffee while you wait.
    <!-- This configuration installs the last supported version of Microsoft 365 for Windows 7 32 bit  -->
    
    <Configuration>
      <Add 
	      OfficeClientEdition="32" 
	      Channel="Current" 
	      Version="16.0.12527.20880"
	  >
        <Product ID="O365ProPlusRetail">
          <Language ID="en-us" />
        </Product>
      </Add>
      <!--  <Updates Enabled="TRUE" Channel="Current" /> -->
      <!--  <Display Level="None" AcceptEULA="TRUE" />  -->
      <!--  <Property Name="AUTOACTIVATE" Value="1" />  -->
    </Configuration>




