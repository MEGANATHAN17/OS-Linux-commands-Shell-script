# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise

```
DEVELOPED BY:
NAME: MEGANATHAN R
REG NO: 21222430156
```


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
<img width="390" height="133" alt="image" src="https://github.com/user-attachments/assets/d69bbace-ed61-414f-a08b-7525e4a4fe7c" />




cat < file2
## OUTPUT
<img width="393" height="74" alt="image" src="https://github.com/user-attachments/assets/013d4bb5-664c-4a47-a72a-b66d7360f951" />



# Comparing Files
cmp file1 file2
## OUTPUT-
<img width="372" height="87" alt="image" src="https://github.com/user-attachments/assets/5ec67841-bcb1-4067-8b73-e342a61e284f" />

 
comm file1 file2
 ## OUTPUT
 
<img width="296" height="275" alt="image" src="https://github.com/user-attachments/assets/cebef82a-3a9f-4882-8c3b-c21beec08737" />

diff file1 file2
## OUTPUT
<img width="390" height="110" alt="image" src="https://github.com/user-attachments/assets/04074b64-f8c2-4ebc-a030-e7d0d322425d" />


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
<img width="391" height="105" alt="image" src="https://github.com/user-attachments/assets/b4ee1885-62ba-4c2d-88fa-c86f809b6fd2" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="380" height="106" alt="image" src="https://github.com/user-attachments/assets/0f26bb36-f75e-4c7c-b44d-8cad90b4284c" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="433" height="94" alt="image" src="https://github.com/user-attachments/assets/e2132d1f-8984-4d81-96cd-139fb6bb8a58" />



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
<img width="460" height="73" alt="image" src="https://github.com/user-attachments/assets/075b5098-fab5-451c-83a7-5385571ff8e2" />






grep hello newfile 
## OUTPUT
<img width="384" height="78" alt="image" src="https://github.com/user-attachments/assets/86d0cd10-2af5-4b9d-92e4-bfdb7c5028ba" />





grep -v hello newfile 
## OUTPUT
<img width="423" height="79" alt="image" src="https://github.com/user-attachments/assets/7f6f8d22-4c46-487b-87ef-df04ee1713fb" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="445" height="81" alt="image" src="https://github.com/user-attachments/assets/8a7849ac-e83d-48f7-9e85-2e7d1bb896d5" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="470" height="97" alt="image" src="https://github.com/user-attachments/assets/5c8eea36-d3e0-4108-bdf8-713ada5b18b0" />




grep -R ubuntu /etc
## OUTPUT

<img width="924" height="782" alt="image" src="https://github.com/user-attachments/assets/569eda21-6670-4f14-8691-6272a6b3d888" />


grep -w -n world newfile   
## OUTPUT
<img width="415" height="105" alt="image" src="https://github.com/user-attachments/assets/ee7f4636-2168-4fae-a3a3-0fc02189e5e0" />



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
## 
<img width="475" height="134" alt="image" src="https://github.com/user-attachments/assets/71adc98e-97b1-4197-afe4-91561de6c532" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="415" height="98" alt="image" src="https://github.com/user-attachments/assets/75c34ea7-b4a1-4fd9-a066-33e55f134001" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="502" height="115" alt="image" src="https://github.com/user-attachments/assets/6c36cc33-994d-44b8-92b5-b8c84400b640" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="410" height="79" alt="image" src="https://github.com/user-attachments/assets/9f53c691-91ab-4c17-b3f1-d203e74e86e0" />




egrep '(world$)' newfile 
## OUTPUT
<img width="359" height="100" alt="image" src="https://github.com/user-attachments/assets/6e45a5b2-822a-4dfc-8ac3-28f04b4bd475" />



egrep '(World$)' newfile 
## OUTPUT
<img width="425" height="113" alt="image" src="https://github.com/user-attachments/assets/30debbfc-9f2f-4b3f-935e-a9000c6489de" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="393" height="114" alt="image" src="https://github.com/user-attachments/assets/9880086f-f145-4397-b335-35a01be0af5e" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="396" height="73" alt="image" src="https://github.com/user-attachments/assets/da65abba-3de4-4cc1-b0fe-0207c737c5c3" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="546" height="78" alt="image" src="https://github.com/user-attachments/assets/476154ec-20fd-48b0-baac-3782a6077805" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="546" height="78" alt="image" src="https://github.com/user-attachments/assets/5a3d2476-78e4-4d3a-b17c-640068be43fb" />


egrep l{2} newfile
## OUTPUT
<img width="451" height="110" alt="image" src="https://github.com/user-attachments/assets/a6a62c8e-0c84-42b6-87fe-472dd60ef526" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="479" height="105" alt="image" src="https://github.com/user-attachments/assets/216506d4-61b1-46a7-91eb-af4c7ee7c267" />


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
<img width="422" height="80" alt="image" src="https://github.com/user-attachments/assets/ad6e309c-ae05-4f1b-874b-a687a0ec15fb" />



sed -n -e '$p' file23
## OUTPUT
<img width="382" height="75" alt="image" src="https://github.com/user-attachments/assets/27fa7108-4fbf-4e53-a0da-779f0442493f" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="490" height="228" alt="image" src="https://github.com/user-attachments/assets/076dbb81-ba4e-4c48-8690-c25b9d1a65a8" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="451" height="234" alt="image" src="https://github.com/user-attachments/assets/1b6f52c1-6d57-485f-ab82-31c5b76c0370" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="407" height="234" alt="image" src="https://github.com/user-attachments/assets/9d896058-9644-439f-a0dc-86a105144a3e" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="409" height="173" alt="image" src="https://github.com/user-attachments/assets/5656225f-880a-4211-b35d-9d4a4582855b" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="406" height="120" alt="image" src="https://github.com/user-attachments/assets/3948c3db-fd0e-4470-99a1-bed5933f26f6" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="550" height="117" alt="image" src="https://github.com/user-attachments/assets/c6bbc632-daed-4d35-8c97-6e8332d85b68" />


seq 10 
## OUTPUT
<img width="434" height="303" alt="image" src="https://github.com/user-attachments/assets/77475164-02d5-4e10-aea0-b4c9152e58d5" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="363" height="125" alt="image" src="https://github.com/user-attachments/assets/fa9cfcf8-6a38-40fd-8dbf-9aac4893ce78" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="409" height="129" alt="image" src="https://github.com/user-attachments/assets/f1aca076-baac-4508-9e06-988088f9a864" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="399" height="149" alt="image" src="https://github.com/user-attachments/assets/4982f528-f71b-4d42-b01d-588ffe4c837e" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="416" height="123" alt="image" src="https://github.com/user-attachments/assets/baa0b811-ed42-4a87-b810-972e4a1eac8e" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="376" height="127" alt="image" src="https://github.com/user-attachments/assets/e75978dc-ca01-414c-a58f-046c44d24cdc" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="407" height="139" alt="image" src="https://github.com/user-attachments/assets/08d0c81f-36e1-46fd-a9eb-317edf059075" />



sed -n '2,4{s/$/*/;p}' file23
<img width="423" height="122" alt="image" src="https://github.com/user-attachments/assets/d99bdf7d-2ecd-4180-9ef7-88d3e2b56569" />


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
<img width="443" height="160" alt="image" src="https://github.com/user-attachments/assets/069b76f4-5d3e-4220-a58c-33a576006bc8" />


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
<img width="473" height="176" alt="image" src="https://github.com/user-attachments/assets/8d03ef1b-07c0-43dd-a4c4-123aa95e2ad3" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="452" height="231" alt="image" src="https://github.com/user-attachments/assets/15e9d019-7df8-498c-9727-ff9ef467177d" />


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
<img width="420" height="138" alt="image" src="https://github.com/user-attachments/assets/4aff68bd-c927-4d64-84ce-12ee0d02108c" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="555" height="124" alt="image" src="https://github.com/user-attachments/assets/a8ebf878-9f66-4f55-b81d-b90ee7e30252" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="528" height="570" alt="image" src="https://github.com/user-attachments/assets/3e0f4f6c-c8f3-4bfc-b09e-773e108906a0" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
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
<img width="566" height="182" alt="image" src="https://github.com/user-attachments/assets/be712e14-1a02-4b39-ab8c-3e334c302fbd" />


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="506" height="137" alt="image" src="https://github.com/user-attachments/assets/0295a2c0-816b-4641-b0a8-229dccd6ffa9" />


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
<img width="333" height="425" alt="image" src="https://github.com/user-attachments/assets/9c54bc7a-18df-4cc1-909a-58a9bc0939b9" />

 
ls file1
## OUTPUT
<img width="302" height="81" alt="image" src="https://github.com/user-attachments/assets/529f714a-c467-46a0-bb70-9d7bd2f3cfa5" />

echo $?
## OUTPUT 
<img width="315" height="78" alt="image" src="https://github.com/user-attachments/assets/35ac749c-6095-49a7-84d3-6408695545fa" />

./one
bash: ./one: Permission denied
## OUTPUT
  <img width="333" height="78" alt="image" src="https://github.com/user-attachments/assets/00b29bed-ce39-4a0c-bde2-dcc2ba1c97d6" />


echo $?
## OUTPUT 
<img width="364" height="73" alt="image" src="https://github.com/user-attachments/assets/d13ab30a-e575-477b-8fea-fc40f8de8738" />

abcd
## OUTPUT 
<img width="372" height="79" alt="image" src="https://github.com/user-attachments/assets/1000b06d-5f96-4f96-a91c-44bdd464a2d7" />

 
echo $?
 ## OUTPUT
<img width="344" height="75" alt="image" src="https://github.com/user-attachments/assets/6ee291a0-16b0-44da-ae60-2705bc010b24" />

 
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
<img width="361" height="253" alt="image" src="https://github.com/user-attachments/assets/fed16091-f7f7-45ed-844f-93b1bde98449" />



chmod 755 strcomp.sh

./strcomp.sh 
## OUTPUT
<img width="351" height="403" alt="image" src="https://github.com/user-attachments/assets/b7fef264-102e-4817-a2b1-32394a6c44c2" />


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
<img width="625" height="281" alt="image" src="https://github.com/user-attachments/assets/aa0081d0-0207-410a-aae5-66fce997fcce" />

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
<img width="589" height="714" alt="image" src="https://github.com/user-attachments/assets/4dde118e-4457-459c-b3c2-071be9fe717f" />



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
<img width="561" height="626" alt="image" src="https://github.com/user-attachments/assets/b48c065b-2fc6-44bd-a609-61c863f88b70" />

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
<img width="545" height="708" alt="image" src="https://github.com/user-attachments/assets/5e9da924-8a7a-4bc0-bd2e-af25fc9536ee" />

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
<img width="615" height="536" alt="image" src="https://github.com/user-attachments/assets/8a170810-8057-4357-817d-8cd4f01f37d1" />


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
<img width="561" height="365" alt="image" src="https://github.com/user-attachments/assets/7072d5bf-c266-4e53-b214-97b6c6f4f72a" />

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
<img width="619" height="488" alt="image" src="https://github.com/user-attachments/assets/c0e62979-98e9-4c4c-9762-703f5deb3659" />

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
<img width="486" height="575" alt="image" src="https://github.com/user-attachments/assets/4c71a934-1846-406e-84c3-734c4b15fe73" />

 
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
 $ ./untiltest.sh
 ## OUTPUT
 <img width="546" height="432" alt="image" src="https://github.com/user-attachments/assets/e469df2d-8a00-428b-8b13-a1a838bc24a1" />

 
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
 $ ./forin1.sh
 ## OUTPUT
 
 <img width="685" height="430" alt="image" src="https://github.com/user-attachments/assets/2c66483e-2ff4-498a-a867-a8cc6ef40e34" />

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
 <img width="595" height="357" alt="image" src="https://github.com/user-attachments/assets/08091f48-6785-4e27-bfef-87cdff8fc105" />

 
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
<img width="589" height="352" alt="image" src="https://github.com/user-attachments/assets/f39e9178-d6ee-4ee0-9e5e-a99643226589" />

 
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
 <img width="547" height="430" alt="image" src="https://github.com/user-attachments/assets/608da47c-d987-4853-8735-3de45df0f563" />

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
<img width="685" height="430" alt="image" src="https://github.com/user-attachments/assets/1241e664-9b78-4cc4-9c2f-f0b9afb100d9" />

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
<img width="365" height="403" alt="image" src="https://github.com/user-attachments/assets/e5f65799-d505-49ab-9e33-eab4ca896518" />

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
<img width="542" height="405" alt="image" src="https://github.com/user-attachments/assets/012a719d-193b-41ca-9453-a89650763c8d" />

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
<img width="390" height="684" alt="image" src="https://github.com/user-attachments/assets/b1a896ec-ade5-4b2b-b4fa-f87ac3636941" />

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
 <img width="421" height="431" alt="image" src="https://github.com/user-attachments/assets/00df8f95-550f-40c7-b08c-5061e2798f54" />

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
 <img width="498" height="490" alt="image" src="https://github.com/user-attachments/assets/6d0308bb-00a5-4c79-961c-64b977790fd9" />

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
<img width="558" height="311" alt="image" src="https://github.com/user-attachments/assets/f526bf83-86ab-4a8c-b57e-ccb7b5fbd565" />


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
<img width="589" height="163" alt="image" src="https://github.com/user-attachments/assets/45a20b25-b53e-4a86-a1fd-91237f70ca10" />

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
 
 ./funcex.sh 1 2
## OUTPUT
<img width="570" height="541" alt="image" src="https://github.com/user-attachments/assets/10559ce2-a928-4808-af92-4506e5ada7d4" />

 
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
<img width="381" height="355" alt="image" src="https://github.com/user-attachments/assets/fa103291-3d64-4bb9-b29f-7c853ab3bfbf" />

 
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
 <img width="387" height="371" alt="image" src="https://github.com/user-attachments/assets/e56f2adc-c792-41ba-aa74-66cfbbd4014e" />

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

 ./argshift.sh 1 2 3
 ## OUTPUT
 <img width="593" height="634" alt="image" src="https://github.com/user-attachments/assets/1471bc05-efdd-4d92-93ea-382da3fbcf03" />

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
 <img width="447" height="658" alt="image" src="https://github.com/user-attachments/assets/ac487cf7-64bf-43e3-990d-62af77e5c652" />

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
<img width="593" height="780" alt="image" src="https://github.com/user-attachments/assets/b7bb5af9-8038-4407-bfca-f25a7ba61740" />


# RESULT:
The Commands are executed successfully.
