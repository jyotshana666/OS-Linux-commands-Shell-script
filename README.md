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
<img width="270" height="147" alt="1" src="https://github.com/user-attachments/assets/500b5290-f933-4c07-afb8-a4e8a5d04297" />




cat < file2
## OUTPUT
<img width="262" height="173" alt="2" src="https://github.com/user-attachments/assets/6891b945-f5a6-4636-9d77-060b4c0dd744" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="277" height="52" alt="3" src="https://github.com/user-attachments/assets/f9f0c91d-45aa-449e-a7c5-4e0437bf6360" />

 
comm file1 file2
 ## OUTPUT
 <img width="391" height="302" alt="5" src="https://github.com/user-attachments/assets/0fef1f19-f92b-4f59-bc09-f24eb05ba785" />


 
diff file1 file2
## OUTPUT
<img width="317" height="272" alt="4" src="https://github.com/user-attachments/assets/2decb68c-481f-467d-97d6-a6c478b97a52" />


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
<img width="286" height="103" alt="6" src="https://github.com/user-attachments/assets/d9c5b705-a9aa-453f-8b78-a970a5e2210c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="297" height="127" alt="7" src="https://github.com/user-attachments/assets/30aeecae-ca69-4dfd-adb4-90518f3d410a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="300" height="123" alt="8" src="https://github.com/user-attachments/assets/43511f9f-b306-4bbc-9b90-90ac010025da" />


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
<img width="265" height="81" alt="9" src="https://github.com/user-attachments/assets/31da7f68-0a16-4b1a-bc80-cd5dd1e4266e" />




grep hello newfile 
## OUTPUT
<img width="267" height="73" alt="10" src="https://github.com/user-attachments/assets/3ec906f6-558c-4684-8540-9376d02095a9" />




grep -v hello newfile 
## OUTPUT
<img width="292" height="77" alt="11" src="https://github.com/user-attachments/assets/3d13c6a7-1d97-42e2-9c2f-c4c7b8b75dcd" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="363" height="102" alt="12" src="https://github.com/user-attachments/assets/1b75a938-b03d-4a62-9142-6005ce3b3055" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="392" height="76" alt="13" src="https://github.com/user-attachments/assets/36e81c30-bb05-43c4-a203-b67c2f0bcc5d" />




grep -R ubuntu /etc
## OUTPUT
<img width="808" height="370" alt="14" src="https://github.com/user-attachments/assets/571e029c-eb10-4969-a9b8-f1dce342a548" />



grep -w -n world newfile   
## OUTPUT
<img width="320" height="105" alt="15" src="https://github.com/user-attachments/assets/ae462c18-e664-4e38-ae13-a6da7e01340d" />


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
<img width="398" height="102" alt="image" src="https://github.com/user-attachments/assets/8c432a03-fc15-4852-9cdc-39bf0ac13635" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="366" height="105" alt="image" src="https://github.com/user-attachments/assets/3ebe37eb-3325-4763-a364-4b858c2e6bce" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="408" height="103" alt="image" src="https://github.com/user-attachments/assets/5c10837a-16cf-40e9-81ab-d84cb0f41ac2" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="338" height="81" alt="image" src="https://github.com/user-attachments/assets/4384cabb-8c28-4d6f-b834-2e027b63971e" />



egrep '(world$)' newfile 
## OUTPUT
<img width="337" height="103" alt="image" src="https://github.com/user-attachments/assets/fed15abc-b183-4241-a524-2963172003bf" />



egrep '(World$)' newfile 
## OUTPUT
<img width="340" height="81" alt="image" src="https://github.com/user-attachments/assets/6a136ac7-3efe-48af-9f1e-f64208993163" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="381" height="132" alt="image" src="https://github.com/user-attachments/assets/1815259c-67af-410e-b4a0-74eeb2522a2b" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="297" height="76" alt="image" src="https://github.com/user-attachments/assets/8e8a3289-91dc-4f73-a30b-00e729dbaf49" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="388" height="85" alt="image" src="https://github.com/user-attachments/assets/2d6be2c8-c09f-49e7-a5a1-757b89cb8323" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="373" height="77" alt="image" src="https://github.com/user-attachments/assets/a0b63017-ad12-46d3-a0c0-5556804f671a" />


egrep l{2} newfile
## OUTPUT
<img width="287" height="108" alt="image" src="https://github.com/user-attachments/assets/cb45dbc9-b173-42fd-8f0a-d76738b8089e" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="347" height="125" alt="image" src="https://github.com/user-attachments/assets/09a2f5a5-9587-46db-ab40-75e2d465168a" />


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
<img width="307" height="77" alt="image" src="https://github.com/user-attachments/assets/c91d69f4-66f1-47a2-8fd9-da8b61746324" />



sed -n -e '$p' file23
## OUTPUT
<img width="322" height="77" alt="image" src="https://github.com/user-attachments/assets/54b1fb8e-f401-48f5-8362-fa53ae62bff1" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="380" height="260" alt="image" src="https://github.com/user-attachments/assets/8981720a-fd7a-40a9-987b-5873d25a0ff6" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="412" height="252" alt="image" src="https://github.com/user-attachments/assets/7de96e7c-898f-4cd1-8114-538718e543cf" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="386" height="252" alt="image" src="https://github.com/user-attachments/assets/a927ee6b-6fcf-44e4-b3bb-866fe973621e" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="337" height="181" alt="image" src="https://github.com/user-attachments/assets/b8cc874e-bc9e-475a-9d10-f1ad6e29b80b" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="367" height="123" alt="image" src="https://github.com/user-attachments/assets/2c9c88e8-4e7e-4210-bfad-b7e09176add2" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="410" height="107" alt="image" src="https://github.com/user-attachments/assets/984b50ef-9e85-4973-94d6-7c5a674e50ed" />



seq 10 
## OUTPUT
<img width="280" height="302" alt="image" src="https://github.com/user-attachments/assets/89323600-1d2e-4648-a0bf-7d0243c83887" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="302" height="135" alt="image" src="https://github.com/user-attachments/assets/0c00812e-618d-4f30-bec5-7936df88049d" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="312" height="132" alt="image" src="https://github.com/user-attachments/assets/3e6b26e9-28dc-4260-a6c7-d856cfe600c4" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="300" height="156" alt="image" src="https://github.com/user-attachments/assets/db63ac68-07b0-4796-be19-53beed4d4985" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="301" height="126" alt="image" src="https://github.com/user-attachments/assets/1f3a5334-1718-434c-b023-7d58f0669006" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="337" height="135" alt="image" src="https://github.com/user-attachments/assets/f11ac523-d49a-45a2-bbe9-8532f3a64700" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="415" height="128" alt="image" src="https://github.com/user-attachments/assets/94b4e266-d43d-488c-bc87-bb8b4ad58284" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="406" height="135" alt="image" src="https://github.com/user-attachments/assets/3fe7836f-f25a-4c25-a695-c629ca1f0417" />


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
<img width="337" height="182" alt="image" src="https://github.com/user-attachments/assets/a91a9c8c-0195-4c92-8255-de47270b48d3" />


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
<img width="338" height="177" alt="image" src="https://github.com/user-attachments/assets/2d7d0d5f-4629-42b8-b823-83e5b61915cc" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="457" height="252" alt="image" src="https://github.com/user-attachments/assets/084dbbbe-ade3-4388-b170-4430daeaa8d0" />

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
<img width="352" height="128" alt="image" src="https://github.com/user-attachments/assets/aee69de0-8bf5-4860-8f59-5a1662d5aa7e" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="470" height="128" alt="image" src="https://github.com/user-attachments/assets/43c43d97-2f51-4b99-bccb-b2b14687b538" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="312" height="253" alt="image" src="https://github.com/user-attachments/assets/f8beced9-1631-428f-ae9e-34ed9509b717" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="722" height="552" alt="image" src="https://github.com/user-attachments/assets/363915bf-7465-4862-8b2b-8825e624efd3" />

tar -xvf backup.tar
## OUTPUT
<img width="416" height="253" alt="image" src="https://github.com/user-attachments/assets/62e2bac5-cebf-401c-ba94-2e0e3cdfa5c9" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="410" height="81" alt="image" src="https://github.com/user-attachments/assets/0872643d-2044-470c-b821-d38091789502" />

gunzip backup.tar.gz
## OUTPUT
<img width="647" height="157" alt="image" src="https://github.com/user-attachments/assets/409604c1-b225-46a3-8f26-90c855e4880d" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="472" height="232" alt="image" src="https://github.com/user-attachments/assets/b891da4f-6013-4239-b34d-ca9ba3a1d162" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="421" height="317" alt="image" src="https://github.com/user-attachments/assets/59b7a742-5e64-4afe-ab6e-4790a3bf5546" />


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
<img width="490" height="775" alt="image" src="https://github.com/user-attachments/assets/4654777b-6335-46c2-9507-cf24bc6c12ed" />

 
ls file1
## OUTPUT
<img width="297" height="77" alt="image" src="https://github.com/user-attachments/assets/2715a3ea-6f7e-4dce-a218-e32d46085faa" />

echo $?
## OUTPUT 
<img width="267" height="81" alt="image" src="https://github.com/user-attachments/assets/003879fc-d174-43cf-8d1b-e4342f24515d" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="335" height="155" alt="image" src="https://github.com/user-attachments/assets/5852a517-af18-4d68-978b-4809e7cc0aca" />


 
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

<img width="363" height="277" alt="image" src="https://github.com/user-attachments/assets/9b2089f1-628c-4cae-9854-31ab00541e89" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="620" height="151" alt="image" src="https://github.com/user-attachments/assets/4e939222-b1ad-444d-91bf-c0fa9d845404" />



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
<img width="612" height="303" alt="image" src="https://github.com/user-attachments/assets/a5965dac-a477-4f5b-ad42-ca4667df33fb" />

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
<img width="530" height="582" alt="image" src="https://github.com/user-attachments/assets/1883a8ba-3038-4f67-910f-533b1efb5350" />



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
<img width="530" height="582" alt="Screenshot 2025-08-18 131157" src="https://github.com/user-attachments/assets/3d0aa2af-53cd-4248-a587-f18e9dec045d" />


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
<img width="517" height="680" alt="image" src="https://github.com/user-attachments/assets/fc05d88c-cff5-47bb-9193-361ff6011740" />

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
<img width="581" height="347" alt="image" src="https://github.com/user-attachments/assets/139a07bd-6224-4ca4-92bb-791af55ad473" />

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
 <img width="612" height="598" alt="image" src="https://github.com/user-attachments/assets/cd4ee855-d48e-4825-9307-7fc745ae7862" />

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
<img width="343" height="610" alt="image" src="https://github.com/user-attachments/assets/6432cc9b-2986-4ee8-a439-c80e0e9bd337" />

 
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
 <img width="306" height="452" alt="image" src="https://github.com/user-attachments/assets/c77dbf53-eac6-420c-b0e8-0307f0d80e87" />

 
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
<img width="655" height="456" alt="image" src="https://github.com/user-attachments/assets/b06f5854-1e34-4465-a145-d68acf689314" />

 
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
<img width="576" height="456" alt="image" src="https://github.com/user-attachments/assets/af123c85-c075-449a-8a66-cb9fe4230bf0" />

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
<img width="572" height="458" alt="image" src="https://github.com/user-attachments/assets/578b0c5e-67a7-4bb4-8832-4cf56c7c46cf" />

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
## OUTPUT
<img width="353" height="502" alt="image" src="https://github.com/user-attachments/assets/e7cc1615-98f7-4ccf-b9c2-ee8db36ca39e" />

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="343" height="450" alt="image" src="https://github.com/user-attachments/assets/4cc623cc-7d35-4daf-8f43-fd5b8fa3f1e9" />


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
<img width="362" height="435" alt="image" src="https://github.com/user-attachments/assets/ab815431-d886-4e24-a34f-05179a1c9fd5" />

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
<img width="401" height="432" alt="image" src="https://github.com/user-attachments/assets/c01b2e37-9b22-4b14-a35b-84df4749dac4" />

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
<img width="360" height="701" alt="image" src="https://github.com/user-attachments/assets/94048ada-f4c3-4632-9e13-c1f04167b3e7" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## OUTPUT
<img width="361" height="505" alt="image" src="https://github.com/user-attachments/assets/11800f6c-c3e4-4851-96a3-9915b2e18fe3" />

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
<img width="553" height="558" alt="image" src="https://github.com/user-attachments/assets/f12ce289-f938-40ae-9870-fb589a5fe0c8" />

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
<img width="460" height="330" alt="image" src="https://github.com/user-attachments/assets/348dddba-1869-4731-a833-9d733fc71b30" />


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
<img width="446" height="330" alt="image" src="https://github.com/user-attachments/assets/d3dc8b42-e6c4-46a3-a6eb-442575021f32" />




 
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
./funcex.sh 
## OUTPUT
<img width="577" height="526" alt="image" src="https://github.com/user-attachments/assets/ac94d21f-b743-4c89-9d75-5a851f0e796c" />


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="302" height="357" alt="image" src="https://github.com/user-attachments/assets/1f76e1b3-21a6-40f0-8fa3-5aa65f48a7ee" />


 
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
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="396" height="483" alt="image" src="https://github.com/user-attachments/assets/a54ec90f-4589-4f98-892e-a7222723458e" />


 
cat argshift2.sh
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
 ./argshift2.sh 1 2 3
 <img width="338" height="678" alt="image" src="https://github.com/user-attachments/assets/415d0981-3964-4a92-9a95-e27f6f5cf993" />

 
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
 <img width="368" height="380" alt="image" src="https://github.com/user-attachments/assets/2d29e341-9440-41fa-beaa-94a5f96738b1" />

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
<img width="340" height="180" alt="image" src="https://github.com/user-attachments/assets/78b54a02-111c-4e80-85b8-0db16b2afc84" />


# RESULT:
The Commands are executed successfully.
