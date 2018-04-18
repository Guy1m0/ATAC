# Writeup for Reverse Engineering Challenge

## Step1
Try to run this executible file
## Step2
Use disassembler to find more information about that. (Recommend: IDA pro with decompiler)
## Step3
* After reading this code, we know that this code is used to check the content of a file whether equals to assigned words.
* So, we need to find this file's name first and create this file, and then try to figure out target words, and write these words into this file.
* The code below shows that file's name is "EthicalHacking". 
* ![](http://ooj03jwxf.bkt.clouddn.com/ethical.jpg)
## Step4
* Accoding to the code, we need to write down "entereky" into the file EthicalHacking
* ![keygen](http://ooj03jwxf.bkt.clouddn.com/enterkey.png)

* According to the code below, Caesar cipher is used to protect the real words. For the first 10 characters, it turns c to a, d to b, etc. For the last 8 characters, they are base64 encoded. In terms of the rest letters, each letter should trace forward, which means a turns to be b, b turns to be c, etc. So the final word is "secretuseryoucannotgetthispassword11235813" . We need to write down this value in the file EthicalHacking.
![](http://ooj03jwxf.bkt.clouddn.com/psd.jpg)
* Run this file again "sudo.exe EthicalHacking"
And the picture shows that "secretuseryoucannotgetthispassword11235813" is the password we are looking for.
