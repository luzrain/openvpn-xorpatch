# OpenVPN with xorpatch sources

[OpenVPN](https://github.com/OpenVPN/openvpn) with added support for the [Tunnelblick obfuscation](https://tunnelblick.net/cOpenvpn_xorpatch.html) patch.  
Patched OpenVPN can be useful to prevent OpenVPN traffic from being detected by censorship mechanisms, such as in China and Russia.

## Scramble Option Syntax
Note: The "scramble" option and parameters in the server and client configuration files must match.  

`scramble xor_string`  
`scramble xormask xor_string`  
These options XOR the bytes in each buffer with xor_string.  

`scramble reverse`  
The "reverse" option reverses order of the bytes in each buffer (except that the first byte is unchanged). So "abcde" becomes "aedcb".  

`scramble xorptrpos`  
The "xorptrpos" option XORs each byte of the buffer of traffic with the position in the buffer.  

`scramble obfuscate password`  
The "obfuscate" option performs several of the above steps, using password as the xor_string in one of the steps.  
