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
<img width="379" height="122" alt="Screenshot from 2026-01-29 18-29-47" src="https://github.com/user-attachments/assets/6ffb3c1e-7592-49b9-ac5f-8ea5bbeb1cce" />



cat < file2
## OUTPUT
<img width="348" height="155" alt="Screenshot from 2026-01-29 18-35-06" src="https://github.com/user-attachments/assets/d7051612-3491-41e9-90e1-ea68f3ae311d" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="350" height="67" alt="Screenshot from 2026-01-29 18-36-29" src="https://github.com/user-attachments/assets/fac6dc5d-a35f-4a7c-96b6-fb18e150a802" />

comm file1 file2
 ## OUTPUT
<img width="356" height="185" alt="Screenshot from 2026-01-29 18-38-01" src="https://github.com/user-attachments/assets/49e7cc0f-6589-42c4-abbc-288ae3634adc" />

 
diff file1 file2
## OUTPUT
<img width="356" height="228" alt="Screenshot from 2026-01-29 18-38-54" src="https://github.com/user-attachments/assets/2ad436c9-3aab-49b5-8887-06380273b975" />


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
<img width="355" height="72" alt="Screenshot from 2026-01-29 18-42-14" src="https://github.com/user-attachments/assets/cb787b93-561b-4e68-89cd-137f816eec6f" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="365" height="99" alt="Screenshot from 2026-01-29 18-46-10" src="https://github.com/user-attachments/assets/f1f3353c-0d3c-4ac3-a075-810a7833eee2" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="365" height="99" alt="Screenshot from 2026-01-29 18-47-09" src="https://github.com/user-attachments/assets/c90cb4dd-15d6-48b3-afd5-453712414fe1" />


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
<img width="370" height="60" alt="Screenshot from 2026-01-29 18-50-32" src="https://github.com/user-attachments/assets/293477ea-ef61-4f49-a6b0-af7cfb97b385" />



grep hello newfile 
## OUTPUT
<img width="372" height="57" alt="Screenshot from 2026-01-29 18-51-26" src="https://github.com/user-attachments/assets/4ba2e3fb-a5df-42e5-b06c-39e11cd45c3d" />




grep -v hello newfile 
## OUTPUT

<img width="370" height="55" alt="Screenshot from 2026-01-29 18-52-43" src="https://github.com/user-attachments/assets/7e7044e0-d7a8-4ac3-85d5-09ead5ef50b2" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="455" height="97" alt="Screenshot from 2026-01-29 18-54-37" src="https://github.com/user-attachments/assets/164d7295-55e0-4b96-b6c3-352ee10ca36c" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="464" height="63" alt="Screenshot from 2026-01-29 18-58-07" src="https://github.com/user-attachments/assets/7f9432d5-f79d-4600-a1e8-b0021dd5b333" />



grep -R ubuntu /etc
## OUTPUT

<img width="501" height="186" alt="Screenshot from 2026-01-29 19-04-08" src="https://github.com/user-attachments/assets/4c79a15a-b4ae-459a-b896-7a945aedfd2b" />


grep -w -n world newfile   
## OUTPUT
<img width="497" height="99" alt="Screenshot from 2026-01-29 19-05-28" src="https://github.com/user-attachments/assets/af4dddf3-7363-4452-81c2-4a899931a129" />


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

<img width="496" height="78" alt="Screenshot from 2026-01-29 19-11-01" src="https://github.com/user-attachments/assets/cf444a3e-58ea-43d0-95a5-445ced42a9e6" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="496" height="78" alt="Screenshot from 2026-01-29 19-15-05" src="https://github.com/user-attachments/assets/953e2793-b83e-4a27-9c6c-46f5c4f753ad" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="496" height="78" alt="Screenshot from 2026-01-29 19-12-55" src="https://github.com/user-attachments/assets/1239242f-b8f6-453f-97c1-e61cd6997434" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="496" height="55" alt="Screenshot from 2026-01-29 19-20-30" src="https://github.com/user-attachments/assets/d2acdf38-ac4b-4074-8a55-c9caf2dd21fc" />


egrep '(world$)' newfile 
## OUTPUT

<img width="495" height="94" alt="Screenshot from 2026-01-29 19-23-37" src="https://github.com/user-attachments/assets/b74acfe0-d6ed-444a-b026-255d13b46496" />


egrep '(World$)' newfile 
## OUTPUT
<img width="495" height="94" alt="Screenshot from 2026-01-29 19-23-37" src="https://github.com/user-attachments/assets/7938f6b7-5d02-447e-b7f8-a68f19c16863" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="495" height="94" alt="Screenshot from 2026-01-29 19-27-04" src="https://github.com/user-attachments/assets/fbe73e15-60b4-4040-857e-d1554c27457e" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="502" height="59" alt="Screenshot from 2026-01-29 19-28-24" src="https://github.com/user-attachments/assets/2142f0d6-e925-4225-bbab-07294bb0cc4b" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="504" height="57" alt="Screenshot from 2026-01-29 19-52-03" src="https://github.com/user-attachments/assets/0b2f92cb-6a9b-47b0-a979-bb28ae16459d" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="502" height="71" alt="Screenshot from 2026-01-29 19-52-55" src="https://github.com/user-attachments/assets/3b1bd562-c4c8-453b-8455-ff4fb8852494" />


egrep l{2} newfile
## OUTPUT

<img width="499" height="73" alt="Screenshot from 2026-01-29 19-54-39" src="https://github.com/user-attachments/assets/4acd17e4-8756-4be2-bdca-fda7e9700117" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="502" height="95" alt="Screenshot from 2026-01-29 19-59-38" src="https://github.com/user-attachments/assets/0231fb18-7a0a-43d7-8643-475c49d9ae9f" />


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
<img width="501" height="49" alt="Screenshot from 2026-01-29 20-11-26" src="https://github.com/user-attachments/assets/d58df144-6bd2-43ab-97b9-09144ddf836d" />



sed -n -e '$p' file23
## OUTPUT
<img width="501" height="49" alt="Screenshot from 2026-01-29 20-17-31" src="https://github.com/user-attachments/assets/a50bbf54-1c24-4eb1-9164-54451e04f7de" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="499" height="207" alt="Screenshot from 2026-01-29 20-20-01" src="https://github.com/user-attachments/assets/6717c727-9c32-4561-a84d-8568ac130b5f" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="499" height="207" alt="Screenshot from 2026-01-29 20-21-29" src="https://github.com/user-attachments/assets/6ca5a284-add1-470d-a6a5-8a9d07c98772" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="499" height="207" alt="Screenshot from 2026-01-29 20-26-16" src="https://github.com/user-attachments/assets/95f52444-673b-4168-8f4f-a6de8048e24a" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="495" height="142" alt="Screenshot from 2026-01-29 20-27-49" src="https://github.com/user-attachments/assets/3c09c8c1-5a61-4a41-aa40-7fd499385a62" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="496" height="98" alt="Screenshot from 2026-01-29 20-29-53" src="https://github.com/user-attachments/assets/aeaf4118-527e-4204-836a-af15ab65cc79" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="500" height="82" alt="Screenshot from 2026-01-29 20-31-43" src="https://github.com/user-attachments/assets/6f83999e-5eae-40d7-945f-65bd369ec256" />


seq 10 
## OUTPUT

<img width="514" height="254" alt="Screenshot from 2026-01-29 20-32-42" src="https://github.com/user-attachments/assets/5467815b-acbd-4313-8b57-39140bb6a3d5" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="506" height="101" alt="Screenshot from 2026-01-29 20-34-54" src="https://github.com/user-attachments/assets/587549f4-a492-4305-bedf-575b79286f61" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="506" height="101" alt="Screenshot from 2026-01-29 20-35-53" src="https://github.com/user-attachments/assets/782a7cfa-5166-4cfc-8aeb-caff7496f436" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="510" height="128" alt="Screenshot from 2026-01-29 20-37-13" src="https://github.com/user-attachments/assets/be1901c4-f1bd-4fd2-b031-bee34ea24011" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="513" height="111" alt="Screenshot from 2026-01-29 20-38-29" src="https://github.com/user-attachments/assets/d7ad8027-f64a-428a-9044-52a00409cfa7" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="513" height="111" alt="Screenshot from 2026-01-29 20-39-54" src="https://github.com/user-attachments/assets/ca7b3e6a-35b1-4404-ad17-73199c700616" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="509" height="105" alt="Screenshot from 2026-01-29 20-42-11" src="https://github.com/user-attachments/assets/18baf14f-0d25-457c-b845-87faf140447b" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="509" height="105" alt="Screenshot from 2026-01-29 20-44-44" src="https://github.com/user-attachments/assets/2e4af883-b8c2-4010-9a68-f5e735633ca6" />


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
<img width="509" height="141" alt="Screenshot from 2026-01-29 20-52-06" src="https://github.com/user-attachments/assets/3e5b8a36-88dd-40b3-b850-4203d0198990" />


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
<img width="509" height="141" alt="Screenshot from 2026-01-29 21-02-20" src="https://github.com/user-attachments/assets/3bc77f52-51b7-415b-a9ef-ddc6fe29f24b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="507" height="208" alt="Screenshot from 2026-01-29 21-04-53" src="https://github.com/user-attachments/assets/bd4de057-f56b-489a-b131-7180a89926cc" />

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
<img width="502" height="102" alt="Screenshot from 2026-01-29 21-08-12" src="https://github.com/user-attachments/assets/e3d6c19e-de39-438d-bd26-b2ee47bd5322" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="502" height="102" alt="Screenshot from 2026-01-29 21-10-08" src="https://github.com/user-attachments/assets/667a4078-43ba-4b71-a121-74f8a4430ebd" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="181" height="137" alt="Screenshot from 2026-01-29 21-33-34" src="https://github.com/user-attachments/assets/04a6c96c-1eae-4940-a5aa-760eb0ac2bd0" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="187" height="146" alt="Screenshot from 2026-01-29 21-31-15" src="https://github.com/user-attachments/assets/f4858c86-aa08-43d9-bfc0-971dd5451717" />


tar -xvf backup.tar
## OUTPUT
<img width="231" height="143" alt="Screenshot from 2026-01-29 21-42-44" src="https://github.com/user-attachments/assets/9c64c159-0e14-4638-810b-f2b36b6a3961" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1155" height="85" alt="so" src="https://github.com/user-attachments/assets/07c1df00-2fa9-425a-af1d-fbeea2c7d4c1" />

gunzip backup.tar.gz
## OUTPUT
<img width="885" height="84" alt="image" src="https://github.com/user-attachments/assets/2172921c-26c8-442c-8d50-ab195c632589" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="891" height="125" alt="Screenshot 2026-01-29 225823" src="https://github.com/user-attachments/assets/efd941b2-4a95-4186-afcc-b7a6fb215823" />



 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="554" height="108" alt="Screenshot 2026-01-29 225831" src="https://github.com/user-attachments/assets/5513e30d-b422-4178-aa24-15242466145e" />



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
<img width="709" height="685" alt="Screenshot 2026-01-29 225946" src="https://github.com/user-attachments/assets/b2ff4cc3-d5f2-407d-bb88-e3efa62dd97e" />

 
ls file1
## OUTPUT
<img width="505" height="57" alt="Screenshot 2026-01-29 230022" src="https://github.com/user-attachments/assets/cf48e1fa-f6fc-4d86-886e-17972217c7bd" />

echo $?
## OUTPUT
<img width="462" height="53" alt="Screenshot 2026-01-29 230052" src="https://github.com/user-attachments/assets/a57b09a5-d48a-4d64-82a6-e86ee32b10a8" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="489" height="58" alt="Screenshot 2026-01-29 230126" src="https://github.com/user-attachments/assets/3ac63f5d-e1c5-46bf-b0b2-01aaf5689f6c" />

abcd
 
echo $?
 ## OUTPUT
<img width="518" height="251" alt="Screenshot 2026-01-29 230153" src="https://github.com/user-attachments/assets/39ffaa89-5e11-4fa4-8ef4-ceffc7dd192c" />


 
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

<img width="556" height="250" alt="image" src="https://github.com/user-attachments/assets/f94fe443-c82f-476f-817d-6856dba6a873" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="674" height="116" alt="Screenshot 2026-01-29 230257" src="https://github.com/user-attachments/assets/185296f3-1e50-4d69-8e92-8a925f93a99a" />


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
<img width="701" height="102" alt="Screenshot 2026-01-29 230412" src="https://github.com/user-attachments/assets/f5f2c261-a630-486f-874f-a4ea4c57ffd3" />

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
<img width="680" height="143" alt="Screenshot 2026-01-29 230449" src="https://github.com/user-attachments/assets/a31338ab-4383-4a16-8238-90ede48dc6c9" />



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
<img width="578" height="104" alt="Screenshot 2026-01-29 230524" src="https://github.com/user-attachments/assets/1beeefbc-6b8a-48d4-8220-520484d7ad68" />

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
<img width="638" height="130" alt="Screenshot 2026-01-29 230601" src="https://github.com/user-attachments/assets/5e93fee8-8c9e-4dc1-9b30-782bda3261af" />

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
<img width="485" height="65" alt="Screenshot 2026-01-29 230751" src="https://github.com/user-attachments/assets/c6be5203-16a7-4284-a859-594fa8140825" />


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
<img width="510" height="65" alt="Screenshot 2026-01-29 230821" src="https://github.com/user-attachments/assets/75d8b021-3cdf-4109-9777-894d6b2a4120" />

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
<img width="503" height="72" alt="Screenshot 2026-01-29 231004" src="https://github.com/user-attachments/assets/471db570-923c-41f4-a8c3-7d86d6955b9f" />

 
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

 <img width="494" height="232" alt="Screenshot 2026-01-29 231045" src="https://github.com/user-attachments/assets/639bfd2f-a015-4d79-832c-640a3e2a41e5" />

 
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
 <img width="516" height="133" alt="Screenshot 2026-01-29 231208" src="https://github.com/user-attachments/assets/b03b3e1e-9dd4-47c1-b528-560e2164d6d7" />

 
 
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
 <img width="510" height="179" alt="Screenshot 2026-01-29 231249" src="https://github.com/user-attachments/assets/ca3e3c4b-f685-4a46-ac4d-98bcf16e8248" />

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
 ## OUTPUT
 <img width="490" height="121" alt="Screenshot 2026-01-29 231333" src="https://github.com/user-attachments/assets/03ec9560-ebf1-4902-ad52-e12da03ce1cb" />

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
<img width="531" height="161" alt="Screenshot 2026-01-29 231424" src="https://github.com/user-attachments/assets/30e3e452-65de-4c2b-895e-20923ac1ef6e" />

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
<img width="528" height="273" alt="Screenshot 2026-01-29 231501" src="https://github.com/user-attachments/assets/f42fc582-e4b6-4cef-9978-595c994efc2c" />


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
<img width="491" height="141" alt="Screenshot 2026-01-29 231544" src="https://github.com/user-attachments/assets/34f91df6-1bdc-4b02-b271-2d081371317a" />

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
<img width="503" height="132" alt="Screenshot 2026-01-29 231618" src="https://github.com/user-attachments/assets/f397eba5-3d10-40d1-a8fe-e43968a76319" />

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
<img width="536" height="268" alt="Screenshot 2026-01-29 231652" src="https://github.com/user-attachments/assets/0d73791e-a611-495b-a822-1facb51133fb" />

 
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

<img width="475" height="101" alt="Screenshot 2026-01-29 231714" src="https://github.com/user-attachments/assets/7ff31a90-f5e8-4244-b9c1-d523d95c4ed0" />

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

 <img width="491" height="136" alt="Screenshot 2026-01-29 231757" src="https://github.com/user-attachments/assets/e9d4487e-1847-424c-840d-a3b62edf34df" />

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




 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh



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

<img width="475" height="55" alt="Screenshot 2026-01-29 232315" src="https://github.com/user-attachments/assets/ed9ac30c-a577-44af-8c9a-2d6af037dba2" />

 
 ./funcex.sh 1 2


 <img width="442" height="47" alt="Screenshot 2026-01-29 232253" src="https://github.com/user-attachments/assets/5a9e001a-cf97-4cd2-895c-df870f608534" />

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

 <img width="462" height="99" alt="Screenshot 2026-01-29 232228" src="https://github.com/user-attachments/assets/eb4b5a05-c611-4c40-8cef-e92031b9cd3d" />

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

 <img width="507" height="100" alt="Screenshot 2026-01-29 232202" src="https://github.com/user-attachments/assets/af83ad51-de98-445b-8469-20d800c11ab1" />

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

 <img width="509" height="311" alt="Screenshot 2026-01-29 232129" src="https://github.com/user-attachments/assets/b5cb78fd-38e6-44b7-b2cc-ac4fc00c6b60" />

 
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

 <img width="473" height="275" alt="Screenshot 2026-01-29 232048" src="https://github.com/user-attachments/assets/3bf197fd-57ec-42a1-bd6c-585ddec8314a" />

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

<img width="523" height="290" alt="Screenshot 2026-01-29 232021" src="https://github.com/user-attachments/assets/f6f02550-9740-4e1a-9322-0b525fd3817d" />


# RESULT:
The Commands are executed successfully.
