
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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/23c092c6-788a-43ab-ba7e-ba9124b16581)



cat < file2
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/5fbfe41c-bdbd-406d-8688-18e1ee467d58)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/e0729d2c-2199-4330-b9e4-2200645ebe4c)


comm file1 file2
 ## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/b4d9e860-7bbe-491a-b33f-5c3964266d94)

diff file1 file2
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/b92aac53-a0af-47f4-b167-d44d2808f75d)


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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/59b75d10-b091-4bd2-97c3-ba54bc446620)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/0996d8f7-bd25-479b-a138-e54f66bcaf2b)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/6af2de0a-baaf-4f6e-abe9-ff76b4d00417)


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/24f34568-fd38-47be-9fd0-f256ae1cdc5f)



grep hello newfile 
## OUTPUT

![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/d9660ca7-22d6-49ca-a37f-dd6cbf0fd60c)



grep -v hello newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/ae0baea6-5113-4d9a-acf1-42155aaf6e45)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/0434422a-04af-49d9-89ce-5b6ea4733a81)




cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/d5f206da-6d16-409e-bc85-8c4c00ea2bdc)



grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/902041cf-f582-4185-970a-06b81832341f)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/681c9d5c-2099-4d58-89d5-52724c6643a2)

cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat <newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/42dd62a2-3075-464b-bcd8-ce4453d5b26d)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/0060d2b7-5427-4bda-8e7d-eef8087670ef)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/0e4f9d3a-fe9f-4ca1-acf7-a5cdcea26f1f)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/69892640-eb63-47d6-9761-267bdae7dc68)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/693f4423-f9d1-4a45-a4b8-cf3a113a48f0)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/557590c8-c566-4309-9462-b2c2786d7bf7)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/0d50f947-d5fc-47d7-9237-2390ce36c37a)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/111afa1a-eaa3-4926-b3e6-29f99a9253a1)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/5454247c-7464-4e22-b5e4-1f9ae21266c7)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/e352a896-4022-46e4-81e9-aa7ccbffdedd)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/0c3998da-9d64-495b-8a2b-e3acfda334a7)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/8b54ad4f-c6fd-4e05-8719-f10ff909490d)


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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/d5937266-564e-42ef-8e84-6b31a9fc113c)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/dadfa3d4-6bca-476f-8cce-7f488ff7b7a1)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/0846fab3-9578-4c96-b1f5-f873d0a2bac9)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/7c5d493c-5701-45fd-a44b-22108ceebb07)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/81c0158a-2dca-4e1b-ac29-de8ca342ebbe)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/a0aa0b72-7f73-40f8-b306-875662e7f42b)

sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/59626a45-e3f6-45b8-b608-863d5e4cdfea)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/bbf59b86-d77d-4abe-8a09-16df7e601f6d)



seq 10 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/831769cf-4b8f-4ebd-bfe8-55e61ac09e58)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/c6f9627b-6b26-49ce-998f-d1088696235b)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/88eddb33-e887-42de-956c-f26a2ff666dd)




seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/356e2969-5689-4634-88d8-4c900fbca6bd)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/38115789-907c-406f-9153-0b370757041d)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/a0c03303-efdc-4d93-b78a-1ce3b06d6f00)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/f77fb1c1-2c47-42ab-b6d3-2c8edc401d5d)


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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/8276495e-c4f6-44f7-8321-8b5973f8935b)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/22ded389-2118-495a-a413-4bc26b7f1e63)

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/436fb252-8e7a-417b-aff1-9860204f7778)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/fe4e0a19-ca62-4041-b89a-c193ad89d8c1)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/2206da92-fac5-4b6b-83a6-f01aef262dc9)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/136bd2ac-b5e6-4661-b445-a8c81efcffe3)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/b8cf3aa3-cd94-4676-adec-1376d464e288)

gzip backup.tar

ls *.gz
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/560717dc-9a9c-40cf-a923-0a62077e1249)

gunzip backup.tar.gz
ls *.gz
la *.tar
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/d2b6a806-1b4c-4f82-a0e8-d82a1b44b1fa)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/167368fa-e2e3-40ea-abc0-fe46a827e392)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/bcdf46c4-3c58-4aca-9ea0-93a56353ea1a)


cat > scriptest.sh 
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
echo 'The $\# is ' $#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/dc1f4bb4-7370-49bc-acaa-7a7d3689910d)

 
ls file1
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/285286a4-c9a5-407a-a335-6c2730771251)


echo $?
## OUTPUT 
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/05be14c8-a511-4e56-bb5f-007d5b81870c)


./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat > strcomp.sh 
```bash
\#!/bin/sh
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
\#!/bin/sh
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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/76d5be49-ec5c-49d4-af51-40acdaf2872b)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/828a2691-2b1e-4bb1-ab5e-46867ea944c4)


# check file ownership
cat >psswdperm.sh 
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
 chmod 755 psswdperm.sh

./psswdperm.sh
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/6d7e346c-6947-41f3-ad5c-793734891166)

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
chmod 755 ifnested.sh
./ifnested.sh 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/58d60442-56ee-4a04-8b33-3c518c899a33)



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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/78b1e667-6455-4a75-a26b-cf73246cd958)

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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/5c0d4f77-57d4-4cb6-8b39-2623a4030b11)

# looking for a possible value using elif
cat > elifcheck.sh 
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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/ba32e0e7-ccd7-4ef0-b6df-9f8093aad92b)


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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/7ed54891-c7df-408a-9b0e-7df1ac44f931)

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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/bc995823-7638-4bc5-b23c-3d800288e79c)


cat > whiletest.sh
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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/0a4aab6f-905f-46c1-9994-16f56d13e20b)

cat > untiltest.sh 
```bash
#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
$ ./untiltest.sh
  ## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/99ec76c8-73e6-4e16-b10a-477e821adf1c)

 
cat forin1.sh 
```bash
#!/bin/bash
#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 $ ./forin1.sh

 ## OUTPUT

![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/1210791e-6915-4105-ab46-413f54b8b8a7)


cat > forin2.sh 
```bash
#!/bin/bash
# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh

$ ./forin2.sh

## OUTPUT 
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/f399141a-fbe1-4791-a7de-c7da68cc8d61)

 
cat > forin3.sh 
```bash
#!/bin/bash
# how to correctly  use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh

$ ./forin3.sh 
## OUTPUT

![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/77783c16-77c5-41ba-bfdb-5f81c6585976)


$ cat > cities
```Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam 
```


$ cat > forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $state"
done
```
$ chmod 777 forinfile.sh

$ cat cities

$ ./forinfile.sh

## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/8b91a683-a130-4a94-8e4c-c16a175528a7)



$ cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
$ chmod 755 forctype.sh

$ ./forctype.sh 

## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/104f5b78-c13a-4584-98c9-c0a751e25722)


cat > forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/9def52be-bdb5-49d8-86dc-d2760f4e5825)


cat > fornested1.sh 
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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/8b33329e-2af4-4463-b182-1bf76b17add8)

 
cat > forbreak.sh 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/57ab5d67-b509-40ef-98dd-70c2758c72e5)

cat > forcontinue.sh 
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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/ec5d313c-b3c1-46e6-8d46-b4b97d2eb567)

cat > exread.sh 
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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/5267f162-c235-4993-b18e-539182fef56e)


 cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh

## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/e892e8c8-a6a0-40e3-9658-c135b88f4491)
 

cat > funcex.sh
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
$ chmod 755 funcex.sh

$ ./funcex.sh 

 
 $ ./funcex.sh 1 2

## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/37e16c8e-50f1-45c2-867b-040722910d4c)


cat > argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh

./argshift.sh 1 2 3

## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/9031d635-4bbf-4997-9386-9c9dbccccec1)


cat > argshift1.sh

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
chmod 777 argshift1.sh

./argshift1.sh 1 2 3

## OUTPUT 
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/1d6aa8e7-06e9-49a5-bd66-e50c9265051a)


cat > argshift2.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
chmod 777 argshift2.sh

 ./argshift2.sh 1 2 3

## OUTPUT
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/d0dd14ae-5aca-4baf-a994-2c2e998f8108)

 
 
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
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/ee629d03-928e-4374-8a2c-e9cc9c1b8f3b)

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
chmod 777 palindrome.sh
./palindrome.sh

## OUTPUT 
![image](https://github.com/Srikaran077/OS-Linux-commands-Shell-script/assets/151993143/a31e765a-54be-4e12-a002-35eeb265badd)


# RESULT:
The Commands are executed successfully.
