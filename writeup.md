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

### Name :- GDB Test Drive

#### Difficulty - Easy (Classified as Medium)
Follow the instructions given in the description.

**Flag** :  picoCTF{d3bugg3r_dr1v3_197c378a}


---

### Name :- unpackme

#### Description :- Can you get the flag? Reverse engineer this binary.
#### Difficulty - High Medium

For this , We first unpack the binary using upx tool and then use Ghidra to analyze the logic of the main function.
We can see its a if statement which results in the flag when executed with the correct number which can be seen in the code. using that number and executing that binary will result in the flag.

**Flag** : picoCTF{up><_m3_f7w_e510a27f}

---
### Name :- bbbbloat

#### Description :-  Can you get the flag? Reverse engineer this binary.
#### Difficulty - Easy(Classified as Medium) 
Same as the previous case, analyzing the functions on ghidra reaveals the number and using that number we can retrieve the flag.

**Flag** : picoCTF{cu7_7h3_bl047_695036e3}

---
### Name :- ARMssembly 0

#### Description :- What integer does this program print with arguments 4134207980 and 950176538? File: chall.S Flag format: picoCTF{XXXXXXXX} -> (hex, lowercase, no 0x, and 32 bits. ex. 5614267 would be picoCTF{0055aabb})
#### Difficulty - Medium

Analyzing the func1, it returns the greater number, so converting the greater number into hex and formatting it to the correct flag format solves the question .

**Flag** : picoCTF{f66b01ec}

---
### Name :- Ready Gladiator 0

#### Description :- Can you make a CoreWars warrior that always loses, no ties? Your opponent is the Imp. The source is available here. If you wanted to pit the Imp against himself, you could download the Imp and connect to the CoreWars server like this: nc saturn.picoctf.net 55249 < imp.red

#### Difficulty - Upperend of easy (Classified as Medium)

imp ex is a core war warrior that does nothing using mov 0 0 it copies itself to the same spot forever never moves never attacks always loses every single match guaranteed


**Flag** : picocTF{h3r0_t0_z3r0_4m1r1gh7_e476d4cf}

---

### Name :- vault-door-3

#### Description :-  This vault uses for-loops and byte arrays. The source code for this vault is here: VaultDoor3.java

#### Difficulty - Meidum 

looking at the file, we can edit the code by trying to creating a new variable which satisfies every if statement in printing the required buffer and that buffer is the flag.

**Flag** : picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c79a21}

---
### Name :-packer

#### Description :-  Reverse this linux executable? binary 
#### Difficulty :- Upperend of Easy (Classified as Medium)
Unpacking the file using upx and analyzing it using ghidra will show this code block

```
  if (iVar3 == 0) {
    *(undefined8 *)(puVar4 + -0x78) = 0x401f57;
    puts(
        "Password correct, please see flag: 7069636f4354467b5539585f556e5034636b314e365f42316e345269 33535f62646438343839337d"
        );
    *(undefined8 *)(puVar4 + -0x78) = 0x401f63;
    puts(local_88);
  }
  else {
    *(undefined8 *)(puVar4 + -0x78) = 0x401f71;
    puts("Access denied");
  }
```
converting that flag to ascii chars reveals the flag.

**Flag** : picoCTF{U9X_UnP4ck1N6_B1n4Ri3S_bdd84893}


---

### Name :- Bit-O-Asm-1

#### Description :- Can you figure out what is in the eax register? Put your answer in the picoCTF flag format: picoCTF{n} where n is the contents of the eax register in the decimal number base. If the answer was 0x11 your flag would be picoCTF{17}.
#### Difficulty :- Easy (Classified as Medium)

In the dumped code, eax register is being inserted by 0x30 which is 48 in decimal 

**Flag** : picoCTF{48}

---

### Name :- Bit-O-Asm-2

#### Description :- Can you figure out what is in the eax register? Put your answer in the picoCTF flag format: picoCTF{n} where n is the contents of the eax register in the decimal number base. If the answer was 0x11 your flag would be picoCTF{17}. Download the assembly dump here.
#### Difficulty :- Easy (Classified as Medium)

In the dumped code, `0x9f1a` which is hexadecimal of 654874 is getting moved into `DWORD PTR [rbp-0x4]` which itself is getting moved in register `eax`

**Flag** : picoCTF{654874}

---

### Name :- Bit-O-Asm-3

#### Description :- Can you figure out what is in the eax register? Put your answer in the picoCTF flag format: picoCTF{n} where n is the contents of the eax register in the decimal number base. If the answer was 0x11 your flag would be picoCTF{17}. Download the assembly dump here.
#### Difficulty :- Easy(Classified as Medium)

- `0x9fe1a` is getting moved to `DWORD PTR [rbp-0xc]`
- `DWORD PTR [rbp-0xc]` is getting moved to `eax`

so now eax := `0x9fe1a`

now multiplication is performed on `eax` from `DWORD PTR [rbp-0x8]` which has a value of `0x4` 

now eax:= 2619448

adding `0x1f5` to eax will give the final `eax` value.which equals to 2619997

**Flag** :- picoCTF{2619997}
 

--- 

### Name :-  Picker I

#### Description :- This service can provide you with a random number, but can it do anything else? Connect to the program with netcat: $ nc saturn.picoctf.net 64700 The program's source code can be downloaded here.
#### Difficulty :- Easy (Classified as Medium )

Reverse Engineering the source code, we can see that it executes the function that matches our input string, so we can execute win and print the flag and then  convert it to ascii chars.

**Flag** :- picoCTF{4_d14m0nd_1n_7h3_r0ugh_ce4b5d5b}

---


### Name :- keygenme-py

#### Description :- keygenme-trial.py
#### Difficulty - Easy (Classified as Medium) 

Adjusting the code to print the required license key , you can do it by altering the check_key() function.

**Flag** :- picoCTF{1n_7h3_|<3y_of_54ef6292}


---
### Name :-  Picker II

#### Description :- Can you figure out how this program works to get the flag? Connect to the program with netcat: $ nc saturn.picoctf.net 54332 The program's source code can be downloaded here.
#### Difficulty :- Medium

As win string is filtered from getting called, we can use ascii chars and call the function. using the following input
`globals()[''.join(map(chr,[119,105,110]))]` to get the flag .

**Flag** :-  picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_95d44590}

---

### Name :- Fresh Java

#### Description :- Can you get the flag? Reverse engineer this Java program.
#### Difficulty :- Easy (Classified as Medium)

Using ghidra, you can decompile the file and see that there is a if block checking the key indexes, you can form the flag by combining those if check statements.

**Flag** :-  picoCTF{700l1ng_r3qu1r3d_738cac89}

---

### Name :- bloat.py

#### Description :- Can you get the flag? Run this Python program in the same directory as this encrypted flag.
#### Difficulty :- Medium

Analyzing the python code, you can see the required code to be `happychance` , its just pure bloated to make us confuse. 

**Flag** :-  picoCTF{d30bfu5c4710n_f7w_b8062eec}

---

### Name :- GDB baby step 1

#### Description :- Can you figure out what is in the eax register at the end of the main function? Put your answer in the picoCTF flag format: picoCTF{n} where n is the contents of the eax register in the decimal number base. If the answer was 0x11 your flag would be picoCTF{17}. Disassemble this.
#### Difficulty :- Easy (Classified as medium) 

Opened the file using ghidra and the flag is getting returned by the main function in the decompiler

Using gdb, you can disassemble main and analyze what value is being set to register `eax`. 

**Flag** :- picoCTF{549698}

---  
### Name :- GDB baby step 2

#### Description :- Can you figure out what is in the eax register at the end of the main function? Put your answer in the picoCTF flag format: picoCTF{n} where n is the contents of the eax register in the decimal number base. If the answer was 0x11 your flag would be picoCTF{17}. Debug this.

Opened the file using ghidra and found the main funciton, run that function in a compiler to get the return value .

**Flag** :- picoCTF{307019}


---

### Name :- timer

#### Description :- You will find the flag after analysing this apk Download here.
#### Difficulty :- Easy (Classified as Medium) 
Using jadx-gui, analyze the apk and search for the flag using `picoCtf` .

**Flag** :- picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}

---

### Name :- vault-door-4

#### Description :- This vault uses ASCII encoding for the password. The source code for this vault is here: VaultDoor4.java
#### Difficulty :-  Easy (Classified as Medium)

Open the java file and convert the text in different bases to ascii chars to get the flag.

**Flag** :- picoCTF{jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b}

---

### Name :- vault-door-5

#### Description :- In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: VaultDoor5.java
#### Difficulty :- Easy (Classified as Medium)


It has two encodings, base64 and url encoding. use decoders for both and you get the flag. 

**Flag** :- picoCTF{c0nv3rt1ng_fr0m_ba5e_64_84fd5095}

---

### Name :- vault-door-6

#### Description :- This vault uses an XOR encryption scheme. The source code for this vault is here: VaultDoor6.java
#### Difficulty :- Easy (Classified as Medium)

It has xor encryption over hex encoding, and analyzing the source code, we can see that the xor value is `0x55`.


**Flag** :- picoCTF{n0t_mUcH_h4rD3r_tH4n_x0r_3ce2919}

---

### Name :- Picker III

#### Description :- Can you figure out how this program works to get the flag? Connect to the program with netcat: $ nc saturn.picoctf.net 51076 The program's source code can be downloaded here.

#### Difficulty - Medium 

Upon analyzing the source code, we can see that read_variable can return the function we want to, so i changed the read_variable varible to return win , and then we get a ascii values which we can convert to ascii chars
 
**Flag** :-  picoCTF{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_226dd285}

--- 
