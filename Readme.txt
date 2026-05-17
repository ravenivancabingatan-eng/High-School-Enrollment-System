How to use the code
High-School-Enrollment-System
System Description

The Enrollment System is a Java-based console application designed to manage student enrollment records. The system allows authorized users to log in and perform operations such as adding, viewing, updating, and deleting student information.

The program uses:

* File handling for saving records
* Regex validation for user input
* Caesar Cipher encryption for passwords
* Role-based access control

There are two types of users:

* Admin → Can add, view, update, and delete records
* Viewer → Can only view records

How to Run
1.Install Java JDK on your computer.
2.Open the project in:

* IntelliJ IDEA
* NetBeans
* Eclipse IDE

3.Create these files in the project folder:
users.txt
data.txt

4.Copy the code into:
EnrollmentSystem.java
5.Compile and run the program.

Features

* User Login Authentication
* 3 Login Attempts Limit
* Role-Based Access
* Add Student Record
* View Student Records
* Update Student Information
* Delete Student Records
* File Saving and Loading
* Regex Input Validation
* Caesar Cipher Password Encryption
* Exception Handling

Sample Accounts

Example content of users.txt:

admin,dplq456,1
viewer,ylhzhu456,2

Username	        Password	           Role
admin	            admin123	           Admin
viewer	          viewer123	           Viewer

Regex Formats
Student ID Format

Format example: HS-0001

HS−\d4

Regex Used:

"^HS-\\d{4}$"

Contact Number Format
Format example: 09123456789

09\d9

Regex Used:

"^09\\d{9}$"

Encryption Used
The system uses Caesar Cipher Encryption.

Each character in the password is shifted by 3 characters
Passwords are encrypted before login verification

Example:

Original Password	      Encrypted Password
admin123	              dplq456
viewer123	              ylhzhu456

Encryption Method:

static String encrypt(String text) {
    String result = "";
    int key = 3;

    for (char c : text.toCharArray()) {
        result += (char)(c + key);
    }

    return result;
}
