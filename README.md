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
![Screenshot from 2025-03-03 09-27-51](https://github.com/user-attachments/assets/2ab25b05-54f6-4bb4-b9ef-2df849b038a4)




cat < file2
## OUTPUT
![Screenshot from 2025-03-03 09-28-04](https://github.com/user-attachments/assets/064e318d-c3eb-4d6f-8944-18cd6b8d7de1)



# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-03-03 09-30-18](https://github.com/user-attachments/assets/0ea064f2-03db-452a-aee9-e7e07a12c322)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-03-03 09-30-30](https://github.com/user-attachments/assets/1fe1c4f0-f992-4850-89b9-31d056d75e48)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-03 09-31-32](https://github.com/user-attachments/assets/bc5e5a75-0bf7-4a9c-ab27-00308b57c255)


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
![Screenshot from 2025-03-03 09-43-25](https://github.com/user-attachments/assets/622f8b1b-1846-4a05-b696-820863aea531)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-03 09-43-36](https://github.com/user-attachments/assets/9bfe42fe-a6c1-402f-901a-b3e68a4e703f)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-03 09-50-10](https://github.com/user-attachments/assets/319b7ff3-d944-4682-bb23-fef1d4f42508)


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
![Screenshot from 2025-03-03 09-47-40](https://github.com/user-attachments/assets/1807913d-280d-4a7c-9cfc-023ee2fb4ee3)



grep hello newfile 
## OUTPUT

![Screenshot from 2025-03-03 09-47-49](https://github.com/user-attachments/assets/9bc6327f-af27-44e1-b144-3935fe8b55d4)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-03 09-48-01](https://github.com/user-attachments/assets/7f0aa8b6-003e-4707-ab47-c39c04a375b2)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-03 09-48-20](https://github.com/user-attachments/assets/f112f4d3-bbda-47e4-9bf2-d2915e005d7e)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-03 09-48-36](https://github.com/user-attachments/assets/ea9df5ae-ef14-42cd-9dc3-92029028780f)




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-03 10-03-56](https://github.com/user-attachments/assets/0489bc0c-a122-4920-b4a1-f793179a5df8)


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

![Screenshot from 2025-03-06 09-26-25](https://github.com/user-attachments/assets/a59ac5f3-8178-4fe9-91fb-571ef675fac0)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-26-33](https://github.com/user-attachments/assets/d8e765fb-9291-4d41-bf04-017d63d1001b)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-26-45](https://github.com/user-attachments/assets/6e3df2fb-e726-47ff-9648-0781221f2e1a)


egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-37-20](https://github.com/user-attachments/assets/2dc09255-0be4-4e8c-9fc2-6b2805819ac2)

egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-27-39](https://github.com/user-attachments/assets/71f64f92-b1ca-430a-b8c7-700787df04c9)


egrep '(World$)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-30-09](https://github.com/user-attachments/assets/7ff02c75-7413-4c29-bd02-339a2b08f3f3)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-30-26](https://github.com/user-attachments/assets/d6e08e19-a0b8-4a07-83c5-54d131f1d61d)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-32-04](https://github.com/user-attachments/assets/00f6c228-815b-4501-9556-9e494fbe7e4d)


egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-32-40](https://github.com/user-attachments/assets/0612bdb8-2eea-490b-b38b-c8b433a25791)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2025-03-06 09-32-55](https://github.com/user-attachments/assets/e97565a1-1ae7-4e1f-8638-f5e9124e9054)

egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-03-06 09-33-16](https://github.com/user-attachments/assets/0297ec9c-eac0-4249-a8c8-0ed937e776a4)


egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot from 2025-03-06 09-33-43](https://github.com/user-attachments/assets/d5ff1101-5282-4918-a87d-a5de7e06c016)


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

![Screenshot from 2025-03-06 09-47-25](https://github.com/user-attachments/assets/07943aac-f979-43dc-8893-ca1ab7770d16)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-03-06 09-47-33](https://github.com/user-attachments/assets/83005360-c36b-4c6e-a018-84706023f63d)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-06 09-47-55](https://github.com/user-attachments/assets/bb007092-10a9-4dbc-b768-fad18ded21f2)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-06 09-48-04](https://github.com/user-attachments/assets/c96ca1c4-a564-402a-a793-f5ead8a35485)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-03-06 09-48-18](https://github.com/user-attachments/assets/b0c5e973-f40c-4f8d-8299-d11216348043)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-03-06 09-48-31](https://github.com/user-attachments/assets/3e4c3cf5-0021-4874-9ca2-c2817b49d042)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-03-06 09-48-47](https://github.com/user-attachments/assets/ce26dee3-0db7-4a81-8759-a6f4d7b304fe)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-03-06 09-48-59](https://github.com/user-attachments/assets/abe04b27-7644-415a-944b-db8a95173d5b)


seq 10 
## OUTPUT

![Screenshot from 2025-03-06 09-49-24](https://github.com/user-attachments/assets/28e04716-2dbf-484d-ae26-53166f2cb725)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-03-06 09-49-44](https://github.com/user-attachments/assets/8c989f06-54d8-462e-8fef-91ee6ac7fc35)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-03-06 09-50-00](https://github.com/user-attachments/assets/7f3b91fa-4e14-40b7-b138-f7399d81ac4f)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-03-06 10-08-41](https://github.com/user-attachments/assets/4a56f0fc-0aa7-468b-a285-962ac4a462b4)


seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-03-06 10-09-23](https://github.com/user-attachments/assets/02baa0d9-e43b-4057-8b3d-a671092e88ac)

seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-03-06 10-09-48](https://github.com/user-attachments/assets/f7fa4b55-fd28-4923-92e7-9665edcd6379)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-03-06 10-10-01](https://github.com/user-attachments/assets/ae8a4e5f-2919-4823-a789-e17b13508d45)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot from 2025-03-06 10-10-22](https://github.com/user-attachments/assets/0343534a-95f9-41cf-9996-15e3bbbd62c1)

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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

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

 
ls file1
## OUTPUT

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
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
##OUTPUT

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
##OUTPUT

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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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

 
 ./funcex.sh 1 2

 
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


# RESULT:
The Commands are executed successfully.
