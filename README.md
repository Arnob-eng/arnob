CREATE DATABASE company11;
USE company11;
CREATE TABLE country(
 countryid INT PRIMARY KEY,
 countryname VARCHAR(20),
 continent VARCHAR(10),
 currency VARCHAR(15)
);
INSERT INTO country
VALUES(
 (10, "Bangladesh", "asia", "taka")
 (11, "India", "asia", "rupi"),
 (12, "france", "europe", "euro"),
 (15, "USA", "North america", "dollar"),
 (16, "UK", "europe", "euro")
);
CREATE TABLE department(
 deptiid INT PRIMARY KEY,
 deptname VARCHAR(20),
 countryid INT NOT NULL,
 FOREIGN KEY(countryid) REFERENCES country(countryid)
);
INSERT INTO department
VALUES(
 (103, "CSE", 10)
 (105, "LAW", 11),
 (106, "EEE", 12),
 (107, "SWE", 15),
 (202, "ADS", 16)
);
CREATE TABLE employee(
 empid INT PRIMARY KEY,
 empname VARCHAR(20),
 deptid INT NOT NULL,
 FOREIGN KEY(deptid) REFERENCES department(deptid)
);
INSERT INTO empolyee
VALUES(
 (1003, "Arnob", 30000)
 (1005, "Adib", 25000),
 (1006, "Antor", 35000),
 (1007, "Sabit", 35000),
 (2002, "Pritam", 36000)
);
CREATE TABLE Folder(
 Folderid INT PRIMARY KEY,
 empid INT,
 accesstype VARCHAR(20),
 FOREIGN KEY(empid) REFERENCES employee(empid)
);
INSERT INTO Folder
VALUES(
 (1, 1003, "veiw")
 (2, 1005, "edit"),
 (3, 1006, "write"),
 (4, 1007, "read"),
 (5, 2002, "edit")
); 
