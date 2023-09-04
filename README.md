# BizCardX: Extracting Business Card Data with OCR
# Technologies
OCR,streamlit GUI, SQL,Data Extraction
## what is easyOCR
It is a Python library . Optical Character Recognition (OCR) that allows you to easily extract text from images and scanned documents. In my project I am using easyOCR to extract text from business cards.
## Overview
BizCardX is a user-friendly tool for extracting information from business cards. The tool uses OCR technology to recognize text on business cards and extracts the data into a SQL database after classification using regular expressions. Users can access the extracted information using a GUI built using streamlit. The BizCardX application is a simple and intuitive user interface that guides users through the process of uploading the business card image and extracting its information. The extracted information would be displayed in a clean and organized manner, and users would be able to easily add it to the database with the click of a button. Further the data stored in database can be easily Read, updated and deleted by user as per the requirement.
## modules 
1.Pandas - To Create a DataFrame 
2.mysql.connector - To store  the data
3.Streamlit - for Create Graphical user Interface
EasyOCR - To extract text from images
## Steps
#### 1.use pip install command to install the above libraries
#### 2.run streamlit command
#### 3.A webpage is displayed in browser, I have created the app with three menu options namely HOME, UPLOAD & EXTRACT, ALTER where user has the option to upload the respective Business Card whose information has to be extracted, stored, modified or deleted if needed.
#### 4.Once user uploads a business card, the text present in the card is extracted by easyocr library.
#### 5.The extracted text is sent to get_data() function(user defined- I have coded this function) for respective text classification as company name, card holder name, designation, mobile number, email address, website URL, area, city, state, and pin code using loops and some regular expression.
#### 6.The classified data is displayed on screen which can be further edited by user based on requirement.

#### 7.On Clicking Upload to Database Button the data gets stored in the MySQL Database. (Note: Provide respective host, user, password, database name in create_database, sql_table_creation and connect_database for establishing connection.)
#### 8.Further with the help of MODIFY menu the uploaded data’s in SQL Database can be accessed for Read, Update and Delete Operations.
