# Tutorial
----------
Let suppose if you want to cat the content of users file you will create a bash script and ask user to input their filename and it will then parse and send you the cat output
The example of the bash file you'll make is as follows:
```#!/bin/bash
echo "Enter the filename to read it's content : "
read filename;
file_content=$(cat $filename);
sleep 5;
echo "Reading the file content....."
echo "$file_content";
```
This is a simple bash script which reads the output of the user(filename) and then outputs it's content.
Now there is a way around which is more preffered to use instead of asking user the input of filename.User can directly input the file name as argument when he writes the script name.
For example instead of reading the output we will write $1(which means the first argument we'll talk about it later in this article):
```#!/bin/bash
file_content=$(cat $1);
sleep 5;
echo "Reading the content of the file....."
echo "$file_content";
```
User can now specify the file directly in the parameter.
`./myscript.sh /etc/passwd`
The above command will cat the content of */etc/passwd* file
*Parameter arguments*
$0 ----> The script itself
$1 ----> First argument 
$2 ----> Second argument
$3 ----> Third argument
$n ----> There can be multiple arguments passed as per script need for double digit argument we need to wrap it in {} braces for example ${10}
$# ----> This means the total number of arguments passed to the script
$@ ----> The total number of arguments passed to the script
$? ----> The exit status of the last executed command
$! ----> The process id of the last executed command
$$ ----> The process id of the current shell

# Exercise
----------
There is no exercise for the given article
