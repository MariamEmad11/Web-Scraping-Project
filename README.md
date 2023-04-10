# Web Scraping Project
Web Scraping has many names, such as Web Harvesting, Screen Scraping, and others. It is a method of extracting large quantities of data from websites and storing it at a particular location (a local file in your computer or a database in a table).
example applyed on : wuzzuf website (Wuzzuf helps you in your career and search to find Jobs across an extensive database of jobs and companies).
python language is used for this project.
detailed explanation:
The code is a Python program that performs web scraping to collect job postings data from the website "wuzzuf.net" for a specific job title entered by the user. The program then stores the data into a CSV file and reads it using the Pandas library. Below is a detailed explanation of the code:

1-The first few lines of the code import the necessary libraries and modules, including requests, BeautifulSoup, csv, itertools, and os.

2-The user is prompted to input the job title they want to search for. The program then replaces any spaces with "+" to format the job title for the URL.

3-A while loop is initiated that will run until all job postings for the given job title have been scraped. The loop will execute the following steps for each page of job postings:

a. The program requests the HTML content of the page using the requests library and saves it to a variable.

b. The content is then passed to BeautifulSoup, which creates a BeautifulSoup object to parse the HTML code.

c. The program then scrapes the necessary data from the HTML code, including the job title, company name, location, skills, and job posting URL. This data is stored in separate lists.
d. The program then checks whether the current page is the last page of job postings for the given job title. If it is, the loop will break. If it is not, the program increments the page number and continues to the next page.

e. If any errors occur during the scraping process, the program will print an error message and continue to the next page.

4-After all job postings have been scraped, the program will initiate another loop to scrape more detailed information about each job posting, including the salary and requirements. This loop will execute the following steps for each job posting URL:

a. The program requests the HTML content of the job posting using the requests library and saves it to a variable.

b. The content is then passed to BeautifulSoup, which creates a BeautifulSoup object to parse the HTML code.

c. The program then scrapes the salary and requirements information from the HTML code and appends them to separate lists.

d. If any errors occur during the scraping process, the program will print an error message and continue to the next job posting URL. In this case, the lists will be appended with the string "GO to Link".
5-After all job postings have been scraped for their detailed information, the program creates a list of all the data scraped from the website and writes it to a CSV file. If the directory does not exist, it will create one with the provided name.

6-Finally, the program reads the CSV file using the Pandas library and displays the data in a DataFrame object.
