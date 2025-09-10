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
<img width="800" height="98" alt="487176822-b27d35f0-a01d-4705-a108-9e88eafac241" src="https://github.com/user-attachments/assets/25fb25b2-717e-4f5c-ba50-aa933a0719e8" />




cat < file2
## OUTPUT

<img width="800" height="98" alt="487176890-449de41a-3979-4155-a2c5-85f596b455c0" src="https://github.com/user-attachments/assets/ba525c94-8763-4f2d-98b9-2d56abe92726" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="834" height="37" alt="487177030-a39f8da8-2dbd-4fb8-8440-aa22a63aa631" src="https://github.com/user-attachments/assets/010ba2f6-85dc-4323-b9e1-bacb81ac7ac3" />

comm file1 file2
 ## OUTPUT

 <img width="833" height="171" alt="487177139-a31d4b58-dfce-4922-82b9-82bbed0b1a9c" src="https://github.com/user-attachments/assets/bd1701c7-2818-4ee7-b104-6f73dc66f3b9" />

diff file1 file2
## OUTPUT
<img width="864" height="215" alt="487177224-a0b7eb64-46f5-4d7a-b77c-e5be080ff1b1" src="https://github.com/user-attachments/assets/c1374c47-de08-4e70-86b2-037516680caa" />


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
<img width="855" height="60" alt="487177382-c4fe7959-b2aa-4a81-b057-cf879a2bc62d" src="https://github.com/user-attachments/assets/d3e43e08-24a3-4f27-9234-5c039bfca1c9" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="895" height="76" alt="487177451-f117a03c-b81d-4d3c-828d-37c7dc5c36d6" src="https://github.com/user-attachments/assets/3cdcf2d5-236b-4ff4-9ed5-c030ac3ea462" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="895" height="76" alt="487177599-4206c68a-1344-4aa2-bcfa-133503c67180" src="https://github.com/user-attachments/assets/f9698580-7891-41af-a51e-cc91da6d55a6" />


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

<img width="822" height="36" alt="487177727-1ef0f5bf-7657-4dc2-9bfa-43966bbc9208" src="https://github.com/user-attachments/assets/fe2dea17-01ec-4977-9e58-310d035791c7" />


grep hello newfile 
## OUTPUT

<img width="822" height="36" alt="487177808-b7bcbdc4-6611-4ca6-922c-2a38e303bcba" src="https://github.com/user-attachments/assets/37f25825-5153-4e6d-9a7c-a2badf7363f8" />



grep -v hello newfile 
## OUTPUT

<img width="822" height="36" alt="487177965-6b238c1b-a171-466e-8cdc-6011feee185b" src="https://github.com/user-attachments/assets/af3ec552-c24b-4fcb-a75b-2e77e7f244e1" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="830" height="54" alt="487178027-7c582bb7-ddb2-419b-8503-c484e916d1c0" src="https://github.com/user-attachments/assets/d17c338a-1053-4748-9767-e9a5209f9bb9" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="829" height="41" alt="487178364-17799ae5-39cb-4a43-99ef-a00829f12c4d" src="https://github.com/user-attachments/assets/b40407f3-0622-449e-b68f-6003b3bc44ee" />



grep -R ubuntu /etc
## OUTPUT
<img width="829" height="506" alt="487178366-2645cf9c-e2b3-4858-81e4-0dc4da0c38a5" src="https://github.com/user-attachments/assets/be0cca29-ae1c-41d5-a45c-1a7c5be15f97" />



grep -w -n world newfile   
## OUTPUT

<img width="758" height="84" alt="487178468-121a8bdb-80a7-4fdf-8388-b2ca60f2b64f" src="https://github.com/user-attachments/assets/63760613-8e5a-4b0f-9b01-dc643cc4bf58" />

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
<img width="810" height="87" alt="487178838-ae9d8c96-f11a-4248-8b4a-663f3d753cdb" src="https://github.com/user-attachments/assets/462f1355-45c6-4d51-a450-1e0935b5b812" />



egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="810" height="87" alt="487178839-45c4a3bc-7f41-482d-a92a-2f9b4c37a3be" src="https://github.com/user-attachments/assets/427abd40-3002-4e7b-9038-83ca2d6d53fe" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="810" height="87" alt="487178858-ffd6cd80-ea10-483f-8ecb-a325ea7017cc" src="https://github.com/user-attachments/assets/647f28b9-1097-41ce-97e2-63018414624a" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="810" height="87" alt="487178919-2779ab11-1b30-4f4f-9541-d7694f657fc0" src="https://github.com/user-attachments/assets/502f9beb-c0b2-496f-b9eb-d8c138ffaf38" />


egrep '(world$)' newfile 
## OUTPUT

<img width="810" height="87" alt="487179048-ad409625-e076-4992-ace8-ecdf0bba0d3a" src="https://github.com/user-attachments/assets/5654e671-cad7-4f51-b8c9-87e4f84b0e83" />


egrep '(World$)' newfile 
## OUTPUT

<img width="810" height="87" alt="487179285-cbdea3c4-882a-455f-a289-3bc62abe47fe" src="https://github.com/user-attachments/assets/66eb36a2-3e48-430a-ab14-8ed49327aadd" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="810" height="87" alt="487179347-24c515e7-8768-47c0-aeb9-5733323d0791" src="https://github.com/user-attachments/assets/4052e50d-14a0-4993-a388-279bad76bc22" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="810" height="87" alt="487179510-4a5875ef-4ad7-47eb-b18e-161ca4e2871b" src="https://github.com/user-attachments/assets/c21613ae-31c3-4918-bbc7-1afbaf6a606d" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="810" height="87" alt="487179584-51df68b2-320e-4e8a-b22a-40e37368ac78" src="https://github.com/user-attachments/assets/4d6da08e-871b-48c0-ab2f-cbf4c4a47bc5" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="810" height="87" alt="487179618-2a70a75f-9902-4170-a97f-fd7950b4de80" src="https://github.com/user-attachments/assets/f623e3cc-3404-4810-ba1f-f39b225072a3" />

egrep l{2} newfile
## OUTPUT

<img width="810" height="87" alt="487179919-1b18dc60-2b0f-4e39-9867-4e89b7148e1f" src="https://github.com/user-attachments/assets/ff599a8a-0307-46ce-94c9-bdac83a66d74" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="823" height="98" alt="487179956-03607f3b-cbb5-4650-bb4e-f0ffe9374806" src="https://github.com/user-attachments/assets/910caca5-d930-429b-b6dc-ff2b362dd4e0" />


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
<img width="823" height="98" alt="487180479-5396fd16-1acd-4d18-943a-8457b83494f8" src="https://github.com/user-attachments/assets/345ef5fb-83f7-4444-8522-c4311c626107" />



sed -n -e '$p' file23
## OUTPUT

<img width="823" height="98" alt="487180522-d409a978-9b6c-4d15-af94-3eebbe4f5581" src="https://github.com/user-attachments/assets/2b200980-9122-4466-ba68-998eb7129674" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="839" height="195" alt="487180572-20f62fde-37c0-49c9-a460-f97fc7ca73bf" src="https://github.com/user-attachments/assets/88b4697a-b694-4628-b813-d4c8a6fed196" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="839" height="195" alt="487180683-3851413b-22b5-4f37-9b96-a90299a8c278" src="https://github.com/user-attachments/assets/70ba510a-2124-4249-a5cf-16e681b9824f" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="839" height="195" alt="487180725-ae883e03-2c38-4d58-9ead-9e4153a40813" src="https://github.com/user-attachments/assets/b293b3c8-c06e-4d2f-834f-c48b3427cf28" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="828" height="141" alt="487180990-ef6ef590-08ae-459b-b973-8c542923bc40" src="https://github.com/user-attachments/assets/2a1b18bb-ebb5-4867-b075-207d0e44c48b" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="817" height="104" alt="487180991-a5f72403-d669-458a-a691-e94f86724d60" src="https://github.com/user-attachments/assets/83e2d154-2033-484a-ae59-5b1353ca9abf" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="817" height="104" alt="487181115-218063a9-2051-410d-99cf-89b3a9c6f305" src="https://github.com/user-attachments/assets/c773ac98-df27-4cbc-93d3-69a91bbb5d75" />

seq 10 
## OUTPUT

<img width="838" height="233" alt="487181384-fc9f4cfd-d24c-4f69-89ad-f95720841626" src="https://github.com/user-attachments/assets/37835269-305e-4d4e-8001-ddaf6526f4dd" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="833" height="133" alt="487181386-7dae501a-c93a-4a7f-a809-449af1746927" src="https://github.com/user-attachments/assets/11fcef3f-e599-42a7-82f1-eabb27ebc68b" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="833" height="133" alt="487181385-57934465-e09d-4382-b66a-30fe91c9270a" src="https://github.com/user-attachments/assets/2a3c0f73-a515-467f-9293-ff36c42ca44d" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="833" height="133" alt="487181394-4dba14c7-1383-4f0c-b160-4d661b0c9c91" src="https://github.com/user-attachments/assets/2c798538-ff1c-4ab8-93a8-264ea0e46cc2" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="833" height="133" alt="487181529-44c3acc3-dadd-4b98-a150-74bf2bc6410d" src="https://github.com/user-attachments/assets/261fd433-fea0-450b-b897-70ed53bd7b14" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="833" height="133" alt="487181583-da605c5f-30e3-494f-8733-7ca543a8161f" src="https://github.com/user-attachments/assets/c3e9d183-08b0-4718-8a1e-db7bf10f10ae" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="833" height="133" alt="487181664-83cbb602-1243-4dda-9ce0-ea5d332d945f" src="https://github.com/user-attachments/assets/04765748-7c17-471d-a685-404f95739bf8" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="833" height="133" alt="487181914-0559660f-4b6b-4fda-9ccd-6d51d89412d9" src="https://github.com/user-attachments/assets/1656055a-b91c-4945-9da8-ba30eecbbb37" />

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
<img width="833" height="133" alt="487181999-8a76aa6f-78ed-4b03-be36-eaef2e5a3bd2" src="https://github.com/user-attachments/assets/cf6d59d3-6dcc-4486-b7a2-65a3f490181c" />


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

<img width="832" height="189" alt="487182228-96d96def-94d4-4f0e-a1f2-9c2610b99420" src="https://github.com/user-attachments/assets/57759461-c4e6-44d9-a02d-12d29f80a8cc" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="832" height="189" alt="487182276-0b2e0ccf-04c2-4600-8d44-64ad52c4f163" src="https://github.com/user-attachments/assets/60cc4a0f-193a-465c-8478-ea225d45f9c7" />

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

<img width="822" height="105" alt="487182636-15e219b8-5459-43c6-a2e2-3da2c305bbd2" src="https://github.com/user-attachments/assets/227b0b97-b41b-4163-b8d4-fc5fc5f3c630" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="822" height="105" alt="487182694-17a49ea3-7b8f-4c26-8d9d-3e8a3130e69e" src="https://github.com/user-attachments/assets/debd3416-d54b-4948-b1de-9bbf8fdf7776" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="834" height="630" alt="487182999-7d0c41a7-e24a-4c48-add8-6d14a04fccb1" src="https://github.com/user-attachments/assets/29e0ddcd-2996-47d6-9a8a-936a6c04fb06" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="837" height="637" alt="487183057-dd9bfa18-4c8f-4593-b4aa-bf0351ad2677" src="https://github.com/user-attachments/assets/c34a2f25-c209-431a-9598-bafb854d585d" />


tar -xvf backup.tar
## OUTPUT
<img width="824" height="71" alt="487183102-e5823b80-ff9b-424e-a884-d621baa20084" src="https://github.com/user-attachments/assets/e774b00e-c229-46b4-91f9-487bdeb73b1a" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="835" height="108" alt="487183170-9755742a-80d9-4cb5-8744-32e1668789a7" src="https://github.com/user-attachments/assets/0df66ab2-04fb-4ec8-a78b-a8d1391cf5d1" />

gunzip backup.tar.gz
## OUTPUT

 <img width="835" height="108" alt="487183170-9755742a-80d9-4cb5-8744-32e1668789a7" src="https://github.com/user-attachments/assets/81a21506-4de1-4b27-ba8b-9d1bacc7b125" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="835" height="108" alt="487184346-2e7aa4c1-bd2d-44a3-9249-fc2f6b714f0f" src="https://github.com/user-attachments/assets/3dd4d80b-340c-4291-953b-16d18cf647e8" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="422" height="116" alt="487184484-dceb295d-3f15-4573-894b-184ce1a279d3" src="https://github.com/user-attachments/assets/292ebebb-c7e1-4682-8671-5dbe58ff7f25" />

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
<img width="811" height="645" alt="487184764-3848ba74-da09-476a-9661-b770584cdfa3" src="https://github.com/user-attachments/assets/62c793fc-411c-41f7-a145-6c843b5265fe" />

 
ls file1
## OUTPUT
<img width="646" height="84" alt="487184859-bedbccba-1f54-4fcb-b85a-84fb55b1dee6" src="https://github.com/user-attachments/assets/142cb5a7-6778-43b6-b834-659bb69a9ec6" />


 
abcd
 
echo $?
 ## OUTPUT

<img width="628" height="63" alt="487185067-cfb1f778-e998-4f16-b578-3855962c0ce0" src="https://github.com/user-attachments/assets/90816d14-9ae7-4d63-8bdd-6c45e32b9357" />

 
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
<img width="487" height="331" alt="487185200-d98edd26-786f-47e6-b1db-97a07e66ac9d" src="https://github.com/user-attachments/assets/eb10899f-9633-4c7c-904a-c8bd7fda4569" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="741" height="88" alt="487185280-a556e682-3df0-4a23-8d07-2a9da3ac1b20" src="https://github.com/user-attachments/assets/56c3ba35-81c9-4866-a3c0-cc95573be7b4" />

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
<img width="741" height="88" alt="487185397-23cb659d-a39c-4416-8c97-115cda3029fa" src="https://github.com/user-attachments/assets/b1924b96-435c-4920-9e14-d88375471ea7" />

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


<img width="746" height="133" alt="487185489-cb52d413-d679-499f-89f0-a94fe289bc6e" src="https://github.com/user-attachments/assets/aec4f532-8577-4213-a6a0-762fa5d7957b" />

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
<img width="746" height="133" alt="487185785-073fec0a-756c-43f7-9a49-e4193cf06dbe" src="https://github.com/user-attachments/assets/0270fa35-b295-48e0-9679-4230e5e4cf3a" />

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

<img width="746" height="133" alt="487185938-b54cde0d-e2d5-4ca9-87fd-707e94787ae6" src="https://github.com/user-attachments/assets/5f748792-f774-42fa-b699-6bfbf5801cbb" />

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

<img width="746" height="133" alt="487186078-9bb14c54-4450-471c-a29d-5ef97d939ca7" src="https://github.com/user-attachments/assets/b8c0411e-8472-405c-9a24-28fc9996ffd7" />

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
<img width="746" height="133" alt="487186147-319e52b3-5e88-4ef6-97eb-6ab0461e04c4" src="https://github.com/user-attachments/assets/2af5690e-5f88-43e2-9493-fcbb44a32e77" />

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
<img width="777" height="172" alt="487187906-c17f9ec5-2ec6-4eec-993d-c163f51a3c8b" src="https://github.com/user-attachments/assets/33230da8-9113-499e-a3e5-88678eb00ea4" />


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

<img width="771" height="180" alt="487188159-5ffae6e5-308f-400a-bde5-0493b812e1bf" src="https://github.com/user-attachments/assets/70807324-718a-4acc-91c2-6053b43bce40" />

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
<img width="771" height="180" alt="487188296-9891b24b-cff4-4d2f-8368-46c4d213b412" src="https://github.com/user-attachments/assets/f0de0439-5555-4968-acb9-bf3cb13d40fb" />

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
<img width="771" height="180" alt="487188433-54d62678-5870-45ff-bab5-87f8019198f6" src="https://github.com/user-attachments/assets/64070a73-67cb-4f87-8101-83f87c3feaae" />

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
<img width="771" height="180" alt="487188575-3726ac5c-d1dd-49a0-8214-382fd55ec3a1" src="https://github.com/user-attachments/assets/18ac3ad5-b694-42d0-b40f-85c776cbe162" />

 
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

<img width="771" height="180" alt="487188709-b871ab33-40eb-412f-ba6e-484078598065" src="https://github.com/user-attachments/assets/f24904e0-e994-40cd-8b10-832b3f9f190f" />

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

 <img width="767" height="155" alt="487188844-51a00670-1f32-4efc-924d-67e6b4f78b54" src="https://github.com/user-attachments/assets/4c9e0a6d-cada-49ef-bf9a-03ff9aba29fb" />

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

## OUTPUT

<img width="759" height="119" alt="487189777-93552cc0-6515-46b7-a7ef-3c8f17410cf0" src="https://github.com/user-attachments/assets/c7308ca8-63f8-44f8-bc7c-be4ebf1a1603" />


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

 
 ./funcex.sh 1 2

 
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
<img width="759" height="119" alt="487190022-e0cc81ee-e2b8-445d-b71f-a77977788128" src="https://github.com/user-attachments/assets/2a366a1f-f2e6-4516-9c09-9c02f9ea7261" />

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
<img width="759" height="119" alt="487190149-350ac84c-d58c-47d3-9290-a9c0cb9842c7" src="https://github.com/user-attachments/assets/dbc299f2-b19d-4c56-826a-de4545d84577" />


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
 
 <img width="754" height="336" alt="487190261-9f9d0d97-0e91-4730-90d2-d88d84816f9f" src="https://github.com/user-attachments/assets/c70d820a-d5e6-41a8-8c20-b64647ca87f8" />

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
 <img width="761" height="288" alt="487190396-aa599537-8049-467d-8613-f5f46600554b" src="https://github.com/user-attachments/assets/5f7b9c79-d2e4-47db-9e69-b587dc7a1c07" />

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
<img width="751" height="119" alt="487190533-c9892eec-a214-4a14-9293-9573bd0f538e" src="https://github.com/user-attachments/assets/45997ca8-8b2d-4ae4-b797-5927b4529ab2" />


# RESULT:
The Commands are executed successfully.
