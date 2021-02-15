---
layout: test post please ignore
title: Bandit OverTheWire Levels 1-15 Writeup
---

Level 0: oJ9jbbUNNfktd78OOpsqOltutMc3MY1

Commands:
ssh bandit0@bandit.labs.overthewire.org -p2220
ls
cat readme

What I learned: How to use ssh to connect to another system.

-----------------------------------------------------------

Level 1: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Commands:
ssh bandit1@bandit.labs.overthewire.org -p2220
ls
cat ./-

What I learned: How to interact with files named “-”.

-----------------------------------------------------------

Level 2: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Commands:
ssh bandit2@bandit.labs.overthewire.org -p2220
ls
cat “spaces in this filename”

What I learned: How to interact with spaces in a filename.

-----------------------------------------------------------

Level 3: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

Commands:
ssh bandit3@bandit.labs.overthewire.org -p2220
ls -a
cat “.hidden”

What I learned: How to access and read hidden files and directories.

-----------------------------------------------------------

Level 4: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

Commands:
ssh bandit4@bandit.labs.overthewire.org -p2220
ls
cd inhere
file ./-file*
cat ./-file07

What I learned: How to look at the contents of a file.

-----------------------------------------------------------

Level 5: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

Commands:
ssh bandit5@bandit.labs.overthewire.org -p2220
ls
cd inhere
find -type f -size 1033c ! -executable
cd maybehere07
cat “.file2”

What I learned: How to search files for specific contents.

-----------------------------------------------------------

Level 6: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

Commands:
ssh bandit6@bandit.labs.overthewire.org -p2220
file / -user bandit7 -group bandit6 -size 33c -type f 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password

What I learned: How to search directories for specific content, as well as how to hide errors.

-----------------------------------------------------------

Level 7: cvX2JJa4CFALtqS87jk27qwqGhBM9plV

Commands:
ssh bandit7@bandit.labs.overthewire.org -p2220
grep -w millionth data.txt

What I learned: How to search files for specific words.

-----------------------------------------------------------

Level 8: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

Commands:
ssh bandit8@bandit.labs.overthewire.org -p2220
sort data.txt | uniq -c | grep '^ *1 '

What I learned: How to filter and sort results from a file search.

-----------------------------------------------------------

Level 9: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

Commands:
ssh bandit9@bandit.labs.overthewire.org -p2220
string data.txt | grep =

What I learned: How to search files for specific characters.

-----------------------------------------------------------

Level 10: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

Commands:
ssh bandit10@bandit.labs.overthewire.org -p2220
base64 -d data.txt

What I learned: How to decode a file encoded in base64.

-----------------------------------------------------------

Level 11: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

Commands:
ssh bandit11@bandit.labs.overthewire.org -p2220
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

What I learned: How to translate a file to solve a rot13 cipher.

-----------------------------------------------------------

Level 12: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

Commands:
ssh bandit12@bandit.labs.overthewire.org -p2220
mkdir /tmp/extra
cp data.txt /tmp/extra
cat data.txt | xxd -r > data
mv data data2.gz
gzip -d data2.gz
file data2
mv data2 data3.bz
bzip2 -d data3.bz
file data3
mv data3 data4.gz
gzip -d data4.gz
file data4
mv data4 data5.tar
tar -xf data5.tar
file data5.bin
mv data5.bin data6.tar
tar -xf data6.tar
file data6.bin
mv data6.bin data7.bz
bzip2 -d data7.bz
file data7
mv data7 data8.tar
tar -xf data8.tar
file data8.bin
mv data8.bin data9.gz
gzip -d data9.gz
file data9
mv data9 data10.txt
cat data10.txt

What I learned: How to convert and decode different file types, and how to find their original type.

-----------------------------------------------------------

Level 13: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

Commands:
ssh bandit13@bandit.labs.overthewire.org -p2220
ssh bandit14@localhost -i sshkey.private
cd /
cd /etc/bandit_pass
cat bandit14

What I learned: How ssh keys can be used for logins.

-----------------------------------------------------------

Level 14: BfMYroe26WYalil77FoDi9qh59eK5xNr

Commands:
ssh bandit14@bandit.labs.overthewire.org -p2220
ssh bandit14@localhost -i sshkey.private
echo “4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e” | nc localhost 30000

What I learned: How to submit a password via port.

-----------------------------------------------------------

Level 15: cluFn7wTiGryunymYOu4RcffSxQluehd

Commands:
ssh bandit14@bandit.labs.overthewire.org -p2220
echo "BfMYroe26WYalil77FoDi9qh59eK5xNr" | openssl s_client -connect localhost:30001 -ign_eof

What I learned: How to use openssl to submit a password.
