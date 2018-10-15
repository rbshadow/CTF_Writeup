### 1. Forensics Warmup 1 - Points: 50
→ Can you unzip this file for me and retreive the flag? 

#### Solution: 

1. Download the file and Unzip.
2. Open flag.jpg file. Here found the flag.

### 2. Reversing Warmup 1 - Points: 50
→ Throughout your journey you will have to run many programs. Can you navigate to `/problems/reversing-warmup-1_3_7c0eade7faf60ffe3485e12098e2a6c2` on the shell server and run this program to retreive the flag? 

#### Solution:

1  Access the shell and connect.
2 Login with credentials like teamname and password.
3 Navigate to `/problems/reversing-warmup-1_3_7c0eade7faf60ffe3485e12098e2a6c2` directory with `cd /problems/reversing-warmup-1_3_7c0eade7faf60ffe3485e12098e2a6c2`
4 Check files with ls -l command. Here can see the file has executable permission.
`-rwxr-sr-x 1 hacksports reversing-warmup-1_3 7420 Sep 28 08:34 run`

5 Run the file with `./run`
6 Final flag is: `picoCTF{welc0m3_t0_r3VeRs1nG}`

### 3. Reversing Warmup 2 - Points: 50
Can you decode the following string dGg0dF93NHNfczFtcEwz from base64 format to ASCII? 

#### Solution:

1 Run terminal
2 Run command:   `echo ‘dGg0dF93NHNfczFtcEwz’ | base64 --decode > flag.txt`
3 Run command: `nano flag.txt`
4 Final flag is: `picoCTF{th4t_w4s_s1mpL3}`

### 4. Crypto Warmup 1 - Points: 75
Crpyto can often be done by hand, here's a message you got from a friend, llkjmlmpadkkc with the key of thisisalilkey. Can you use this table to solve it?. 

#### Solution:

1. Download the table and open. table file contain a table of letter A-Z which can be a clue that flag can be encrypted with Vigenere Cipher. 
2. A key supplied with the question which can be helpful to get the flag.
3. Go to https://www.dcode.fr/vigenere-cipher to decode.
4. Copy  llkjmlmpadkkc and paste to the text field and write the key in key portion.
5. Left side we can see a text which is: `secretmessage`.
6. Final flag is: `picoCTF{SECRETMESSAGE}` [Flag will be in capital format mentioned is the HINTS]

### 5. Crypto Warmup 2 - Points: 75
Cryptography doesn't have to be complicated, have you ever heard of something called rot13? `cvpbPGS{guvf_vf_pelcgb!} `

#### Solution:

1. Goto https://cryptii.com/ 
2. Select **rot13** of middle option and select decode
3. Cope the `cvpbPGS{guvf_vf_pelcgb!}` and paste it to the left section
4. Final flag is: `picoCTF{this_is_crypto!}`


### 6. HEEEEEEERE'S Johnny! - Points: 100
Okay, so we found some important looking files on a linux computer. Maybe they can be used to get a password to the process. Connect with nc 2018shell2.picoctf.com 42165. Files can be found here: passwd shadow. 
Hints: 
If at first you don't succeed, try, try again. And again. And again. 
If you're not careful these kind of problems can really "rockyou". 


#### Solution:

1. Download passwd and shadow file.
2. Run command from terminal: `/usr/bin/unshadow passwd shadow > pass.txt`
3. Download rockyou.txt wordfile to crack the password
4. Run command: `sudo john --wordlist=rockyou.txt pass.txt`
5. Output should be: 

~~~~bash
Created directory: `/root/.john`
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
thematrix        (root)
1g 0:00:01:04 100% 0.01553g/s 171.5p/s 171.5c/s 171.5C/s jemjem..davida
Use the "--show" option to display all of the cracked passwords reliably
Session completed
~~~~


6. So the password is _**thematrix**_ for user root
7. Run  `nc 2018shell2.picoctf.com 42165`
8. Enter username as root and password as thematrix
9. Final flag is: `picoCTF{J0hn_1$_R1pp3d_5f9a67aa}`

### 7. pipe - Points: 110
During your adventure, you will likely encounter a situation where you need to process data that you receive over the network rather than through a file. Can you find a way to save the output from this program and search for the flag? Connect with 2018shell2.picoctf.com 37542. 

#### Solution:

1. Run command: `nc  2018shell2.picoctf.com 37542 | pico`
2. Final flag is: `picoCTF{almost_like_mario_a6975cdb}`

### 8. grep 2 - Points: 125
This one is a little bit harder. Can you find the flag in `/problems/grep-2_4_06c2058761f24267033e7ca6ff9d9144/files` on the shell server? Remember, grep is your friend. 

#### Solution:

1. Go to shell. 
2. Go to `/problems/grep-2_4_06c2058761f24267033e7ca6ff9d9144/files` directory with cd.
3. Type command: `grep -Rin pico *`
4. Final flag is: `picoCTF{grep_r_and_you_will_find_036bbb25}`

### 9. admin panel - Points: 150 
We captured some traffic logging into the admin panel, can you find the password? 

#### Solution: 

1. Download traffic file which is a pcap
2. Open `traffic.pcap` file with wireshark
3. Select a HTTP protocol packet. Right click and select Follow HTTP Stream
4. Final flag is: `picoCTF{n0ts3cur3_df598569}`

### 10. caesar cipher 1 - Points: 150
This is one of the older ciphers in the books, can you decrypt the message? You can find the ciphertext in `/problems/caesar-cipher-1_3_160978e2a142244574bd048623dba1ed` on the shell server. 

#### Solution:

1. Download the message file.
2. Go to _https://dcode.fr/caesar-cipher_ and paste the text of message file
3. Select test all possible solution and click Decrypt
4. Left side you can find the flag.
5. Final flag is: `picoCTF{justagoodoldcaesarcipherwoyolfpu}`

### 11. hertz - Points: 150
Here's another simple cipher for you where we made a bunch of substitutions. Can you decrypt it? Connect with `nc 2018shell2.picoctf.com 48186`. 

#### Solution:

1. Connect  `nc 2018shell2.picoctf.com 48186` from terminal
2. Copy the response text. It’s substitution cipher text.
3. Go to _https://guballa.de/substitution-solver_
4. Paste the copied text.
5. Final flag is: `picoCTF{substitution_ciphers_are_solvable_vmlvpvmcwr}`

### 12. hex editor - Points: 150
This cat has a secret to teach you. You can also find the file in `/problems/hex-editor_1_10cafee5618ce2cfe32f2188ca1f472e` on the shell server. 

#### Solution:

1. Download the cat file which is hex-editor.jpg
2. Let’s search string from terminal. Type: `strings hex-editor.jpg | grep pico`
3. Final flag is: `picoCTF{and_thats_how_u_edit_hex_kittos_4bE5aCb8}`

### 13. Truly an Artist - Points: 200
Can you help us find the flag in this Meta-Material? You can also find the file in `/problems/truly-an-artist_0_4f3e3848bbbfc5cfcfa404bd18b8ac96`. 

#### Solution:

1. Download the Meta-Material file.
2. Check with exitftool. Command: `exifftool 2018.png`
3. Final flag is: `picoCTF{look_in_image_788a182e}`

### 14. Now you don't - Points: 200
We heard that there is something hidden in this picture. Can you find it? 

#### Solution:
1. Download the picture file.
2. Run `Stegosolver.jar`
3. Open the picture and analyze. 
4. Final flag is: `picoCTF{n0w_y0u_533_m3}`

### 15. What's My Name? - Points: 250 
Say my name, say my name. 

#### Solution
1. Download the `myname.pcap` file
2. Open with wireshark.
3. Select a DNS traffic and follow UDP stream.
4. Final flag is: `picoCTF{w4lt3r_wh1t3_033ad0f914a0b9d213bcc3ce5566038b}`

***

#### Thank you for the great reading.