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
<img width="248" height="58" alt="Screenshot from 2025-08-18 11-47-28" src="https://github.com/user-attachments/assets/2f28980e-a53e-4f43-b721-ca3ce5e47906" />



cat < file2
## OUTPUT
<img width="214" height="92" alt="Screenshot from 2025-08-18 11-48-20" src="https://github.com/user-attachments/assets/56fd44c0-783b-48e0-b0e0-e762d812c62f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="501" height="40" alt="Screenshot from 2025-08-18 11-49-14" src="https://github.com/user-attachments/assets/98685f08-8752-43e5-a9d7-7df0cdba322b" />

comm file1 file2
 ## OUTPUT
<img width="499" height="128" alt="Screenshot from 2025-08-18 11-50-15" src="https://github.com/user-attachments/assets/af6cd1df-856f-4be6-98db-ee05e1294fb5" />

 
diff file1 file2
## OUTPUT
<img width="506" height="144" alt="Screenshot from 2025-08-18 11-51-43" src="https://github.com/user-attachments/assets/c63dcf4a-a99d-427e-a48f-7ee1645d97b9" />


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
<img width="494" height="64" alt="Screenshot from 2025-08-18 11-55-23" src="https://github.com/user-attachments/assets/5f5d2e1d-8a4d-47f2-9ac4-bda9cbd881a0" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="546" height="78" alt="Screenshot from 2025-08-18 11-56-40" src="https://github.com/user-attachments/assets/1af66d61-4c08-48b4-bafa-264a1d1b8f73" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="543" height="78" alt="Screenshot from 2025-08-18 11-57-47" src="https://github.com/user-attachments/assets/d4b413c6-feb5-4f91-870c-248752a993d0" />


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

<img width="539" height="44" alt="478883273-b3057e20-ab8a-459b-af99-6de5ec0e9ef2" src="https://github.com/user-attachments/assets/cbcd3f83-922e-483f-8ce3-00a4e199cc4b" />


grep hello newfile 
## OUTPUT
<img width="539" height="44" alt="478883273-b3057e20-ab8a-459b-af99-6de5ec0e9ef2" src="https://github.com/user-attachments/assets/dc8f5168-80d8-4b1a-a714-f261bea6b081" />




grep -v hello newfile 
## OUTPUT

<img width="530" height="47" alt="478883328-ca92e7a9-0f16-4bcf-b04e-3177ac9c24ee" src="https://github.com/user-attachments/assets/8577525c-dd92-403b-8778-c431afc8d7d8" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="552" height="44" alt="478883491-8357174c-e186-48ca-820a-636073f99a8c" src="https://github.com/user-attachments/assets/29863183-5102-4d85-9bbe-55340d518fe7" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="595" height="89" alt="478883743-a6658a89-020d-4c48-9f9f-3435336f9616" src="https://github.com/user-attachments/assets/47b2821c-dcbd-4130-994a-52d2b352fec9" />




grep -R ubuntu /etc
## OUTPUT

<img width="599" height="602" alt="478883791-144ac063-875a-425d-a52f-5a0ffcffceb9" src="https://github.com/user-attachments/assets/6e569b22-2720-44a9-aafc-0db9fdfacac0" />


grep -w -n world newfile   
## OUTPUT

<img width="589" height="67" alt="478883829-abff3912-85c6-44a8-b5d3-44906cd78191" src="https://github.com/user-attachments/assets/299836b7-a4d3-4626-a97c-907f72f41545" />

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

<img width="600" height="90" alt="478883893-70059bb0-2ee7-4d94-8f16-e30ed00e7c72" src="https://github.com/user-attachments/assets/d45aa9f1-c941-4a79-b3a9-a1418ec0d806" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="595" height="86" alt="478883931-0815c606-d8fa-487e-a459-6e76bade12d1" src="https://github.com/user-attachments/assets/0f6686ed-91af-4d24-8f78-99c5fb5619b8" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="600" height="89" alt="478884016-f785600d-1da7-48d1-af71-c1fb81e52bdf" src="https://github.com/user-attachments/assets/1d6d6500-bf10-49c7-9611-ef6e65aba709" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="587" height="47" alt="478884057-fce21795-a5b4-4310-ae82-40d5ce674d93" src="https://github.com/user-attachments/assets/637beb04-04ee-4c6f-8e84-d3b161c5dbdc" />


egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT

<img width="586" height="68" alt="478884114-83317c2b-79d3-42d0-963a-cfc8200c9721" src="https://github.com/user-attachments/assets/92a20ff6-1ac9-469f-befd-64cdf8457661" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="594" height="45" alt="478884182-6e6751d0-8c39-4722-8909-754789f2c293" src="https://github.com/user-attachments/assets/d16eb06c-2d7f-47db-beac-8dbf92666950" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="598" height="112" alt="478884240-c2375281-4e10-48d7-9581-3d58cb5ff4c2" src="https://github.com/user-attachments/assets/cca7c181-b61d-4135-a185-378b48a5d856" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="573" height="53" alt="478884278-dbe17a4b-89d3-426a-888a-7e04ab39b274" src="https://github.com/user-attachments/assets/f983fe61-1905-4288-9831-2f3a54deab5e" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="598" height="71" alt="478884714-79395cc8-18ec-441f-bdf3-a68c9a467473" src="https://github.com/user-attachments/assets/289265b7-999d-4500-afca-8347369a72a4" />

egrep l{2} newfile
## OUTPUT

<img width="536" height="69" alt="478884741-37c86662-a830-4633-81a9-d626f8311abc" src="https://github.com/user-attachments/assets/24a3b84a-d6c9-463f-991c-0a5a54523107" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="569" height="86" alt="478884774-b7fa40af-16fc-4eed-b788-72be1c684870" src="https://github.com/user-attachments/assets/d9988439-c3ef-4c68-9d68-0787293e1b02" />

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
<img width="549" height="41" alt="478884823-32a07242-1af4-437f-b8e9-3e4758e4a0cc" src="https://github.com/user-attachments/assets/9268b92a-8e4c-4dd1-a953-c1ab4ba06918" />



sed -n -e '$p' file23
## OUTPUT

<img width="553" height="43" alt="478884850-b75de511-2ba0-495b-a04d-8c3a97e4846c" src="https://github.com/user-attachments/assets/bf32e214-f233-4cb7-8149-0fd7c777454c" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="597" height="219" alt="478884956-2fcffdd3-9650-4285-bf90-f60c8b9ccf9e" src="https://github.com/user-attachments/assets/87d815bd-3010-4075-97f0-6dcc7c862b01" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="593" height="221" alt="478885002-4d990337-7e96-44a8-89fc-6e43e9e7a344" src="https://github.com/user-attachments/assets/a9b30ac7-f087-49d6-9624-3079b4950734" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="596" height="220" alt="478885090-f9232e0d-827c-4629-966d-3bab3e758926" src="https://github.com/user-attachments/assets/0061fc6d-cb4b-4e0e-94d7-7f0a1987f5fc" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="571" height="134" alt="478885133-0350f000-faa4-4578-99c7-37c16716c249" src="https://github.com/user-attachments/assets/027de680-bb59-4655-ba88-6b4f207bba51" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="594" height="110" alt="478885189-83a22e73-7975-4733-bd75-cf1640adaa0e" src="https://github.com/user-attachments/assets/ac6d4846-3c7d-4c91-9c34-e0d1fcf43272" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="596" height="93" alt="478885223-a7aa91cd-cc92-49b8-af79-0a1873314994" src="https://github.com/user-attachments/assets/e74d0970-435d-4b09-b933-8c84f1aef910" />



seq 10 
## OUTPUT

<img width="407" height="245" alt="478885239-ceee87be-c28f-4d10-9d61-f438e8cc2191" src="https://github.com/user-attachments/assets/0b614345-0c25-4d0b-9837-8d6c7e487df9" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="575" height="91" alt="478885335-65cbc34d-0bb1-40ff-9602-a4143b67a709" src="https://github.com/user-attachments/assets/9fd94335-a198-4694-9e12-fc468624849b" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="575" height="91" alt="478885335-65cbc34d-0bb1-40ff-9602-a4143b67a709" src="https://github.com/user-attachments/assets/f42bccc4-0df0-405b-bafd-6536d3c1c001" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="568" height="117" alt="478885360-356b42a4-ee83-4cea-a253-927fc7268384" src="https://github.com/user-attachments/assets/7b8a79f6-af6e-4b95-aa5b-53a45f44f3c5" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="559" height="92" alt="478885400-c4099407-1adb-461a-b5e6-d00be8cebc01" src="https://github.com/user-attachments/assets/1c871dd5-abb0-4e73-a84e-ec88e14a3781" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="583" height="90" alt="478885428-6167e454-c4b6-4fde-9758-8523ee858f28" src="https://github.com/user-attachments/assets/26ae55b2-2c08-4702-9eb3-74ab95e0e62d" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="595" height="111" alt="478885517-20da1fac-24de-43bd-b940-aeff9a2d1186" src="https://github.com/user-attachments/assets/d7b1f42c-2f17-49f2-81d9-3da5683ae6ce" />

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
<img width="458" height="134" alt="478885551-ad97c1bb-03bd-407d-a15a-2f170d424f7b" src="https://github.com/user-attachments/assets/ae4015f3-ebba-45de-a3cd-14a38fdbd938" />


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

<img width="454" height="136" alt="478885583-0f010419-5527-4d50-97d2-dfb1cb1952d2" src="https://github.com/user-attachments/assets/4922fad4-f7b0-4380-bc45-1410daba8976" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="602" height="223" alt="478885604-d40db652-e54d-4df1-a3ea-d74fdc414017" src="https://github.com/user-attachments/assets/d4a0a309-24b8-4870-be6e-85d9bcd408a7" />

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


 <img width="586" height="113" alt="478885645-dc25d46b-4bc3-4cb7-834e-3a7cc3fe45d7" src="https://github.com/user-attachments/assets/354c363d-c396-4791-ba80-6dea18aba736" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="593" height="118" alt="478885670-e5ac1b5f-965d-4aa8-84f4-d0d21dc94a8e" src="https://github.com/user-attachments/assets/1fb06c20-5b58-4038-af75-3edebbb8188a" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="558" height="200" alt="478885691-7cc4adad-d50b-4443-9771-09d044ecd27c" src="https://github.com/user-attachments/assets/2e5d2773-6ded-444a-b45b-780721aefffe" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="598" height="226" alt="478885713-41d5df0c-d8a8-4951-ac50-12e563587188" src="https://github.com/user-attachments/assets/d18cc772-4cb2-45c4-9322-aecef04d0775" />


tar -xvf backup.tar
## OUTPUT
<img width="591" height="220" alt="478885760-58239357-f228-4c63-9494-05c35c018a1e" src="https://github.com/user-attachments/assets/e66a64dc-1398-424d-b85b-032d238c8b58" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="560" height="48" alt="478885788-cc9b5c0f-ef60-4a8c-9d02-137b603e364c" src="https://github.com/user-attachments/assets/d9b217dd-e35a-4652-a7e3-d3efd4bda591" />

gunzip backup.tar.gz
## OUTPUT
<img width="606" height="113" alt="478885805-fdc1bbd2-15f2-4d76-b596-3c5f3a8af1e7" src="https://github.com/user-attachments/assets/1a521f9e-d0ad-41e2-9e99-af8dae706a8f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="593" height="92" alt="478885854-0ad498a3-039c-4063-8069-68b56788698e" src="https://github.com/user-attachments/assets/57b0f236-0620-421b-b0fd-d9e0df61a558" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="526" height="87" alt="478885894-2c1dd1a1-3e21-4734-8d13-04c0dd996762" src="https://github.com/user-attachments/assets/f269899b-0a12-4c9b-a56a-bcb1bd4fa94d" />



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
<img width="598" height="353" alt="478885930-34cf3c13-ab14-45c8-b608-c2fbf3aa8740" src="https://github.com/user-attachments/assets/0f75a6d6-420a-4921-a14e-15a3c5c6a757" />

 
ls file1
## OUTPUT
<img width="434" height="48" alt="478885974-58aa7ffd-372f-4a9d-8fe2-ce29711c8e43" src="https://github.com/user-attachments/assets/921cb91f-97ac-456d-b650-ec70f23f19e1" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="411" height="44" alt="478886089-c18b7ddb-7902-47f9-b27b-7f1e5c855a3f" src="https://github.com/user-attachments/assets/75fea54a-0f8f-4bc9-a6b6-18199535068f" />

abcd
 
echo $?
 ## OUTPUT

<img width="427" height="43" alt="478886158-45479c03-caad-46f6-9bd9-2296d6c4b942" src="https://github.com/user-attachments/assets/974223da-f957-4fb7-9251-745b5e645fcb" />

 
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

<img width="546" height="162" alt="478886218-fc708c9a-a927-4947-afc0-8ac10181bfc2" src="https://github.com/user-attachments/assets/900f3d2b-054b-42a4-97e6-8807143cb62f" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="565" height="91" alt="478886267-b041f365-c4af-4c30-aef0-d9df4eccf660" src="https://github.com/user-attachments/assets/04aa3a8d-ece3-4d3b-88c4-0aa1e3dbe162" />


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
<img width="565" height="91" alt="478886341-6d26ed8a-8c29-4340-b47b-3970c75301bd" src="https://github.com/user-attachments/assets/b1d41088-73d1-44dc-ae95-61f62590acbb" />

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

<img width="548" height="135" alt="478886426-6da2df2f-bd4f-4cb8-b5ab-e76556aea0f6" src="https://github.com/user-attachments/assets/67c47e0e-974a-4dc5-871c-e6995fdd883c" />


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
<img width="554" height="110" alt="478886481-690ebb49-4b0a-45d2-9f0a-e3d6b1d115ec" src="https://github.com/user-attachments/assets/e49c0b77-ffa1-4878-9588-c61b8ddacbad" />

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
<img width="555" height="138" alt="478886556-832090bf-f9c5-4ac4-a54c-a8718a25b763" src="https://github.com/user-attachments/assets/cc8e5327-6510-4db0-8a5c-1d0bea67f30d" />

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

<img width="567" height="90" alt="478886611-d9e7a975-62b9-4ac9-919c-6ce3bb486563" src="https://github.com/user-attachments/assets/041e0773-580b-4821-96a9-4648d205702c" />

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
<img width="560" height="83" alt="478886678-e4bb3333-e75d-415a-bdd7-85499acb7eb3" src="https://github.com/user-attachments/assets/15a731d5-7605-48fc-a912-2d6d716f3e62" />


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


<img width="547" height="204" alt="478886853-daec9f07-5587-4fc6-a37e-0a34f86350a7" src="https://github.com/user-attachments/assets/41f01437-e53c-4f79-a90f-572fa67de23d" />


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

<img width="587" height="218" alt="478886933-0b3ba4ef-734a-42d4-8100-3bfebf75cfe7" src="https://github.com/user-attachments/assets/1d804692-836e-4d10-8d5d-43ced090b6ce" />

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
<img width="562" height="153" alt="478886974-e563353f-4089-41a4-9a91-feea18765eef" src="https://github.com/user-attachments/assets/a9ca2c5c-dfe2-463e-a3c1-74066a49e3cb" />


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
<img width="572" height="155" alt="478887042-050430ff-df31-453a-8ba4-c5ead6f9e2b0" src="https://github.com/user-attachments/assets/c0c080c8-b8c1-4a80-aa29-15ed503315fe" />


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
<img width="565" height="305" alt="478887113-3d25888f-b67a-4887-9b67-c6e25231bce5" src="https://github.com/user-attachments/assets/6c950004-6b05-43fb-a26f-11263f05dd42" />

 
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
<img width="583" height="179" alt="478887183-f72396e3-36e4-4d0c-b329-ad07e0d274e6" src="https://github.com/user-attachments/assets/0c23d0a1-3652-4427-95bc-42724c359b8b" />

 
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

<img width="544" height="93" alt="478887231-9f02690a-660e-4482-a526-b6f3a36cb9a1" src="https://github.com/user-attachments/assets/366aeece-b8c1-4a0d-b3ea-8e1c67ba189a" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="548" height="91" alt="478887261-8fb60c74-2746-4288-b10b-9f5b532bd621" src="https://github.com/user-attachments/assets/7a0903e3-0459-455e-8a0d-10db1311eb9f" />


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

 <img width="546" height="71" alt="478887319-feaf7d5b-83e1-4476-87ff-0fb7e1a56bdc" src="https://github.com/user-attachments/assets/b0714698-44c3-4ca8-9f07-a8673b4a4075" />

 ./funcex.sh 1 2
<img width="519" height="47" alt="478887344-404a4dc4-7106-4b41-aebd-3615548f648b" src="https://github.com/user-attachments/assets/edc5e353-2a75-4e77-bd24-3969045d2f75" />

 
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
 <img width="570" height="93" alt="478887389-9964ae2e-194c-4c17-94a0-8fd2bb69e71c" src="https://github.com/user-attachments/assets/3bdc3f38-1821-41ea-b9f4-3458ca6ade46" />

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
 <img width="571" height="110" alt="478887493-164337d6-2730-46b1-b26c-6a9240ae2256" src="https://github.com/user-attachments/assets/d1fae5cc-f03b-45db-b15b-6fbef0803476" />

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
 
 <img width="568" height="329" alt="478887622-467af86f-c444-42ab-8701-242708ec82ba" src="https://github.com/user-attachments/assets/c8cf5b88-b72c-4478-9935-1fdebd6d2c24" />

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
 <img width="557" height="309" alt="478887678-d3d93b32-fcac-4fa2-af28-288bc5124e5e" src="https://github.com/user-attachments/assets/ecde8d21-6dc4-492b-b50f-430f388dcf3d" />

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
<img width="582" height="112" alt="478887713-8375ca20-7f3a-4740-abc3-54300d1bffc3" src="https://github.com/user-attachments/assets/1d1ce9b7-0d4d-48b9-970e-f91e8a37b86c" />


# RESULT:
The Commands are executed successfully.
