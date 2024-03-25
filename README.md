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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/d30add2b-c855-4fcc-a4c8-405eade17a4b)

 cat < file2
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/f7000fd5-f910-467f-9525-ffb161be853e)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/76b4a936-602f-47f2-86da-d56c68616ba9)

comm file1 file2

 ## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/332ca85b-57d1-4c88-bb49-8cf2e288e068)

diff file1 file2
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/eb3dd8e6-5db5-4575-bf4a-eb447d6837ab)


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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/2023d972-e3cb-4f5c-a26e-5331677522c7)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/70de7b58-6879-43af-b3fa-acfd72cbda4e)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/45394aff-704a-4a43-9c32-fd63d2a3f82a)


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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/3f7c4d0f-0675-4739-9817-5611a43d8100)



grep hello newfile 
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/d6ec9124-fbaf-4a24-8bb2-66a0a125b353)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/dceefd27-9f60-4d74-ac58-d81301110157)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/52c42650-808e-48cc-9cbe-1385e8466a15)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/911bf28c-1f06-424b-900f-8a7d83b4c97b)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/2c971571-9416-4ea7-be0d-b94a1cd7ea1f)

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

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/6778f00e-b2e2-4235-b80a-3ea3e9a9c410)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/d253ed79-2c44-4a0e-ae7f-a3f24d7f4b15)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/fdd87003-a010-499b-a1aa-203959245fdb)


egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/1a1e44ea-8dc1-4ed4-aa34-5d477dc04017)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/e2414657-02ed-4c9f-b7cf-af9071235e6d)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/185eb153-cb1b-4d52-aec7-ed192666846f)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/4564ca35-a9c5-44f2-b0e7-f161eef6bbf8)


egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/a35d77ed-6ab7-40fd-bd7b-9ed9175c33fc)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/aa83c3b0-9750-4ee7-a6ab-fa65387d1df4)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/ba2f32f2-d6c6-45f3-8a50-0b59e043cf6f)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/601f7c22-c097-4531-b639-2df6638762b4)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/3a8e8e60-a66d-4a11-8814-edab735b526d)


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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/8162c262-e03e-409b-8f5f-0d17cfd0e8e7)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/8a48fa53-fc61-417d-ae71-f24370955731)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/d2e1dc0e-23b1-4846-9499-79cf97977428)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/17031e4a-0dd1-4013-8810-390abb41130b)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/c933437c-9721-4009-a50b-4dcd633a294f)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/6152508c-d7bb-43c5-8a76-9d83d506245a)



sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/290c48d8-fa7b-4704-ba26-6e06fa4b4264)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/99665ba4-4e99-4e12-8c80-607ae7b2e464)


seq 10 
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/243e1a90-3a30-4bc5-9a3d-3d443cf7c2aa)



seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/234e7b89-14cd-4a47-a00b-32c98316acd3)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/8a362b80-e12f-4c90-aece-62c696f889e8)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/a785069e-61ed-463c-a2df-715d85fb8a38)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/030fd5ad-9257-4373-8c48-d532ce3d3953)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/82baf7ff-83d9-4a47-9691-6aeb244365ab)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



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

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/68d6973c-8dc0-4f7f-ad4a-d080f2531cc7)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/18faf860-b8f7-4f87-8c02-a28becb298fc)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/41922d2c-c88f-428a-9b64-983529805b14)

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

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/f6283ff4-e017-4cf1-a2ce-8df0554192ee)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/cc55fa29-4b83-4a2a-93b1-d6721e110f93)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/f460d633-f4f3-4641-8c0b-b3a972d85d0e)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/e2c70bc4-1381-484e-9e8a-9aa95e239286)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/ebdfa3bc-f2ba-4254-ae96-493559988727)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/f648f632-61b2-4d80-a124-16cdc28ef7ef)


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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/dabd452f-ae90-4b8a-b055-e7453056c7e8)

 
ls file1
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/968edd0d-1022-44bc-a575-cae4a82a4849)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/35e145fa-aa2a-42c1-b859-9ab7904d2503)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/c6ae26c5-1616-4bef-b610-78ad1931da41)


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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/6c7ed860-c1f2-444c-afe0-12cbbb91b01b)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/29feb126-e6d1-4214-bccc-b4a21841ad6f)



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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/f69c28d6-a589-4479-854c-2b8cdbf8f1e0)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/d5afa7aa-5cf9-4f3e-8c4a-ecc7e40f9460)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/ccac53e9-efa3-4198-bb43-05e803522833)


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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/b4152443-9aff-4de5-995e-8ce2ee7120ca)

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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/d6e2748c-459d-4188-9f1e-275795126370)

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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/231d9b25-e67b-4489-966f-23113d3da13b)

 
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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/a587e03d-fb88-476c-bdfe-657c735ef7a9)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/944548a2-e34c-4773-8869-0379ca385111)

 
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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/c72f6c09-9e16-490b-8146-b03ff4f77f43)

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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/92bc0706-786b-4a1b-a764-10e69d223ef3)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/91289d1d-1edd-443e-b6c2-599750ea460c)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/60472b2d-35f2-4250-ac15-73f27b213dd1)


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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/59578020-d11e-4949-9359-a777eb30115a)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/621f8174-587e-409e-b744-c5e0bffd0b95)

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

 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/fc177f32-2d6c-47f5-af9d-411ba34a1b03)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/471877c0-2712-4050-a57e-725878e4dceb)

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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/d4cc1660-92cb-410e-867d-c3cf9272165e)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/10f2b7ee-a56d-4f20-9a2f-25c340d42932)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/cf69ef9d-fb7c-4ca5-bc1e-950b33549ced)


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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/b2ede66d-fcc9-4a7e-9856-1d1dfcd61963)

 
 ./funcex.sh 1 2
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/9e53f4d6-f5d8-48f4-aeb2-5d8e44f4bdad)

 
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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/6955a771-cedc-4694-8d5f-105726bb057f)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/7b2c8a78-609f-42aa-a225-77990d8c6fb9)

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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/45066861-e388-4da7-a59a-8f780188b9ff)

 
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
 ![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/0bc62d14-5aa2-478f-8d3f-c63e48f70af1)

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
![image](https://github.com/MARXINLIJO/OS-Linux-commands-Shell-script/assets/145742540/17fd94a9-a5e8-4ad5-855a-130a71679c06)


# RESULT:
The Commands are executed successfully.
