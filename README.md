# secedgar-form13
Processing Form 13F filings for various fund managers

**What is SEC EDGAR?**
EDGAR (Electronic Data Gathering, Analysis, and Retrieval) is an online public database from the U.S. Securities and Exchange Commission (SEC). EDGAR performs automated collection, validation, indexing, acceptance, and forwarding of submissions by companies and others who are required by law to file forms with the SEC.

**How is data stored at the website in general?**
Read https://www.sec.gov/developer and https://www.sec.gov/os/accessing-edgar-data pages in detail to understand how data is stored and can be easily accessed for free by anyone.

**What is form 13F?**
All institutional investment managers with investment discretion of over $100 million or more must report its holdings quarterly on Form 13F with the SEC. It has information about their equity holdings. You may get detailed information about it at https://www.sec.gov/about/forms/form13f.pdf location. Additional information is available at https://www.sec.gov/divisions/investment/13ffaq.htm site.

**Lookup the filings manually.**
You can get to https://www.sec.gov/edgar/searchedgar/companysearch.html site and lookup information for any company or fund. Let us take an example of Berkshire Hathaway Inc. You will see it opened a site with the URL as https://www.sec.gov/edgar/browse/?CIK=1067983&owner=exclude where you can now click ‘View Filings’. You may further filter by typing 13F in the search table. If you go to the bottom of the page, you will see ‘Data source: CIK0001067983.json’. This is the json that we will use to process in this program.

**High Level Logic**
Read CIK
Lookup json for that CIK
Parse it to filter for form 13F filings and up to last X years (in the program took oldest date as Jan 1, 2015).
The based on the adsh number, get the index.json for that filing. Extract the primary xml and the infotable xml files.
Append to the dataframe and finally write to a CSV file. This file may then be used for analysis to see which stocks are being bought/sold

**Warnings**
This is not intended to be any form of advice. These programs are just for fun and feel free to use it anyway you like to. There is no assurance that this is always going to generate accurate information.



