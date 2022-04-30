### 目錄
* [Crypto](#crypto)
* [MISC](#misc)
* [工具](#工具)
* [程式碼](#程式碼)
---
# Crypto
### Bugku CTF
|<a href="https://ctf.bugku.com/challenges/index/gid/1/tid/6.html" target="_blank">連結</a>||||||
|:-:|:-:|:-:|:-:|:-:|:-:|
|/.-|聰明的小羊|ok|[+-<>]|你喜歡下棋嗎|easy_crypto|
|7+1+0|簡單加密|散亂的密文|.?!|一段Base64|奇怪的密碼|
|告訴你個秘密|這不是md5|貝斯家族|進制轉換|affine||
### OverTheWire Natas
* <a href="https://overthewire.org/wargames/natas/natas0.html" target="_blank">連結</a>
* natas0 ~ natas11
* natas14（密碼：Lg96M10TdfaPyVBkJdjymbllQ5L6qdl1）
---
# MISC
|<a href="https://ctf.bugku.com/challenges/index/gid/1/tid/4.html" target="_blank">連結</a>|持續增加中...||||
|:-:|:-:|:-:|:-:|:-:|
|1和0的故事|這是一張單純的圖片|telnet|眼見非實|啊噠|
---
# 工具
<a href="https://overthewire.org/wargames/natas/natas0.html" target="_blank">連結</a>
* <a href="https://portswigger.net/burp/releases/professional-community-2022-3-6?requestededition=community&requestedplatform=" target="_blank">Burp suite</a>
* <a href="https://cryptii.com/" target="_blank">循序解碼</a>
* <a href="https://www.dcode.fr/cipher-identifier" target="_blank">密碼分析</a>
* <a href="https://x-ways.net/winhex/" target="_blank">Winhex</a>
* Convert.exe<a href="http://down.99u2.com:8099/down/Converter.rar" download>下載</a>
* <a href="https://morsecode.world/international/decoder/audio-decoder-adaptive.html" target="_blank">摩斯密碼mp3解碼</a>
* <a href="http://factordb.com/" target="_blank">因式分解</a>
* <a href="https://tool.oschina.net/encrypt" target="_blank">AES/DES解碼</a>
---
# 程式碼
### Wiener's attack（RSA）
* python
```python
import owiener
c = 0
e = 0
n = 0
d = owiener.attack(e, n)
print(d)
```
### 文字轉ASCII
* python
```python
string s = 'AAAAAAA'
for t in s:
    print(ord(t), end=' ')
```
* c++
```cpp
string s = "AAAAAAA";
for(char c : s)
{
    cout << int(c) << " ";
}
```
* java
```java
String s = "AAAAAAA";
for(int i = 0;i < s.length();i++)
{
    System.out.print((int)s.charAt(i) + " ");
}
```
### ASCII轉文字
* python
```python
s = '65 66 67 68 69'
t = s.split(' ')
for u in t:
    print(chr(int(u)), end='')
```
* c++
```cpp
#include <cstring>
char s[] = "65 66 67 68 69";
char* t = strtok(s, " ");
while(t != NULL)
{
    cout << char(stoi(t));
    t = strtok(NULL, " ");
}
```
* java
```java
String s = "65 66 67 68 69";
String t[] = s.split(" ");
for(String u : t)
{
    System.out.print((char)Integer.parseInt(u));
}
```
