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
<img width="220" height="141" alt="image" src="https://github.com/user-attachments/assets/2b5de248-9b44-4395-962c-c8e51ffe586d" />


cat < file2
## OUTPUT
<img width="227" height="173" alt="image" src="https://github.com/user-attachments/assets/c3c898ba-3361-415c-be42-0d934e2562a1" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="360" height="49" alt="image" src="https://github.com/user-attachments/assets/869254a4-31de-4fdc-b775-aa9bf52919c6" />

comm file1 file2
 ## OUTPUT
<img width="397" height="327" alt="image" src="https://github.com/user-attachments/assets/05cf727f-5519-4a61-bf71-85bea8071661" />

 
diff file1 file2
## OUTPUT
<img width="374" height="254" alt="image" src="https://github.com/user-attachments/assets/c9791eee-f4b6-4233-ad8f-2bf4e0eff4b6" />


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
<img width="282" height="118" alt="image" src="https://github.com/user-attachments/assets/af9d726c-8321-4eb1-a845-fc2022c1df57" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="386" height="36" alt="image" src="https://github.com/user-attachments/assets/76bdb019-8e9e-48c2-8f3d-30c6620378e0" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="383" height="33" alt="image" src="https://github.com/user-attachments/assets/ae2446d0-4928-4e06-a1a0-65a09a8f3b13" />


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
<img width="344" height="45" alt="image" src="https://github.com/user-attachments/assets/7b843aa5-c459-41a8-ba54-d12d6121fd3c" />



grep hello newfile 
## OUTPUT

<img width="335" height="40" alt="image" src="https://github.com/user-attachments/assets/0263c019-66ca-4375-bb73-5cabdd0a7bf8" />



grep -v hello newfile 
## OUTPUT
<img width="362" height="44" alt="image" src="https://github.com/user-attachments/assets/744f8d6a-3217-41e4-965d-4bb6683604b6" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="465" height="46" alt="image" src="https://github.com/user-attachments/assets/f3ad1f2a-e450-4a26-ac3c-a4e02a20fc0a" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="412" height="52" alt="image" src="https://github.com/user-attachments/assets/cd547bf8-936a-49e1-9956-78a0806df403" />




grep -R ubuntu /etc
## OUTPUT
<img width="808" height="503" alt="image" src="https://github.com/user-attachments/assets/837e34f6-92f5-4304-909b-9cb7406713df" />



grep -w -n world newfile   
## OUTPUT
<img width="349" height="38" alt="image" src="https://github.com/user-attachments/assets/cc3a407c-96f0-40d8-a51b-629215be87e6" />


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
<img width="473" height="46" alt="image" src="https://github.com/user-attachments/assets/dc5fa11d-40ff-4d19-a962-6bbd8b156f3a" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="363" height="40" alt="image" src="https://github.com/user-attachments/assets/a88a725a-b7ba-499c-bea1-64585c33c369" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="425" height="34" alt="image" src="https://github.com/user-attachments/assets/d608fc54-7d73-40a6-b3e5-9345cd3dd9c5" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="342" height="41" alt="image" src="https://github.com/user-attachments/assets/c2b0670a-4624-4064-8069-e093ba57e9a5" />


egrep '(world$)' newfile 
## OUTPUT
<img width="432" height="44" alt="image" src="https://github.com/user-attachments/assets/8659a05a-3a0d-427f-9c9f-55fb82f89847" />


egrep '(World$)' newfile 
## OUTPUT
<img width="435" height="61" alt="image" src="https://github.com/user-attachments/assets/09f9ea77-5d7c-423c-bd19-8b74a9709305" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="444" height="45" alt="image" src="https://github.com/user-attachments/assets/43d98f22-3d14-4d3a-89e8-9cddd6c6c88b" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="355" height="43" alt="image" src="https://github.com/user-attachments/assets/6427168a-975a-4499-b861-7d4de6935e8b" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="480" height="56" alt="image" src="https://github.com/user-attachments/assets/d51d463f-9ed7-4be6-9a01-350436ec9b36" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="436" height="51" alt="image" src="https://github.com/user-attachments/assets/76dc74be-bc0d-4f54-bbba-53a0e3762bb7" />


egrep l{2} newfile
## OUTPUT
<img width="319" height="55" alt="image" src="https://github.com/user-attachments/assets/5e2465cd-bdbf-42b7-a120-2eb3379a2956" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="392" height="41" alt="image" src="https://github.com/user-attachments/assets/264d639b-d28c-4ba0-906c-172f287d0769" />


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
<img width="372" height="42" alt="image" src="https://github.com/user-attachments/assets/498ba87d-7ba0-43fd-9ea6-464d7c53bcbf" />



sed -n -e '$p' file23
## OUTPUT
<img width="136" height="40" alt="image" src="https://github.com/user-attachments/assets/80d09bdf-f8da-4647-955d-a05252f4a6da" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="481" height="240" alt="image" src="https://github.com/user-attachments/assets/a2790ee1-91ff-43bc-8fb8-d7e25c019a82" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="473" height="231" alt="image" src="https://github.com/user-attachments/assets/d9f52e8d-4aab-4bfa-8715-057f4270c07a" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="419" height="227" alt="image" src="https://github.com/user-attachments/assets/c73092fd-0506-45e1-96ed-6acf7d8428e8" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="544" height="146" alt="image" src="https://github.com/user-attachments/assets/eae550f8-106e-4f1e-9191-ca3efdfba24f" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="447" height="92" alt="image" src="https://github.com/user-attachments/assets/ae6bdfe5-4ab6-4063-ab9d-b1a5a70fb478" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="443" height="82" alt="image" src="https://github.com/user-attachments/assets/842f267d-23d3-415a-9cdd-c1c2b8b439ac" />



seq 10 
## OUTPUT
<img width="443" height="276" alt="image" src="https://github.com/user-attachments/assets/44bc6079-221f-4b93-918d-d66960b380aa" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="448" height="103" alt="image" src="https://github.com/user-attachments/assets/2a15fc5c-3598-4a76-87a0-52cef10c7875" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="376" height="96" alt="image" src="https://github.com/user-attachments/assets/be29f96f-db9b-4792-b3ef-1ec219a9505d" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="349" height="131" alt="image" src="https://github.com/user-attachments/assets/5c45fcb6-a6fd-4135-839b-072e920322ea" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="432" height="99" alt="image" src="https://github.com/user-attachments/assets/007e8a6d-7e7b-4b22-9f4e-887f0a4c622b" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="418" height="97" alt="image" src="https://github.com/user-attachments/assets/b468d8aa-5403-4442-9dc7-f0aff1ea21c3" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="557" height="112" alt="image" src="https://github.com/user-attachments/assets/941ce00d-cf42-4c76-8117-7d0489d3e512" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="452" height="107" alt="image" src="https://github.com/user-attachments/assets/871aa3e4-e3d8-4830-94e9-a6f5de565cb3" />

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
<img width="306" height="57" alt="image" src="https://github.com/user-attachments/assets/e11886ea-1643-4942-9409-2eedb9b898c2" />


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
<img width="372" height="32" alt="image" src="https://github.com/user-attachments/assets/289708e7-6e47-43c4-8adf-b8b888f33eab" />



#Using tr command
cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="450" height="233" alt="image" src="https://github.com/user-attachments/assets/0537c0dc-27f6-4115-9ea4-7b8a2287562e" />

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
<img width="443" height="64" alt="image" src="https://github.com/user-attachments/assets/190f6337-fac4-4837-bb7d-2542a09183a4" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="464" height="60" alt="image" src="https://github.com/user-attachments/assets/cdd46578-eaaa-432a-b3d5-14d835ad71eb" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="463" height="224" alt="image" src="https://github.com/user-attachments/assets/ed83d632-94ee-4c37-9987-7077029a06c4" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="743" height="275" alt="image" src="https://github.com/user-attachments/assets/6312c0f2-a05f-4b29-80dc-2307c6c8ed71" />


tar -xvf backup.tar
## OUTPUT
<img width="497" height="227" alt="image" src="https://github.com/user-attachments/assets/ed3e6566-5d44-49d4-b9e6-cd207718b720" />

gzip backup.tar
ls .gz
## OUTPUT
<img width="749" height="78" alt="image" src="https://github.com/user-attachments/assets/33d3d9e2-07e3-4053-866a-27256c69aae6" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="664" height="34" alt="image" src="https://github.com/user-attachments/assets/5268adaa-2f6f-423a-9645-0ee7af7207ad" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
## OUTPUT
<img width="642" height="57" alt="image" src="https://github.com/user-attachments/assets/3569d36e-aba4-4e2b-ba25-854256ad1c74" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="571" height="61" alt="image" src="https://github.com/user-attachments/assets/51ebe8d1-e435-422e-8925-0deb272ba070" />


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
<img width="817" height="128" alt="image" src="https://github.com/user-attachments/assets/58cfe9f9-4f9b-4c93-b9aa-358b7e296185" />

ls file1
## OUTPUT
<img width="256" height="59" alt="image" src="https://github.com/user-attachments/assets/2170f2e5-3e6e-4650-a3bd-b9b2543abaa9" />

echo $?
## OUTPUT 
<img width="352" height="54" alt="image" src="https://github.com/user-attachments/assets/fa3d93c9-14c1-4d95-8a1a-e6df0d9af0cb" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="490" height="107" alt="image" src="https://github.com/user-attachments/assets/72ddbffa-3fb4-4f88-9d30-8b4b243b0889" />

abcd
 
echo $?
 ## OUTPUT
<img width="413" height="126" alt="image" src="https://github.com/user-attachments/assets/82cfc97b-be26-48d5-8465-e626c05436a4" />

 
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
<img width="489" height="56" alt="image" src="https://github.com/user-attachments/assets/e0a59cf0-4d00-4e12-967c-9faca2d2072c" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="657" height="86" alt="image" src="https://github.com/user-attachments/assets/059ee4bd-b24a-4072-a330-ea8267926759" />


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
<img width="502" height="57" alt="image" src="https://github.com/user-attachments/assets/88469662-412f-47d9-8330-0a0bf279cedd" />

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
<img width="684" height="37" alt="image" src="https://github.com/user-attachments/assets/34aeb05b-f74b-431d-b35c-4e93ffe6ee25" />


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
<img width="340" height="106" alt="image" src="https://github.com/user-attachments/assets/8418abe0-01a1-4171-8065-ac73ea2d4c1b" />


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
<img width="482" height="107" alt="image" src="https://github.com/user-attachments/assets/e08b8d00-aea1-4008-82db-8b312c115147" />

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
<img width="533" height="108" alt="image" src="https://github.com/user-attachments/assets/a0c03977-d0ed-4487-bd8f-22dc16b7d44a" />


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
<img width="460" height="109" alt="image" src="https://github.com/user-attachments/assets/f7c1c949-f0ca-46dd-ac44-d08961d47795" />


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
<img width="336" height="47" alt="image" src="https://github.com/user-attachments/assets/04072004-d0a8-4cb8-9b2e-e6d7bbec2547" />

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
<img width="641" height="252" alt="image" src="https://github.com/user-attachments/assets/566302e0-f46a-486d-9ba5-ef9572ad1500" />


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
<img width="432" height="110" alt="image" src="https://github.com/user-attachments/assets/c2ce6846-2b06-46ce-9dfe-996ed9791988" />


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
<img width="343" height="74" alt="image" src="https://github.com/user-attachments/assets/f535ebb5-9844-40a5-950a-15ff8866010b" />

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
<img width="433" height="103" alt="image" src="https://github.com/user-attachments/assets/b8f80cda-2016-448c-9a95-c3ff5f51da3a" />


 
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
<img width="339" height="102" alt="image" src="https://github.com/user-attachments/assets/a869edbb-c944-4a57-b2dc-1cf93490e0fd" />


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
 <img width="355" height="96" alt="image" src="https://github.com/user-attachments/assets/8a669085-4d80-4491-a7d8-d7128893dcd3" />

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
<img width="475" height="80" alt="image" src="https://github.com/user-attachments/assets/e6c3fa7a-299b-44e6-8d8e-4999a23cab83" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="451" height="38" alt="image" src="https://github.com/user-attachments/assets/5aa66fc8-3cf2-4f3a-b06b-c85ac6ae1195" />

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
<img width="554" height="47" alt="image" src="https://github.com/user-attachments/assets/2f5dc7b6-0c0a-457c-b39b-5680b4543037" />

./funcex.sh 1 2
<img width="502" height="71" alt="image" src="https://github.com/user-attachments/assets/2370a0e0-c575-4761-9db8-3f652064b02a" />

 
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
<img width="459" height="64" alt="image" src="https://github.com/user-attachments/assets/83cc2793-7895-49e3-8fa9-9274a6230d4c" />

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
<img width="352" height="37" alt="image" src="https://github.com/user-attachments/assets/100bfca4-1165-44a3-a1e2-d20eeb7db424" />

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
 <img width="568" height="68" alt="image" src="https://github.com/user-attachments/assets/cf7e3fa2-56a6-44b4-acd7-9ae3edb8b6dd" />

 
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
<img width="777" height="49" alt="image" src="https://github.com/user-attachments/assets/ee169363-f27d-4cf3-9efb-39b7af009dae" />

cat > palindrome.sh
```
bash
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
<img width="690" height="557" alt="image" src="https://github.com/user-attachments/assets/8b8a36b6-1ef6-4d7d-8f4b-a0d86f3381b2" />

# RESULT:
The Commands are executed successfully.
