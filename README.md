Three-Tier Architecture Setup (Physical Separation)
To implement a three-tier architecture with physical separation, I used three machines:


Presentation Tier – User interface only

Business Tier – Logic and server code (PHP)

Data Tier – Database (MySQL)


Machine Roles:

1️- Data Tier (Machine 1)
  Turn on MySQL in XAMPP

  Open phpMyAdmin

  Create a database called skillswap

  Create two tables:

    messages

    users


2️- Business Tier (Machine 2)
  Turn on the Apache server in XAMPP

  Place all PHP and web application code into the /htdocs directory (e.g., /htdocs/skillswap)

  Open database.php and change the host to the IP address of the data tier machine (where the MySQL database is running)


3️- Presentation Tier (Machine 3)
  No code or server needed

  Simply open a browser and enter the IP address of the business tier machine, followed by /skillswap
  Example: http://192.168.X.X/skillswap

  This accesses the web app through the business tier, which communicates with the data tier


Summary
  Presentation Tier: Only runs the browser

  Business Tier: Runs the application logic and Apache server

  Data Tier: Runs MySQL with tables and handles data

  If the web app loads correctly in the browser of the Presentation Tier, using the Business Tier's IP, and it successfully connects     to the database in the Data Tier, then your 3-tier separation is working correctly. 🎉
