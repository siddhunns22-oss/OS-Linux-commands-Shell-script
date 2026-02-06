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
<img width="339" height="152" alt="511956363-bae81d38-6fb4-4124-9326-1ae84fe087bb" src="https://github.com/user-attachments/assets/2e7977f7-aef5-4d53-bca0-fa88e74418e0" />




cat < file2
## OUTPUT
<img width="317" height="173" alt="511956528-27fed866-46f4-4e2b-a7f6-fdcb8febf0c2" src="https://github.com/user-attachments/assets/b386e68d-6da9-4187-a62f-0d30d8a65400" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="372" height="73" alt="511956826-fc47f30b-a40a-4ca6-b039-3fdfe93611a3" src="https://github.com/user-attachments/assets/800b7fe1-f9c9-48c3-9ebc-b0db5a1bd2ec" />

 
comm file1 file2
 ## OUTPUT
 <img width="348" height="225" alt="511956989-270cc12d-2474-4108-86f0-d8d387c85acf" src="https://github.com/user-attachments/assets/b830dd54-aea1-49fe-9085-54ecd735cea1" />


 
diff file1 file2
## OUTPUT
<img width="331" height="276" alt="511957088-1fe6d29c-a924-4814-9a0c-b5ce7396dfd4" src="https://github.com/user-attachments/assets/e3b84279-7ac7-482d-9af3-fbc6cdb2c6ca" />


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




cut -d "|" -f 1 file22
## OUTPUT

<img width="317" height="123" alt="511959341-1b049f46-4075-44c8-a0ef-efe5cd178e25" src="https://github.com/user-attachments/assets/7bd1dac6-577b-44b1-a7dd-30b418bd0fc0" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="318" height="121" alt="511959462-abdbda19-afb4-4c9a-9f08-20b0c8e8fe69" src="https://github.com/user-attachments/assets/f5573262-d5e7-42ce-ac9e-d6d6521da576" />


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
<img width="318" height="75" alt="511960675-8006ca74-4ed5-49dc-b45d-b976c0e96d93" src="https://github.com/user-attachments/assets/5f35a486-09b5-4648-9fe9-afba845c67af" />



grep hello newfile 
## OUTPUT
<img width="323" height="73" alt="511961377-a63bb5b1-dbb9-4494-879a-5ed03040fead" src="https://github.com/user-attachments/assets/3f55253a-f718-4bba-9773-35dc7643d90a" />




grep -v hello newfile 
## OUTPUT

<img width="325" height="72" alt="511962389-c05d9cc5-9bb4-4bb3-8888-5b5abcb8d612" src="https://github.com/user-attachments/assets/0836f8e0-cc59-44cb-9e1c-876d912d1120" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="360" height="96" alt="511963700-9ec70746-4c3c-40a4-ba65-3bac15b999b4" src="https://github.com/user-attachments/assets/6036caa8-f00d-4df2-99c2-1ba7173ecbcd" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="393" height="75" alt="511963902-a4536a7c-dfdb-4832-b18a-dbb29642c0dd" src="https://github.com/user-attachments/assets/4e47d2bc-c3cf-4d79-8040-ddcad7b6c925" />




grep -R ubuntu /etc
## OUTPUT

<img width="944" height="123" alt="511964895-a405e563-4de5-4ac9-a1ce-b6e7aedc7b76" src="https://github.com/user-attachments/assets/c7c82e4e-27e2-4405-b168-d7c6e493dc76" />


grep -w -n world newfile   
## OUTPUT
<img width="320" height="98" alt="511965103-0753b3b9-0a29-49c6-95a7-74b1a8b05593" src="https://github.com/user-attachments/assets/a996ab96-d18c-4758-8c38-1d1bb7c2b5b8" />


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
<img width="372" height="99" alt="511966204-9892ada7-562b-4060-beee-defa21d3d804" src="https://github.com/user-attachments/assets/9577f493-8a19-4d79-9b18-daf1e5d3d2c6" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="353" height="101" alt="511966544-c8e04b76-470d-4734-b04b-9b670c75401b" src="https://github.com/user-attachments/assets/57c18488-5ed5-4c3d-aa43-40a99d52a4bc" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="394" height="98" alt="511967892-5ab2c74a-c2ce-4250-a457-62bbf1eb7d51" src="https://github.com/user-attachments/assets/7934d737-b846-41c6-8114-e22619b8c5d3" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="318" height="75" alt="511968042-e885a80a-c34f-442d-8370-32575e081fbd" src="https://github.com/user-attachments/assets/b942ccea-0610-4066-9234-11c750d3d71c" />


egrep '(world$)' newfile 
## OUTPUT
<img width="315" height="98" alt="511968225-7c215ba4-95fc-4ea4-9f7f-01e916df41f0" src="https://github.com/user-attachments/assets/fe42c534-8f6d-49e4-ab5b-57fea69e2376" />



egrep '(World$)' newfile 
## OUTPUT
<img width="330" height="70" alt="511968460-27dab50e-47b6-44fe-9df9-123f9f41c3a4" src="https://github.com/user-attachments/assets/d1f4a04a-a54f-4fb9-856c-c3e75e230952" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="368" height="121" alt="511968949-39492592-b6c2-41d3-9404-f5dcce00272f" src="https://github.com/user-attachments/assets/042735d6-6f41-4907-a0f3-bed805f44a7f" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="318" height="75" alt="511969221-3c46f261-07a1-42a3-bfaa-4cf3edcce7b6" src="https://github.com/user-attachments/assets/ab776fb8-8431-49df-9b95-bebd7c6a000e" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="354" height="74" alt="511969465-da91ea7c-03b9-4827-9da4-5f343173311a" src="https://github.com/user-attachments/assets/ef8e9831-94b9-4980-ac42-dbbee5fd778f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="348" height="71" alt="511969793-15932af5-e9b2-4cfc-9f87-d7dac3bb29e9" src="https://github.com/user-attachments/assets/c2538f7f-a0a9-455d-9cfe-a5ad701792cd" />


egrep l{2} newfile
## OUTPUT
<img width="321" height="98" alt="511970379-66fc8a49-7488-405c-87ea-12332344b2b6" src="https://github.com/user-attachments/assets/6c93838d-6cee-4eb3-a14e-f87c63ae3ddc" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="326" height="123" alt="511971231-648e84a0-e3f8-4f6a-a45b-bae3268cfaaf" src="https://github.com/user-attachments/assets/0ea0d3fb-b2b5-457f-bc08-28f346dd3ec2" />


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
<img width="319" height="76" alt="511976491-9a8505c9-0112-4591-8559-43544801bff4" src="https://github.com/user-attachments/assets/d8dca06b-458b-4b5b-8b0b-3a7d58b57b9e" />



sed -n -e '$p' file23
## OUTPUT

<img width="314" height="75" alt="511976772-419645fa-09f2-46a4-a2b5-ee1f2ee158c5" src="https://github.com/user-attachments/assets/400a8174-8c3b-4505-b587-4027250ebb91" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="354" height="252" alt="511976967-efef5255-52a3-42da-9c9f-d078a38d4d7d" src="https://github.com/user-attachments/assets/8eb927e8-82a7-4e55-bcf1-234f3f03eefb" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="369" height="250" alt="511984545-c68e3939-60a2-4059-a6ed-4feca23f7e9b" src="https://github.com/user-attachments/assets/8856b12d-e913-40d3-bb56-b38bcab45d09" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="395" height="248" alt="511986043-dd486f8a-1c63-4a72-8e27-f3aece331d26" src="https://github.com/user-attachments/assets/b8556ad2-1627-451f-a561-b133a46ee556" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="329" height="176" alt="511988662-c1042905-6faf-4ac0-9ecc-1602654b62a9" src="https://github.com/user-attachments/assets/c3ef56f2-c022-47c5-a93a-cba46dcdb797" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="350" height="123" alt="511988854-8d0c368e-24aa-4a0c-bff1-a4fe8ae217d9" src="https://github.com/user-attachments/assets/f7433fd8-c068-48df-8e16-f32f6b7b3e51" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="384" height="100" alt="511989037-c13c045c-ec53-4df3-8e60-aed2a922f4f8" src="https://github.com/user-attachments/assets/de0b2f7c-7a9f-4d4b-ab66-b346548b47ee" />


seq 10 
## OUTPUT
<img width="317" height="297" alt="511989262-0d05aa17-ce63-4cc4-ad19-8a5577adf768" src="https://github.com/user-attachments/assets/2c02cc29-60b7-49a9-b779-d33e3b79f166" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="318" height="123" alt="511989425-16910e90-f0b2-4b24-be3c-3bfba92140a4" src="https://github.com/user-attachments/assets/007f20a9-1861-4de0-a113-0d7e7306947f" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="318" height="120" alt="511989565-9021381c-3968-44af-b3e9-49c9c4dd8ec3" src="https://github.com/user-attachments/assets/c716b7af-a893-415b-92e5-0e421a9b811e" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="318" height="149" alt="511989745-9ac03df2-5cf3-4936-b114-cc41fda3eb12" src="https://github.com/user-attachments/assets/0189f04b-ae62-4cc1-b185-c712b01cf767" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="311" height="123" alt="511989926-bf802a81-2e0e-490e-8127-ec24718597c4" src="https://github.com/user-attachments/assets/bed808da-445f-4f59-b727-045384e853a7" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="326" height="119" alt="511990064-e7fd48c5-9967-4391-aa8d-b76d9616f7ff" src="https://github.com/user-attachments/assets/c93c7f84-d9e5-4df8-95b4-17024de0eb15" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="326" height="119" alt="511990064-e7fd48c5-9967-4391-aa8d-b76d9616f7ff" src="https://github.com/user-attachments/assets/c5747cfc-0d58-4f25-8b38-7e67002fa876" />

sed -n '2,4{s/$/*/;p}' file23

## OUTPUT
<img width="363" height="126" alt="511990199-964f8929-ce1d-40d4-b76f-df686d23290a" src="https://github.com/user-attachments/assets/f095acf5-7bc5-423c-9afe-b0195dcbd5ef" />


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
<img width="335" height="175" alt="511990866-7a119411-3ea4-476e-a61f-1d670abfc172" src="https://github.com/user-attachments/assets/fa71f8a1-99b2-4275-9e4c-a28478b83315" />


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
<img width="336" height="173" alt="511991123-4b2b0bc5-6b49-4a81-a86d-30cd1012961b" src="https://github.com/user-attachments/assets/5090bd2f-927a-47eb-86a5-f33d6c20e8a1" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="424" height="249" alt="511991257-b9a56d12-7cf6-46be-86e3-d06a6d1cf44f" src="https://github.com/user-attachments/assets/e5ba5758-9ada-473d-a74f-b4579ad764f5" />


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
<img width="343" height="123" alt="512013281-fac59e97-13e4-4a7d-9dc0-624a8c45ec9f" src="https://github.com/user-attachments/assets/2737eb22-f8b3-420a-aaa4-e435a277c895" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="474" height="125" alt="512013440-f4a52021-6d59-4e1a-a2cf-195a694e63c5" src="https://github.com/user-attachments/assets/a10dbb18-0827-4e47-ac92-fd19cbfb7324" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="333" height="249" alt="512013577-5ff943cc-7b1e-4607-b497-4256749ff00f" src="https://github.com/user-attachments/assets/5136a8d1-6929-411a-8f85-ccacaf6af491" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="619" height="250" alt="512013821-ba5ea408-c5bc-463f-8688-60202ea4da42" src="https://github.com/user-attachments/assets/f78bc145-7cf9-4f9f-adb8-c9d1f068f972" />


tar -xvf backup.tar
## OUTPUT
<img width="424" height="249" alt="512014071-f8e2b043-2473-4b3f-b258-d1270b7df838" src="https://github.com/user-attachments/assets/67802543-0f30-4a6a-b690-caf2bd2e2d31" />


gzip backup.tar

ls .gz
 
gunzip backup.tar.gz

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="435" height="98" alt="512017522-b144942e-89c3-4df7-8c61-2c26460a32f5" src="https://github.com/user-attachments/assets/7d9ba61b-4849-40b0-b6d9-19a992e2757e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="449" height="127" alt="512017736-a03de28b-545d-47d0-bf62-2c278dfffe80" src="https://github.com/user-attachments/assets/d6041a32-66f1-4cac-b12f-e3d2d1cf8438" />


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

 <img width="619" height="447" alt="512018811-fcbe484d-6395-481c-82ba-1a5dc3e11bc2" src="https://github.com/user-attachments/assets/95afbef6-9891-4101-bc8f-1e0dc0cfe3b1" />

ls file1
## OUTPUT
<img width="423" height="72" alt="512018973-f012eb97-9e6a-42a4-9a5a-60a72aa05405" src="https://github.com/user-attachments/assets/20b07bb4-6cd3-4dcf-b237-bc043c0a8d02" />

echo $?
## OUTPUT 
 <img width="423" height="74" alt="512019312-c73e56f4-828e-4446-8a7a-43b0f0847ed0" src="https://github.com/user-attachments/assets/c040f2cd-4784-4e18-97e5-145b153468ac" />

abcd
 
echo $?
 ## OUTPUT
<img width="468" height="148" alt="512022754-5eb4e28a-df2e-49c1-89af-c744499c9770" src="https://github.com/user-attachments/assets/f0c2ab54-4937-4a9c-9b57-d33afd8f75b6" />


 
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

<img width="427" height="272" alt="512022852-b0dbf0a2-f285-4b7f-887d-358262bc5371" src="https://github.com/user-attachments/assets/4b114bad-977a-492f-8d38-479f1c19f56e" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="609" height="100" alt="512023484-2284344d-5db3-42dd-9368-05f3abbf063e" src="https://github.com/user-attachments/assets/f3035968-5d85-47db-bc7d-471693101433" />


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
<img width="457" height="76" alt="512092760-46be0b05-43f9-4d78-b5d6-9316a47a9283" src="https://github.com/user-attachments/assets/1f169cdb-1173-42f8-b8ca-e948a4ec5bde" />

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
<img width="423" height="75" alt="512093163-1844c946-358c-41fa-8c2c-63ef4945d28f" src="https://github.com/user-attachments/assets/a8ad56d1-f2c9-4e29-b08b-59c6290183cb" />



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
<img width="609" height="125" alt="512093595-49fd1f69-d262-4fb3-8e01-b99f768c0f6d" src="https://github.com/user-attachments/assets/d6dc7f84-10fb-4b2b-85a2-41bdeeb1f07b" />


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
<img width="633" height="150" alt="512094201-319ccf34-0ad4-447e-bbb6-e28a2ac2ed69" src="https://github.com/user-attachments/assets/bba1cb74-10f5-45d8-b09f-ad0aa8460a1b" />


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
<img width="629" height="105" alt="512094843-031c5add-3e6e-4cc0-9a49-b935dec26acc" src="https://github.com/user-attachments/assets/679ee9db-caa5-486c-92a0-124c57938de7" />


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
<img width="644" height="103" alt="512095276-219e6655-64b0-4726-ab48-179d33d570d0" src="https://github.com/user-attachments/assets/c5598b37-07e6-47a8-abae-52f6f7df7384" />

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
<img width="423" height="77" alt="512095831-a02bc547-575c-4087-b4ee-66149884f9ce" src="https://github.com/user-attachments/assets/fa308ca1-d584-40b0-a7cf-2475b6cb8a89" />

 
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
 <img width="441" height="304" alt="512096634-79237711-8203-4c97-8392-638e94d08d49" src="https://github.com/user-attachments/assets/902a9aab-cbc9-431b-b0db-42f35575df01" />

 
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
 <img width="504" height="175" alt="512097404-4a017ee1-8dc2-417f-8ba9-0e2075e958f3" src="https://github.com/user-attachments/assets/2107a5cb-ee3f-4970-9f0a-f8ecd0214c46" />

 
 
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
 <img width="603" height="249" alt="512098158-329bbb47-7739-4911-89ea-1255f096fb52" src="https://github.com/user-attachments/assets/1201b51e-595c-401d-847f-835b64d35171" />

 
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
<img width="605" height="177" alt="512099143-56c4cbf4-05d4-4eed-a726-9dc1c2c4abf6" src="https://github.com/user-attachments/assets/7960c912-841c-4670-926d-5a7b83ce1ab8" />

 
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
<img width="605" height="177" alt="512099143-56c4cbf4-05d4-4eed-a726-9dc1c2c4abf6" src="https://github.com/user-attachments/assets/684c0a81-0911-4c21-84a2-d8caa9b29a91" />


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
 <img width="618" height="252" alt="512108456-df6a52c2-1601-4787-933e-ee70e4267a50" src="https://github.com/user-attachments/assets/224f380b-5b3c-42be-9103-1354e6615504" />

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
<img width="615" height="252" alt="512111378-7372a389-0ce8-449f-97d7-6ed8a82a5893" src="https://github.com/user-attachments/assets/0a4e07d8-589c-43a7-b2cd-8a80b959bdb9" />


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
<img width="417" height="223" alt="512112487-1436bf04-0cd0-4fdb-8e84-fa55e359fd40" src="https://github.com/user-attachments/assets/cd2e159f-396b-493d-94af-36be0f3b3e9c" />


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
<img width="422" height="175" alt="512113707-42475008-5c1e-49ee-8624-0708580a9e77" src="https://github.com/user-attachments/assets/165137f4-54f0-4216-8ed9-b052db5d6f05" />

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
 <img width="428" height="76" alt="512114150-cdddea3b-89be-4092-8f86-480bc44d4213" src="https://github.com/user-attachments/assets/48f94dfc-c96c-44ec-8fc5-0f24df6997cc" />

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
<img width="414" height="353" alt="512114590-a78aec15-5751-4c48-ace5-1e78abc0d4d9" src="https://github.com/user-attachments/assets/c3d9cd71-8567-42f1-b84d-9f0ece5fea77" />

 
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
 <img width="414" height="353" alt="512114590-a78aec15-5751-4c48-ace5-1e78abc0d4d9" src="https://github.com/user-attachments/assets/96e74f97-1b90-4252-95e5-2352d3f0aa3a" />

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
 <img width="435" height="147" alt="512129204-68bae45d-fe6f-4d05-9989-f79300800260" src="https://github.com/user-attachments/assets/81ad4a3f-2c10-4ec0-a174-7132a71a2477" />

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
<img width="442" height="100" alt="512129699-0ef44a1d-0002-429f-917a-20806d1155d0" src="https://github.com/user-attachments/assets/ba66c427-7f94-471b-8eed-0ac9bccb27f4" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

 <img width="451" height="101" alt="512130568-524573b5-f62b-400b-a24f-78219c6602f5" src="https://github.com/user-attachments/assets/60d6dbca-9704-473b-91ae-d42f1c76fb66" />

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
 <img width="423" height="74" alt="512131479-369a8ca5-0786-4c58-8d69-04272ac8fc4b" src="https://github.com/user-attachments/assets/bc569fa9-dd5c-42e9-bd92-379876c993cc" />

 
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
<img width="420" height="124" alt="512131877-b3dc6c67-0f17-4f55-aef8-d62e2194d2ff" src="https://github.com/user-attachments/assets/2c579ffb-7109-4b3a-bd84-cfd37f634895" />

 
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
 <img width="419" height="124" alt="512132313-2f4797aa-917c-4736-915b-61095d21fa1e" src="https://github.com/user-attachments/assets/90e682d6-0f0e-4dcd-9dc0-72c174a23774" />

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
 <img width="418" height="401" alt="512132703-7d2af3b7-78f9-433a-b67c-14633bf26e8f" src="https://github.com/user-attachments/assets/8f87fa6d-374c-49ef-9755-a2df935acc76" />

 
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
<img width="433" height="126" alt="512133702-cdfd2ebe-5e0a-438e-89f6-d52db6af51f9" src="https://github.com/user-attachments/assets/93ab60fe-a7c5-4174-a9ab-7681ebac708e" />


# RESULT:
The Commands are executed successfully.
