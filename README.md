# University/school book manegment system
#### Description:
A highly efficient and user-friendly system can be developed to optimize the management of books in educational institutions. With this system, users can save books by inputting details such as the book's name, edition, author, price, and available quantity. Additionally, the system allows for the tracking of which student has borrowed a specific book, including their personal information such as name, student ID, and course. This not only enables schools and universities to effectively keep track of their book inventory, but also facilitates the seamless operation of borrowing and returning books. By employing a local MySQL server, all the information related to the books and their borrowers can be securely stored, even if the application or computer is shut down. Through this system, educational institutions gain the ability to effortlessly monitor the availability and condition of their books, update any necessary information, and track the borrowing history of each student, including the dates of book loans and expected return dates. Such an organized system improves the overall efficiency of book management and promotes a seamless experience for both educators and students.

The main.py file serves as the central hub where the majority of the code for our application resides. Within this file, we meticulously develop various functions that handle crucial operations such as adding, removing, and issuing books. Additionally, we design the framework of the application, ensuring its smooth functioning. This comprehensive code also grants users the ability to add, issue, update, and search for books effortlessly. Furthermore, it establishes a connection with the local MySQL server that is created specifically for this purpose.

The customs.py file plays a crucial role in enhancing the appearance and functionality of the application. It enables us to select and customize the colors of the background and buttons, thereby creating a visually appealing user interface. Additionally, in this file, we specify the names of the columns that the user needs to fill out when adding or issuing books. By doing so, we ensure that the necessary information is.

The credentials.py file serves as a repository for storing essential information related to your MySQL server, such as the host, database, user, and password details. These credentials are crucial for ensuring proper connection and access to the server, where all the information pertinent
#### TO start using:
Install PyMySQL:
pip install PyMySQL

Install Tkinter:
pip install tk

Install MySQL server:

Create a Database and Two Tables:

Create a table "book_list" under the library_management:

create table book_list(

	book_id VARCHAR(10) NOT NULL,
	book_name VARCHAR(50) NOT NULL,
	author VARCHAR(50) NOT NULL,
	edition VARCHAR(10) NOT NULL,
	price Int(6) NOT NULL,
	qty Int(4) NOT NULL,
	PRIMARY KEY ( book_id )
);

Create a table "borrow_record" under the same database:

create table borrow_record(

	book_id VARCHAR(10) NOT NULL,
	book_name VARCHAR(50) NOT NULL,
	stu_roll VARCHAR(15) NOT NULL,
	stu_name VARCHAR(50) NOT NULL,
	course VARCHAR(10) NOT NULL,
	subject VARCHAR(30) NOT NULL,
	issue_date date NOT NULL,
	return_date date NOT NULL
);
