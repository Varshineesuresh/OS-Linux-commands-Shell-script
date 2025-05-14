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

<img width="1581" alt="cat file1" src="https://github.com/user-attachments/assets/c4073ba7-43d0-426e-aa49-853907915886" />


cat < file2
## OUTPUT
<img width="1581" alt="cat file2" src="https://github.com/user-attachments/assets/3ce371b0-8386-4622-ad6f-978dffcdd0ad" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="1593" alt="comp" src="https://github.com/user-attachments/assets/1827a844-cfba-4ca9-964f-ad88d67c6425" />

comm file1 file2
 ## OUTPUT
<img width="1581" alt="comm" src="https://github.com/user-attachments/assets/03f2dd90-60ef-44cb-b66a-1c068bdf38bf" />

 
diff file1 file2
## OUTPUT
<img width="1581" alt="diff" src="https://github.com/user-attachments/assets/8932a53b-b3e9-4d28-85f5-1fafaa75a5f7" />


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

<img width="1581" alt="cut-c1-c3file11" src="https://github.com/user-attachments/assets/c9eb7e71-45de-4bd6-9278-365d08c6e2b8" />



cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT

<img width="1669" alt="cut-d-f2file22" src="https://github.com/user-attachments/assets/7afe8216-1944-46b9-9635-2dd85aae43fe" />


cat < newfile 
```
Hello world<img width="1669" alt="grepHello" src="https://github.com/user-attachments/assets/fef2de9e-6bfb-4391-a1d5-cc0904f729e7" />

hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT



grep hello newfile 
## OUTPUT

<img width="1669" alt="grep_hello" src="https://github.com/user-attachments/assets/319c6421-5e86-4320-afd4-ea2103238699" />



grep -v hello newfile 
## OUTPUT
<img width="1669" alt="grep-v" src="https://github.com/user-attachments/assets/ec6ed5e0-55af-45f8-9982-1eebc3d7af76" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="1781" alt="catgrepi" src="https://github.com/user-attachments/assets/f9405e85-846c-4831-814a-00285fe4b652" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1827" alt="catgrepic" src="https://github.com/user-attachments/assets/34a57c5f-a694-4a0f-801d-9c22d7d156cf" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="1108" alt="grep newworld" src="https://github.com/user-attachments/assets/b0e4f681-ead7-4eba-a802-11660d16b400" />


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

<img width="1172" alt="egrep1" src="https://github.com/user-attachments/assets/aedfcc9c-abb0-4d1a-a4c3-1477d0525029" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

OUTPUT


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1191" alt="egrep3" src="https://github.com/user-attachments/assets/f27c1d05-b402-468b-a2ca-347aa4ff8255" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="1191" alt="egrep4" src="https://github.com/user-attachments/assets/0d6c6276-ee60-4de7-83cd-4688260dc663" />


egrep '(world$)' newfile 
## OUTPUT

<img width="1191" alt="egrep5" src="https://github.com/user-attachments/assets/98033db8-f551-492c-ad6f-cfdc82ffedfb" />


egrep '(World$)' newfile 
## OUTPUT
<img width="1191" alt="egrep6" src="https://github.com/user-attachments/assets/454d2b49-23cc-43d4-a8ec-ad48060fb87f" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1191" alt="egrep7" src="https://github.com/user-attachments/assets/822a81b7-c4f3-4d12-9391-a096334b8d95" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="1191" alt="egrep8" src="https://github.com/user-attachments/assets/a667acf1-6651-4cd3-a5a8-06858c304a67" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1191" alt="egrep9" src="https://github.com/user-attachments/assets/5aac9c53-1e62-4c3d-ab97-5c6f6e6167da" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1191" alt="egrep10" src="https://github.com/user-attachments/assets/8fb733cf-b6fe-4d3c-9fad-3ea8b087f0ea" />

egrep l{2} newfile
## OUTPUT

<img width="1191" alt="egrep11" src="https://github.com/user-attachments/assets/14013d7c-dd09-417a-8be9-fd229f168a81" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1191" alt="egrep12" src="https://github.com/user-attachments/assets/19d4c022-dc90-4cc2-b42d-788023565113" />

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

<img width="1191" alt="sed1" src="https://github.com/user-attachments/assets/0e0e4058-5f4b-482d-8c68-672e6bf14a05" />


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="sed3" src="https://github.com/user-attachments/assets/2f5ad98d-cd0d-4bb8-a698-ef7d042470a1" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="sed4" src="https://github.com/user-attachments/assets/25071c07-18a5-4992-a5d4-3f3167f99885" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1191" alt="sed5" src="https://github.com/user-attachments/assets/3da175d9-912e-4b92-aad6-2639ef32090d" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1191" alt="sed6" src="https://github.com/user-attachments/assets/c0b9a8a7-8e07-473e-9dc1-dcba851703d6" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1191" alt="sed7" src="https://github.com/user-attachments/assets/6337db4e-f065-4035-8c88-ad11f90025b8" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1191" alt="sed8" src="https://github.com/user-attachments/assets/dc862b79-3c8e-458a-a830-cb58e823916d" />


seq 10 
## OUTPUT
<img width="1191" alt="seq1" src="https://github.com/user-attachments/assets/857b0959-92ba-4b0a-93da-d220a5698d56" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1191" alt="seq2" src="https://github.com/user-attachments/assets/8962928c-10cb-41ec-828c-b8f7dd7c0f25" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1191" alt="seq3" src="https://github.com/user-attachments/assets/2cfa490d-67ef-41bf-a6af-39fc1c6a6e3b" />


seq 3 | sed '2a hello'
## OUTPUT



seq 2 | sed '2i hello'
## OUTPUT
https://github.com/heyitsgautham/OS-Linux-commands-Shell-script/blob/main/img/seq5.png

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="1191" alt="seq6" src="https://github.com/user-attachments/assets/bff1a3f1-4aed-47a9-9134-6537f6fe024d" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1191" alt="seq7" src="https://github.com/user-attachments/assets/9416e7b8-173b-459b-bfce-ee0331b4f36c" />


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
<img width="1191" alt="sort" src="https://github.com/user-attachments/assets/7bbb670b-0228-49ee-82e8-035f228b9aaf" />


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
<img width="1191" alt="uniq" src="https://github.com/user-attachments/assets/35b60b72-57a9-430f-be59-728365c57faf" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
<img width="1220" alt="catfile23" src="https://github.com/user-attachments/assets/e2714edc-d6d3-49fd-b6c2-22203b3bd171" />

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
<img width="1150" alt="caturl1" src="https://github.com/user-attachments/assets/f87b9eca-997d-4f5d-a8c2-114a036843de" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1262" alt="caturl2" src="https://github.com/user-attachments/assets/36c25d8f-1891-4c0f-af9c-1a9b0972e91f" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="983" alt="tar1" src="https://github.com/user-attachments/assets/648b6597-8916-4361-92e4-4186531dded6" />


mkdir backupdir
 
mv backup.tar backupdir

## OUTPUT

<img width="983" alt="mv1" src="https://github.com/user-attachments/assets/6ed5f7f3-589b-4b2d-bfdc-7d59135862f8" />



cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="983" alt="tar2" src="https://github.com/user-attachments/assets/c32abae5-3c8e-45e9-8663-bc273b5c2a8c" />


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
<img width="983" alt="ls1" src="https://github.com/user-attachments/assets/4d9c7451-3073-4d60-9215-fc636ef4419f" />

 
gunzip backup.tar.gz
## OUTPUT

 <img width="1112" alt="ls2" src="https://github.com/user-attachments/assets/7e25f8ab-f026-43a9-a886-bc437a081696" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="1303" alt="echo1" src="https://github.com/user-attachments/assets/65d2fa2d-1a96-47b5-af84-919bee11fc57" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1303" alt="catherecheck" src="https://github.com/user-attachments/assets/169a01f4-6c51-41f1-a8b5-02277102f952" />



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

 <img width="1303" alt="catscriptcheck" src="https://github.com/user-attachments/assets/de1fc9d8-612e-45cf-9c6b-c112a3912dd7" />

ls file1
## OUTPUT

<img width="1303" alt="ls_1" src="https://github.com/user-attachments/assets/a76dfeca-0b1b-4039-aada-432121b29535" />

echo $?
## OUTPUT 
<img width="1303" alt="echo_1" src="https://github.com/user-attachments/assets/b15bb2cd-e445-4c52-99cf-f93405b81c15" />


./onebash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="1303" alt="echo_3" src="https://github.com/user-attachments/assets/bfe93a5d-6e0d-4f63-95c7-930f76bc529f" />
abcd
echo $?
 ## OUTPUT

<img width="1303" alt="echo_2" src="https://github.com/user-attachments/assets/df8e580c-2b29-4039-b96e-9a8fe4eabd76" />

 
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

<img width="1303" alt="cat_Strcmp" src="https://github.com/user-attachments/assets/c3683e79-8078-4edb-94e1-5d67ad0a7c45" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="1303" alt="strcmp" src="https://github.com/user-attachments/assets/84e276b4-e1c0-4636-bc10-9d75e0914a21" />


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

<img width="1303" alt="psswdperm" src="https://github.com/user-attachments/assets/132f9a87-702c-4c13-b46e-2298fe82b751" />

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

<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/38db4b95-6ca9-4fca-bc0e-d061b42816a5" />


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

<img width="1303" alt="iftest" src="https://github.com/user-attachments/assets/860c4b6b-e5fa-40a0-918b-1b816f86406a" />

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

<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/5bf4e6f9-8c32-4bcd-9af0-e939b0c9dc11" />


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

<img width="1303" alt="elifcheck" src="https://github.com/user-attachments/assets/2e26ca01-c304-4bf5-a7aa-5f3887984db3" />


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

<img width="1303" alt="ifcompound" src="https://github.com/user-attachments/assets/71935130-5846-4686-ac6e-9f164ed22833" />

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

<img width="1303" alt="casecheck" src="https://github.com/user-attachments/assets/669978b4-e70a-449d-a79c-0c034e3c907f" />

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

 
 <img width="1303" alt="whiletest" src="https://github.com/user-attachments/assets/8cd34b81-86e4-4b3f-974f-0a40b83146bb" />

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
$ chmod 755 untiltest.sh $ ./untiltest.sh
## OUTPUT



 
 <img width="1303" alt="untiltest" src="https://github.com/user-attachments/assets/7f7dbff8-a4c4-4a7b-986e-7573a1635643" />

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh $ ./forin1.sh
## OUTPUT

 <img width="1303" alt="forin1" src="https://github.com/user-attachments/assets/9c129c99-533a-42b5-a3d9-71f2a29d9d6d" />

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```

 
$ chmod 755 forin2.sh  $ ./forin2.sh
  ## OUTPUT

  <img width="1303" alt="forin2" src="https://github.com/user-attachments/assets/199392bd-6731-416f-bc26-34283b61ef64" />


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
 ## OUTPUT
<img width="1303" alt="forin3" src="https://github.com/user-attachments/assets/fbe2270c-0e9d-405c-91d6-55903d4841ae" />

 
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
<img width="1303" alt="forneseted1" src="https://github.com/user-attachments/assets/c34e21ad-962a-4661-8ffa-aa7699362b4a" />

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
<img width="1303" alt="forneseted1" src="https://github.com/user-attachments/assets/308e1234-d133-4c67-8ede-a507bdd1f733" />

 
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
 <img width="1303" alt="forcontinue" src="https://github.com/user-attachments/assets/f54724ce-8b41-4d63-a8d2-532b6f0e9024" />

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
<img width="1303" alt="exread" src="https://github.com/user-attachments/assets/0b3aab77-d947-47bd-a262-0bf1070d8b72" />


 cat exread1.sh
```bash
#!/bin/bas
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
 ## OUTPUT
 <img width="1303" alt="funcex" src="https://github.com/user-attachments/assets/932db69c-ac61-4313-aa88-8d7d7972fd9b" />

 ./funcex.sh 1 2

  ## OUTPUT
  <img width="1303" alt="funcex123" src="https://github.com/user-attachments/assets/385b8333-9211-4e7e-94cf-de3f2a6aa003" />

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
  ## OUTPUT
  <img width="1303" alt="argshift1" src="https://github.com/user-attachments/assets/2929975b-d7b2-4e9a-89da-662f88533ccd" />

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
<img width="1303" alt="argshift1" src="https://github.com/user-attachments/assets/0176013b-0759-491c-8b0f-595a3a099069" />


$ ./argshift.sh 1 2 3
 ## OUTPUT
 <img width="1303" alt="argshift3" src="https://github.com/user-attachments/assets/d27bdb90-c649-4a47-9219-2d85e7d2f939" />

 
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
  ## OUTPUT
  
 <img width="1303" alt="argshift3" src="https://github.com/user-attachments/assets/a0b36df1-6346-416c-8abb-585ce0df811d" />

cat > nc.awk
 ## OUTPUT
 
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
 ## OUTPUT
 
<img width="1303" alt="awk" src="https://github.com/user-attachments/assets/1f8fa621-2851-4716-9507-4bb8978de7ad" />

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
<img width="1303" alt="awk" src="https://github.com/user-attachments/assets/66e72e4f-9a7a-47dd-8ee1-eefe7ef85d37" />


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
