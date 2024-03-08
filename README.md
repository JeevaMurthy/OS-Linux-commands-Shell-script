# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/8ec645b2-415e-4eb2-b353-b3bd980a72b6)



cat < file2
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/48acdb79-1b3b-4996-be4e-81c5e87db18a)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/12fc52be-f138-4291-84ee-2bd1cfda4fc5)

comm file1 file2
 ## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/e7b25c3d-ad0e-422c-b3b1-b491bbeee44d)

 
diff file1 file2
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/52ab01ad-39e1-4ca3-8118-6910a3374708)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/2401713c-2483-492d-8905-25c40ea0a5bc)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/66ab34c9-0e8b-4fd8-b561-29a0d8462c04)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/0a2b3038-2ca3-4a4e-bbc6-d7c9af0559b8)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
 ![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/8af4669e-d13d-4230-bce1-19c02fb96266)



grep hello newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/613d4027-5fa2-4706-b663-a748c33f1478)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/dc50cfa0-2f30-42d4-a420-ce4fbeed8d12)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/ca7b73bc-2718-474f-88b8-7e71f766cb64)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/804b0bfa-83f4-466b-82a3-4d5639d57e2f)




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/2687bda5-aadb-48e9-922e-bd63f2da47c0)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/1218fea4-95dd-470c-ae2a-cb2699d893b0)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/fd91f8ad-0a2c-4ec4-ba0e-09b77c3a3ea2)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/62606a8c-4c50-41ca-8b08-9be1cd0f67b8)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/0c6b3a15-1258-47ad-bd6f-a00f2dc2d26d)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/266afc62-6955-409e-9315-83ced2a8cbf7)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/6cc34e4e-8531-42d0-91d4-a50d8614c01c)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/77e21fc8-790d-4730-9f02-3ba16bde94c6)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/a69f152b-a992-4263-8e35-028b175f8e49)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/77ba612c-a21b-486b-bccd-650d8eb4f730)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/f0656b3b-476a-4156-8e73-943101c792a2)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/603af3c1-b02f-433e-803b-14f6547a9ddb)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/c4bddd4c-5abd-4c57-b789-72cff13c28ca)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/a74040f9-518b-4ec9-a4e3-40c940009572)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/e1bdefce-b3fe-4036-a566-a09b789f8c72)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/9275a483-a5bb-4ef3-8df6-ba3c1bea7ab4)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/82f5d5d1-c7b9-4215-9acf-f4b870224a87)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/e6701927-1458-41f3-80ed-ce5b4e2bddb8)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/1d2bf03a-c2f8-41bf-a29a-1d4e1ccf886a)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/64b7f721-8760-45c9-9f11-ca65aa956f56)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/aad8cb34-1a39-4d1d-9ec2-7a3c6d7982ef)



seq 10 
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/ed207c5f-c1a7-40ff-839b-05641328c277)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/5beacce8-d83c-4e5d-9da6-f2fa7f9a8af6)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/08467bef-22eb-4eda-b581-f857c4dcc3ca)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/f9678413-4e1b-4a58-8eb9-3d70d06a9110)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/03f12492-d12e-419b-95b0-ff8146144d0c)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/6c72a53f-07fb-4222-bc96-522e104af61f)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/85d6830e-965f-4550-8506-9ae725e220c2)



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/640471f7-0f7c-4036-bfc3-8fba5aa04fab)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/0169c0e7-d8a9-457d-a1c8-dda191004e24)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/4b28efcb-7154-4d69-ad5d-f73f0e63e4f8)


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/8d1f0cf1-e95f-410b-8408-cfba575c8793)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/JeevaMurthy/OS-Linux-commands-Shell-script/assets/147222117/53f9845b-50db-4334-9145-02a2eb250bac)



# Backup commands
tar -cvf backup.tar *
## OUTPUT
![alt text](image-36.png)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![alt text](image-35.png)

tar -xvf backup.tar
## OUTPUT
![alt text](image-34.png)
gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![alt text](image-33.png)

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![alt text](image-32.png)
 
ls file1
## OUTPUT
![alt text](image-31.png)
echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
![alt text](image-30.png)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![alt text](image-29.png)

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![alt text](image-28.png)
# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![alt text](image-27.png)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
![alt text](image-26.png)
# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
![alt text](image-25.png)
# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![alt text](image-24.png)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![alt text](image-23.png)
# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
## OUTPUT
![alt text](image-22.png)
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## OUTPUT
![alt text](image-20.png)
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
## OUTPUT
![alt text](image-19.png)
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
## OUTPUT
![alt text](image-18.png)
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
## OUTPUT
![alt text](image-17.png)
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
## OUTPUT
![alt text](image-16.png)
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![alt text](image-15.png)
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![alt text](image-14.png)

cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![alt text](image-13.png)
cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![alt text](image-12.png)
cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
## OUTPUT
![alt text](image-11.png)
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![alt text](image-10.png)
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![alt text](image-9.png)
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![alt text](image-8.png)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![alt text](image-7.png)


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
![alt text](image-6.png)
 
 ./funcex.sh 1 2
![alt text](image-5.png)
 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
![alt text](image-4.png)
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
![alt text](image-3.png)
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 ![alt text](image-2.png)
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ![alt text](image-1.png)
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![alt text](image.png)

# RESULT:
The Commands are executed successfully.
