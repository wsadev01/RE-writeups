# Metadata 
------------------------
Name: CrackMe1  
Extension: *exe*  
MD5: 4883f8fc77d151454c36145c49f39427  
Packed: False  
PEiD 0.95: MASM32/TASM32  
CFF Explorer:TASM/MASM
Disassembler: Ida freeware 7.0  
  
# Observations
-------------------

## Before Executing it  
  
1) The password is not in cleartext at any moment  
2) At offset 0000008A2 there is a %d, %d is for integer, and the password only accepts integers 
3) UPDATE: It actually was in cleartext, i just did not see it<br>
<br>
<b>This is my methodology for PE</b><i>(.exe) <br>
&emsp;1. Collect metadata (PEiD, PeStudio, CFF Explorer, String overview, etc.)<br>
&emsp;2. Static analysis<br>
&emsp;3. Dynamic analysis</i><br>
