# Task-in-C


In this challange, you are supposed to implement following functions

FILE* open_file_in_read_mode() - should open file in read mode and return the FILE pointer.

FILE* open_file_in_read_write_mode( )- open file in read and write mode, returns the FILE pointer.

size_t read_file(FILE *fp,char *buffer,int length) - Read the data from the file, fp - FILE pointer. buffer - Buffer where the data needs to be read length - the length of the buffer. This function should return the amount of data that has been read.

size_t write_file(FILE *fp,char *data) - Write the data to the file. fp - FILE Descriptor for the file where the data needs to be written. data - Contains the string that needs to be written.

student_t* read_student_from_file(FILE *fp) - Read the Student data from input file handle and return pointer to student_t structure. Use fscanf function.

void write_student_to_file(FILE *fp,student_t *student) - Write Student data to the file handle. Use fprintf function. While writing Student fields, use space as a separator between fields

size_t read_from_location(FILE *fp,char * buffer,int position,int length) - Read given length of data form a given position in the file. Use fseek() to get to the right position.

Input Format

1st line - data - Text data

2nd line - Flag - 0/1 ->0 represents the file does not exist, 1 represents file exists.

3rd line - count - Number of students records

4th line - id

5th line - name

6th line - college

7th line - passing_year --repeast 3-7 lines--

Constraints

0

Output Format

File Open Successful - When file is opened successfully. Data Written: - Indicates the data written to file Data Read: Indicates data read from the file. id:,name:,college:,passing_year: - student record Data Read at location:, is and size is: - output from read_from_location function

Sample Input 0

ThisIsTest
0
Sample Output 0

File Open Failed
Sample Input 1

ThisIsTest
1
1
1
Ayush
JECRC
2021
Sample Output 1

File Open Successful
File Open Successful
File Open Successful
Data Written:ThisIsTest
Data Read:ThisIsTest
File Open Successful
id:1,name:Ayush,college:JECRC,passing_year:2021
File Data:1 Ayush JECRC 2021 
Data Read at location:9, is ECRC 2021 and size is:9
Sample Input 2

ThisIsTest
1
2
1
Ayush
JECRC
2021
2
Raghav
BIT
2020
Sample Output 2

File Open Successful
File Open Successful
File Open Successful
Data Written:ThisIsTest
Data Read:ThisIsTest
File Open Successful
id:1,name:Ayush,college:JECRC,passing_year:2021
id:2,name:Raghav,college:BIT,passing_year:2020
File Data:1 Ayush JECRC 2021 2 Raghav BIT 2020 
Data Read at location:18, is  2 Raghav BIT 2020 and size is:18
