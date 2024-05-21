# Zip Code Database RESTful Interface

This project provides a RESTful interface for navigating and updating a Zip code database using Flask. It fetches data from a CSV file and displays it. The interface allows searching for populations by Zip code and updating Zip code details, with changes reflected in the database managed via PhpMyAdmin. The source code was adapted from another GitHub repository by ellisju37073.

## Features

- **Search Population by Zip Codes**: Retrieve and display Zip code information.
- **Update Zip Codes**: Modify Zip code details in the database.
- **CSV Import**: Fetch initial data from a CSV file.
- **Database Management**: Utilize PhpMyAdmin for database management.

## Prerequisites

- Python 3.x
- WAMP Server (Windows, Apache, MySQL, PHP)
- MySQL database with PhpMyAdmin
- Packages: Flask, pandas, SQLAlchemy, PyMySQL, mysql-connector-python

## Installation

1. **Set Up WAMP Server**

   - Download and install [WAMP Server](http://www.wampserver.com/en/).
   - Ensure that Apache and MySQL services are running.
   - Access PhpMyAdmin via `http://localhost/phpmyadmin` to manage your MySQL databases.

2. **Clone the Repository**

   Clone this repository to your local machine:
   ```bash
   git clone https://github.com/YeabMoges/RESTful-DB
   ```

3. **Install Required Packages**

   Use pip to install the required packages:
   ```bash
   pip install flask pandas sqlalchemy pymysql mysql-connector-python
   ```

4. **Database Setup**

   - Open PhpMyAdmin and create a new database (e.g., `zipcode_db`).
   - Create a table for Zip codes using the following SQL command:
     ```sql
     CREATE TABLE zipcodes (
         id INT AUTO_INCREMENT PRIMARY KEY,
         zip VARCHAR(10) NOT NULL,
         Population INT,
     );
     ```

5. **Configuration**

   Update the database configuration in your Flask application (`zipcodes.py`) with your MySQL credentials and database name.


## Project Structure

```
RESTful-DB/
│
├── database/
│   ├── csv/
│       └── zip_code_database.csv    
│   └── zipcodes.py
│
├── templates/
│   ├── login.html
│   ├── search_results.html
│   └── update_success.html
│
├── rest_web.py
└── README.md
```

