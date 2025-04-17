### Name :- file-run2

#### Description :- Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"? Download the program here.

#### Difficulty - Easy ( classified as Medium)

Just download the file , give permissions to it to run and give input of "Hello!".

You can also get the flag into your clipboard by using this command

` chmod +x ./run | ./run Hello! | grep -aoE "picoCTF\{[^}]*\}" | xsel --clipboard`


**Flag** : picoCTF{F1r57_4rgum3n7_96f2195f}

--- 

### Name :- Shop

#### Description :- Best Stuff - Cheap Stuff, Buy Buy Buy... Store Instance: source. The shop is open for business at nc mercury.picoctf.net 24851.

#### Difficulty : Medium ( Classified as Medium )

You were given a server to access by netcat `nc mercury.picoctf.net 24851` , but the code doesnt deal with negative numbers well . so if you try to buy negative number of items, you
will get credited with the cost price.you can get 100 using that edge case and buy the flag .

if we convert that flag to its respective ASCII chars , we get our flag.

**Flag** :  picoCTF{b4d_brogrammer_532bcd98}

---

### Name :- Safe Opener

#### Description :- I forgot the key to my safe but this program is supposed to help me with retrieving the lost key. Can you help me unlock my safe? Put the password you recover into the picoCTF flag format like: picoCTF{password}#### Difficulty - Easy (Classified as Medium)

Opening the give file shows us a base64 encoded text . put that into a decoder and it will reveal the flag.

**Flag** : picoCTF{pl3as3_l3t_m3_1nt0_th3_saf3}

--- 

### Name :- unpackme.py

#### Description :- Can you get the flag? Reverse engineer this Python program.
#### Difficulty - Upperend of easy (Classified as Medium)

If you open the python file, you can see that a payload sent to fermet algorithm and plain variable as the decrypted version of that payload.Printing that plain variable reveals the flag.

**Flag** : picoCTF{175_chr157m45_5274ff21}

--- 

### Name :- Reverse

#### Description :- Try reversing this file? Can ya? I forgot the password to this file. Please find it for me?
#### Difficulty - Easy ( Classified as Medium)

The flag is in the source code, you can either grep it or just copy it when you `cat` the file for looking file contents.

**Flag** : picoCTF{3lf_r3v3r5ing_succe55ful_9ae85289}

---

### Name :- Safe Opener 2

#### Description :- What can you do with this file? I forgot the key to my safe but this file is supposed to help me with retrieving the lost key. Can you help me unlock my safe? 
#### Difficulty - Easy (Classified as Medium)

Using grep to find the flag in the file worked.
`cat SafeOpener.class | grep -oaE "picoCTF\{[^}]*\}"`
***Flag** : picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_0e57c117}

--- 
