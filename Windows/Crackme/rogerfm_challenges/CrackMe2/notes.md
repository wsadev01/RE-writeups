# Metadata
-------------------
Name: CrackMe2<br>
Extension: <i>exe</i><br>
MD5: 23623873E18A02E69178F806E2172D14<br>
Packed: False<br>
PEiD 0.95: MASM32/TASM32<br>
CFF Explorer: TASM/MASM<br>
Disassembler: Ida freeware 7.0<br>
<br>
# Observations<br>
1) It looks more obfuscated than the first one<br>
2) The username must be at least 4 characters<br>
3) UPDATE: Indeed, there is a strlen in the function sub_40117F<br>
4) With ida, i can see that what seems to be an array of 11 characters are being pushed<br>
&emsp;<i>(push offset dword_403015 - at Offset 0x00401194)<br>
5) UPDATE: The 11 characters array is the reserved array for the username<br>
6) At offset 0x00401200 <i>(a.k.a sub_40117F+81h)</i> it is compared eax with ebx, i assume ebx is the serial number... we will see if that assumption is right.<br>
7) Update, i found the password by changing the zero flag, therefore the binary behave like i wanted to popping out the password. Also found a number (3570), i assume this is the serial that i talked about... but respecting to username i just found a compare between eax and number 0 (0x30 in hex), lets try it...<br>
8) UPDATE: It is not that the username, there is some weird increment and decrement part of the code, that runs almost 8 times, lets analyze that part.. (Offset 0x004011CF)<br>
9) UPDATE: I believe that that thing, does not run 8 times, it runs in function of the length of the username input, i believe that this is a for loop.<br>
10)LAST UPDATE: Ok so, i realized, this can be cracked with a keygen but i will do it later, just change the Zero Flag on you debugger and make the program to show the password, solved but not completely cracked, i will upload that later and make a video explaining how i do that keygen
