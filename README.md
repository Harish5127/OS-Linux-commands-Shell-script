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

![Screenshot from 2025-03-10 08-04-27](https://github.com/user-attachments/assets/c9afafb9-095c-4996-a1af-2262192b8307)

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

![Screenshot from 2025-03-10 08-05-11](https://github.com/user-attachments/assets/d9fa7fd4-ae66-492c-a9c3-0cfcd91a03be)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![Screenshot from 2025-03-10 08-06-10](https://github.com/user-attachments/assets/17fcc9a0-5d42-4cdc-8fad-6ddc8e1ea2e7)

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

![Screenshot from 2025-03-10 08-15-04](https://github.com/user-attachments/assets/99a7fab6-afc4-4bb8-b76f-11e1e56c41da)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-03-10 08-15-20](https://github.com/user-attachments/assets/2e3db8ee-c90f-4f3d-81a3-0c95f2fd3d35)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot from 2025-03-10 09-40-19](https://github.com/user-attachments/assets/bc497a1c-4908-45ba-a9dc-efc5de09c381)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![Screenshot from 2025-03-11 22-56-07](https://github.com/user-attachments/assets/4241fbc6-f5d2-459f-b684-84c9dd747213)

tar -xvf backup.tar
## OUTPUT

![Screenshot from 2025-03-11 22-57-06](https://github.com/user-attachments/assets/ea9f74cf-5b24-4ffa-b973-65a529704273)

gzip backup.tar


ls .gz
## OUTPUT

![Screenshot from 2025-03-11 23-20-59](https://github.com/user-attachments/assets/823e123d-e312-4d87-a926-3bea5c209a0e)

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

![Screenshot from 2025-03-13 00-23-16](https://github.com/user-attachments/assets/e215ab41-413a-4e36-a91e-00d0e9d7bb0d)

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

![Screenshot from 2025-03-13 00-26-12](https://github.com/user-attachments/assets/184e9041-53ea-4097-ba43-e46990c292bb)

ls file1
## OUTPUT

![Screenshot from 2025-03-13 00-26-36](https://github.com/user-attachments/assets/d4262028-fee2-4c4a-957d-7d023d01842b)

echo $?
## OUTPUT 

![Screenshot from 2025-03-13 00-26-48](https://github.com/user-attachments/assets/8dcf68ed-f6f5-415f-8f3f-e080904f4de3)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![Screenshot from 2025-03-13 00-33-53](https://github.com/user-attachments/assets/fa2128ff-eb70-4117-b95d-f843455489b5)

abcd
 
echo $?
 ## OUTPUT
 
![Screenshot from 2025-03-13 00-33-38](https://github.com/user-attachments/assets/41ef7015-a80a-4a5b-8d54-bfb2c1c45709)

 
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

![Screenshot from 2025-03-13 00-35-15](https://github.com/user-attachments/assets/c16e9682-a413-4454-a16c-a22d18a40a76)

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

![Screenshot from 2025-03-13 00-38-55](https://github.com/user-attachments/assets/0d208821-05fb-4dab-a0fe-edf1d594c35f)

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

![Screenshot from 2025-03-13 00-40-19](https://github.com/user-attachments/assets/8ea7ebd5-16ce-412d-95dc-710239f5e1aa)


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

![Screenshot from 2025-03-13 00-41-25](https://github.com/user-attachments/assets/1df4130e-26be-4d6a-a221-fc908a1fd361)

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

![Screenshot from 2025-03-13 00-42-55](https://github.com/user-attachments/assets/ace92d66-272b-479e-b1bc-e9d04e214202)

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

![Screenshot from 2025-03-13 00-43-55](https://github.com/user-attachments/assets/7bcb13bc-d8b5-403d-972f-7330cb76b6bd)

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

![Screenshot from 2025-03-13 00-46-56](https://github.com/user-attachments/assets/15f9bd7a-c56a-4fe1-a64c-8ef00a038585)

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

![Screenshot from 2025-03-13 00-47-47](https://github.com/user-attachments/assets/b1c9a923-15e2-47c4-bd90-66c6aa91d47d)


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
 
![Screenshot from 2025-03-13 01-04-35](https://github.com/user-attachments/assets/36645f92-92d6-4546-b1df-75d808741961)

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

 ![Screenshot from 2025-03-13 01-05-26](https://github.com/user-attachments/assets/105fe629-b1d7-455d-af76-09ff8cfb2b46)

 
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

 
 ![Screenshot from 2025-03-13 01-06-23](https://github.com/user-attachments/assets/d4eb7fad-a0c2-4b2b-9fe2-bff43cc278ef)

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

 ![Screenshot from 2025-03-13 01-15-23](https://github.com/user-attachments/assets/ace1b994-478c-4048-b8e0-e52130d42029)
 
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

 ![Screenshot from 2025-03-13 01-27-57](https://github.com/user-attachments/assets/9000aff6-abd2-431c-b5a7-05b1dc241120)

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

![Screenshot from 2025-03-13 01-41-55](https://github.com/user-attachments/assets/f65d0145-eda4-40c7-83ea-6b6ec404ed4b)

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

![Screenshot from 2025-03-13 09-45-08](https://github.com/user-attachments/assets/ecfba77b-c0d8-4437-bbf2-b90818a14ee4)

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

![Screenshot from 2025-03-13 09-46-47](https://github.com/user-attachments/assets/3a88527d-2b5f-4638-bdaa-0048821d0d44)

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

![Screenshot from 2025-03-13 09-47-25](https://github.com/user-attachments/assets/cc7f9e63-cdd9-4043-9377-6176acffe613)

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

![Screenshot from 2025-03-13 10-02-13](https://github.com/user-attachments/assets/412cdd51-6e21-430c-aea8-4b5f255a4526)

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

![Screenshot from 2025-03-13 10-02-58](https://github.com/user-attachments/assets/13e4f854-8b49-47de-8045-266d83928f8a)

cat forcontinue.sh 
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

![Screenshot from 2025-03-13 10-04-41](https://github.com/user-attachments/assets/1a1ac5e0-87fd-458d-b64c-a01510d98baf)

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

![Screenshot from 2025-03-13 10-05-50](https://github.com/user-attachments/assets/f7aaeeb7-def2-4b1d-8530-5c7e0719565e)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh 

## OUTPUT

![Screenshot from 2025-03-13 10-07-38](https://github.com/user-attachments/assets/90030979-8627-484d-86ff-962156abd59a)

 
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

 ![Screenshot from 2025-03-13 10-10-17](https://github.com/user-attachments/assets/c9beb15e-c08c-4380-8612-18828c8bb4e7)


 ./funcex.sh 1 2

 ![Screenshot from 2025-03-13 10-10-38](https://github.com/user-attachments/assets/30a6a0e5-5cd3-4b93-a475-d72bce6ce9fc)

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

 ![Screenshot from 2025-03-13 10-11-40](https://github.com/user-attachments/assets/8e8fbc7a-39b2-437f-b6c0-489648cc3148)

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
 
![Screenshot from 2025-03-13 10-31-50](https://github.com/user-attachments/assets/4f94ac16-3bce-48d8-bdfb-5349db953f56)

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
 
![Screenshot from 2025-03-13 10-33-25](https://github.com/user-attachments/assets/029d5638-93aa-45dc-abe1-69ba70f53359)

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

![Screenshot from 2025-03-13 10-36-32](https://github.com/user-attachments/assets/55338cce-fd8b-42a5-88ed-c2750c988b03)


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

![Screenshot from 2025-03-13 10-38-24](https://github.com/user-attachments/assets/9f32d1bd-0de8-498a-bdee-afefdf138d82)

# RESULT:
The Commands are executed successfully.
