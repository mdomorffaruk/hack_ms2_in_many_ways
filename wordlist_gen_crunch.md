# Crunch wordlist generation #
- Generate a wordlist with crunch
- Usage: crunch min max -t combination
- As we see crunch with a-z char and min 8 character, it will need nearly 1750 GB
- And we know that FTP username and password is msfadmin.
- So lets generate a small ammount that we can use as an example. 
- let generate length of 8 char with the combination of 'adfimns' char's. so It will contain the username and password 'msfadmin' and store it in largewordlist.txt
```
crunch 8 8 adfimns -o largewordlist.txt
```
- Lets see the size of the wordlist by
```
wc -l largewordlist.txt
```
- And insure that it contains msfadmin by
```
cat largewordlist.txt | grep msfadmin
```
- But as we know, it is a large wordlist and for finding password with bruteforce with this large file will take long time. In order to perform the test, we can make it small by piping and grep
```
crunch 8 8 adfimns | grep 'msfadm' > wordlist.txt
```
- It will have only few word, lets find out.
```
wc -l wordlist.txt
```
So we can use it. 