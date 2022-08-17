# NAUPA-III-Schema

General Information

The National Association of Unclaimed Property Administrators (NAUPA) has created this reporting format to make electronic reporting more uniform. Two previous NAUPA formats have been offered, first in the 1990s and then 2000s.  They have been modified over the years. This most recent version has not only added new data elements and codes but has moved from the fixed width format to Extensible Markup Language (XML).  When using the NAUPA format to report, do not mix and match which version is being used.  Check with the jurisdictions in which you will report to determine which version(s) of the NAUPA layout is accepted.

The purpose of this document is to assist all parties with understanding the general layout structure and identifying all the various data elements and codes. Included with this document is an XML Schema Definition (XSD). The XSD provides specific guidance on how to create and test your final XML file before sending it to the appropriate Unclaimed Property jurisdiction. The XSD file contains logic which allows an associated XML file to be validated, to ensure that the data has been entered and is in the proper format. For example, if the XSD requires that a particular field contain a dollar amount, the presence of non-numeric characters will generate an error.

In addition to the XSD each state may have additional reporting requirements. NAUPA encourages you to check with each Unclaimed Property jurisdiction if they have any additional requirements or verification that will be performed.

XML Structure

XML is a language used for storing and transporting data.  XML can be read and processed by computers, but can also be human-readable.uses human and not computer language.  Tags label, categorize, and organize information in a specific way.  A tag for a specific data element is placed between angle brackets (< >). 

There are two types of tagsangle brackets:  starting tagsbrackets, which identify the starting point for the tagged data and ending tagsbrackets, which denote the end point.  TheAn ending tag bracket for a particular starting tagbracket  has a forward slash added to the beginning.  Here is a sample XML tag for a Namename data element, or field:

Note:  XML tags cannot contain spaces, and it is generally considered a best practice to use camel case for tag names.

	<Name>John Smith</Name><name> John Smith </name>

XML also permits tags to be embedded within each other, to denote hierarchical, or related data.  Here is a more complex example of an XML representation of some data about a particular person:

	<Person>
<Name>John Smith</Name>
<PhoneNumber>
<HomeNumber>506 555 3555</HomeNumber>
<MobileNumber>506 555 7653</MobileNumber>
</PhoneNumber>
	</Person>
<person>
		<name> John Smith </name>
		<phone number>
			<home number> 506 555 3555 </home number>
			<mobile number> 506 555 7653 </mobile number>
		</phone number>
	</person>

The specific type of data to be contained between defined tags can be specified set out in a separate XSD file.  This makes it possible to ensure that data being transmitted by XML is of the right type, thereby making it easier for the recipient to process correctlyusually to enable the importing of transmitted data to a database. 

Below is a link to an example NAUPA-III XML file that conforms to the NAUPA-III XML schema. list of all data elements and how they are organized in their hierarchical structure. Each opening tag is in a blue italic font. Each closing tag is in a red italic font. All the data elements within an opening and closing tag can be repeated as many times as needed.

View Example NAUPA-III XML FileView Example XML elements
