# Scrape Email Addresses From Websites
The aim of this notebook is to scrape email addresses from websites. It takes a list of website urls, loads each website url in a browser and will attempt to find and scrape any email addresses present within the html of the page. 

Most websites have some variation on the 'contact us' page that contains contact details including email addresses. To try and find this, it will look for any html links on the webpage that contain the word 'contact'. It will open the pages they link to and will scrape any email addresses found on these pages as well.

## How to use: 
Full details can be found in the **emails_scrape.ipynb** file. Below we summarise the key steps: 
1. Create csv file that contains the websites you wish to scrape for email addresses. It must have the following format: 
  - Be called 'websites.csv' 
  - Have a column called 'website' that contains a single website url per row. This defines the websites that will be scraped for email addresses.
  - It can have other columns e.g. for metadata. These will be ignored by the script and will not prevent it from working. 
2. Open the **emails_scrape.ipynb** file (e.g. in jupyter lab or as a standalone jupyter notebook or with any other IDE / tool).
3. Run all cells of the notebook. The notebook handles commonly encountered errors when using chromedriver / selenium and will handle and log any unexpected errors. The log is displayed in the notebook after the scraping has completed. 
4. If the scraping is successful, the scraped email addresses are cleaned and saved to a csv file. The email addresses are stored as semi colon separated strings e.g. 'joe@email.com;andy@email.com'.    
