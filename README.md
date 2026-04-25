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
<img width="684" height="148" alt="image" src="https://github.com/user-attachments/assets/1dee1723-ff31-4675-badc-be94279e35e2" />



cat < file2
## OUTPUT
<img width="742" height="172" alt="image" src="https://github.com/user-attachments/assets/7357abf7-0a30-4675-af2a-3269e140555d" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="642" height="79" alt="image" src="https://github.com/user-attachments/assets/fe9277aa-5682-4b38-941f-e53b384d7b7a" />
comm file1 file2
 ## OUTPUT
<img width="694" height="225" alt="image" src="https://github.com/user-attachments/assets/f21621a5-6cd0-4d69-a780-cee4141ccaa7" />

 
diff file1 file2
## OUTPUT

<img width="697" height="284" alt="image" src="https://github.com/user-attachments/assets/5f929e00-c2c4-4fa6-8885-035aa309371d" />


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

<img width="676" height="158" alt="image" src="https://github.com/user-attachments/assets/2eeff6c7-2f29-499e-ba10-f39626e2bf7b" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="636" height="151" alt="image" src="https://github.com/user-attachments/assets/c9eb41b9-1e25-4cad-937f-c88633ca4fcf" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="694" height="233" alt="image" src="https://github.com/user-attachments/assets/72fe4bad-1e64-4864-bd26-b6b2db8592ec" />


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

<img width="771" height="83" alt="image" src="https://github.com/user-attachments/assets/76b59243-0e57-4f84-ac2f-8738b6e434b2" />


grep hello newfile 
## OUTPUT
<img width="665" height="82" alt="image" src="https://github.com/user-attachments/assets/ef338a40-52bc-4b29-88e3-77006f7b979b" />




grep -v hello newfile 
## OUTPUT
<img width="684" height="102" alt="image" src="https://github.com/user-attachments/assets/1b7a74d2-a2be-4056-9562-badf072326fe" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="667" height="69" alt="image" src="https://github.com/user-attachments/assets/10a75a35-17f6-48f9-aa1f-7cd780cd9baf" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="910" height="601" alt="image" src="https://github.com/user-attachments/assets/3d771334-1f2f-4ab4-96af-c014841ef663" />



grep -R ubuntu /etc
## OUTPUT

<img width="795" height="104" alt="image" src="https://github.com/user-attachments/assets/8c8100c2-5d85-4794-a6ad-5f75ab382386" />


grep -w -n world newfile   
## OUTPUT

<img width="759" height="104" alt="image" src="https://github.com/user-attachments/assets/4c83f550-c6ec-43ad-8a31-459e78eeaae9" />

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

<img width="665" height="100" alt="image" src="https://github.com/user-attachments/assets/efc35427-2a37-494e-925f-4d1c7718bcc0" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="655" height="96" alt="image" src="https://github.com/user-attachments/assets/5a2a187f-6173-45f8-8560-0fd66cc427b2" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="636" height="75" alt="image" src="https://github.com/user-attachments/assets/5081a013-5fd3-4689-b63b-9f609f3d666e" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="649" height="99" alt="image" src="https://github.com/user-attachments/assets/b50e2edb-3107-4118-b8ce-a4f233fb0942" />


egrep '(world$)' newfile 
## OUTPUT

<img width="691" height="91" alt="image" src="https://github.com/user-attachments/assets/f4101941-dc1f-4933-9926-9e31cd592802" />


egrep '(World$)' newfile 
## OUTPUT

<img width="634" height="133" alt="image" src="https://github.com/user-attachments/assets/b255d209-1d03-4c80-b55d-8107014ebf1d" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="649" height="81" alt="image" src="https://github.com/user-attachments/assets/01854bb7-6965-4605-9c2f-5007364fb463" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="692" height="75" alt="image" src="https://github.com/user-attachments/assets/3c112675-9b4b-4762-9cb7-edc5a27750be" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="702" height="81" alt="image" src="https://github.com/user-attachments/assets/446340a4-d79e-4a0e-9ed9-2f563891a42b" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="704" height="99" alt="image" src="https://github.com/user-attachments/assets/4a2b278b-6bc7-408d-bcb5-39fe9d795627" />

egrep l{2} newfile
## OUTPUT

<img width="663" height="136" alt="image" src="https://github.com/user-attachments/assets/7fa02d9c-86b2-4aa4-8ff5-cac2fa44664f" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="700" height="75" alt="image" src="https://github.com/user-attachments/assets/fa168530-13a4-460a-9d2f-1190f1daf9af" />

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

<img width="704" height="75" alt="image" src="https://github.com/user-attachments/assets/1c3cd44b-c410-4ab1-a7bf-571d7cd257f1" />


sed -n -e '$p' file23
## OUTPUT

<img width="744" height="250" alt="image" src="https://github.com/user-attachments/assets/becac793-36c5-42a3-98ff-8b491b0023e3" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="740" height="262" alt="image" src="https://github.com/user-attachments/assets/cf503310-d5a3-4d0a-8895-08d34c1c1ec0" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="733" height="261" alt="image" src="https://github.com/user-attachments/assets/bee08f3f-aeb8-4e8e-b85d-c42b9a1d4e01" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="911" height="86" alt="image" src="https://github.com/user-attachments/assets/20f47bd1-d96c-49b9-a17e-e4077e4b843c" />

sed -n -e '1,5p' file23
## OUTPUT


<img width="829" height="185" alt="image" src="https://github.com/user-attachments/assets/4e9f8a3a-0454-44ea-801a-d733a8f98224" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="697" height="135" alt="image" src="https://github.com/user-attachments/assets/ad81edc4-fd1e-424b-998c-8a11cdf5f413" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="717" height="106" alt="image" src="https://github.com/user-attachments/assets/391802f5-87de-4cdc-802e-bcbb2bae72c1" />



seq 10 
## OUTPUT
<img width="683" height="332" alt="image" src="https://github.com/user-attachments/assets/e68ffd3e-dce8-4d26-aa5d-4ea3fb4d768d" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="663" height="132" alt="image" src="https://github.com/user-attachments/assets/4340b8d8-f0c9-4bd8-9e7b-8fee5753d8f1" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="744" height="133" alt="image" src="https://github.com/user-attachments/assets/1b3375c8-96ad-47b8-8abb-ea36a380474f" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="736" height="151" alt="image" src="https://github.com/user-attachments/assets/b071582a-f330-4e18-b99e-2ce42d0f0f61" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="640" height="125" alt="image" src="https://github.com/user-attachments/assets/94b60008-5ead-4555-a729-e3e2949616f8" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="759" height="134" alt="image" src="https://github.com/user-attachments/assets/7bc2143c-fed2-4a27-85fe-00e2d85e44bf" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="682" height="126" alt="image" src="https://github.com/user-attachments/assets/d6e11e2d-fa1d-43ad-8b9a-02ae2c756f8f" />


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

<img width="728" height="168" alt="image" src="https://github.com/user-attachments/assets/fba63539-6075-4c66-a8c0-bc2b8877db3b" />

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

<img width="702" height="258" alt="image" src="https://github.com/user-attachments/assets/61608319-a1df-452e-82e1-1e9fd1ea8f3b" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="756" height="247" alt="image" src="https://github.com/user-attachments/assets/b5bc951f-9966-47bf-acbf-bc994042d33d" />

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
<img width="697" height="151" alt="image" src="https://github.com/user-attachments/assets/c1af48a2-6a47-4091-966a-76f1eb9a0881" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="848" height="154" alt="image" src="https://github.com/user-attachments/assets/2cf231b0-427f-49f9-b2ff-2d7183e7eb2e" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="793" height="330" alt="image" src="https://github.com/user-attachments/assets/0d883f44-36dd-4f32-86e2-71406fe08ca9" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="866" height="316" alt="image" src="https://github.com/user-attachments/assets/21f278e5-b23d-4cd8-a9c6-cce8c97c66f8" />


tar -xvf backup.tar
## OUTPUT
<img width="853" height="357" alt="image" src="https://github.com/user-attachments/assets/12e045d2-22a7-4721-8c41-9196f5256787" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="761" height="49" alt="image" src="https://github.com/user-attachments/assets/b45ae1c0-aed7-4946-98e5-7b6601f170f0" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="911" height="224" alt="image" src="https://github.com/user-attachments/assets/4ca3fa84-608b-449d-8071-09c9e6070f12" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="859" height="126" alt="image" src="https://github.com/user-attachments/assets/fe8a20f8-c002-4449-b52c-e84d452ff1b9" />


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

 <img width="733" height="80" alt="image" src="https://github.com/user-attachments/assets/63511d11-f634-44b2-99ac-0df99e633dbd" />

ls file1
## OUTPUT
<img width="798" height="90" alt="image" src="https://github.com/user-attachments/assets/141943b6-29d6-4615-bb55-645b231132fe" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="832" height="109" alt="image" src="https://github.com/user-attachments/assets/bf7ac693-03aa-4b19-b167-a433c2fedd13" />

 
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

<img width="916" height="308" alt="image" src="https://github.com/user-attachments/assets/4ad545a0-e6af-4381-8922-6f69e50d3e4f" />



# RESULT:
The Commands are executed successfully.
