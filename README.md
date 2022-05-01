### 目錄
* [Crypto](#crypto)
* [MISC](#misc)
* [工具](#工具)
* [程式碼](#程式碼)
---
# Crypto
### Bugku CTF
|[連結](https://ctf.bugku.com/challenges/index/gid/1/tid/6.html)||||||
|:-:|:-:|:-:|:-:|:-:|:-:|
|/.-|聰明的小羊|ok|[+-<>]|你喜歡下棋嗎|easy_crypto|
|7+1+0|簡單加密|散亂的密文|.?!|一段Base64|奇怪的密碼|
|告訴你個秘密|這不是md5|貝斯家族|進制轉換|affine||
### OverTheWire Natas
* [連結](https://overthewire.org/wargames/natas/natas0.html)
* natas0 ~ natas10
---
# MISC
|[連結](https://ctf.bugku.com/challenges/index/gid/1/tid/4.html)|持續增加中...||||
|:-:|:-:|:-:|:-:|:-:|
|[1和0的故事](1和0的故事.txt)|[這是一張單純的圖片](這是一張單純的圖片.jpg)|[telnet](telnet.zip)|[眼見非實](眼見非實.zip)|[啊噠](啊噠.zip)|
|[隱寫1](https://github.com/gemini910610/ctf/blob/main/隱寫.rar)|[隱寫2](https://github.com/gemini910610/ctf/blob/main/隱寫2.jpeg)|[隱寫3](https://github.com/gemini910610/ctf/blob/main/隱寫3.png)|[花點流量聽聽歌](https://github.com/gemini910610/ctf/blob/main/花點流量聽聽歌.mp3)||
---
# 工具
* [Winhex](https://x-ways.net/winhex/)
* [Burp suite](https://portswigger.net/burp/releases/professional-community-2022-3-6?requestededition=community&requestedplatform=)
* [密碼分析](https://www.dcode.fr/cipher-identifier)
* [循序解碼](https://cryptii.com/)
* [AES/DES解碼](https://tool.oschina.net/encrypt)
* [摩斯密碼mp3解碼](https://morsecode.world/international/decoder/audio-decoder-adaptive.html)
* [因式分解](http://factordb.com/)
* Convert.exe[下載](http://down.99u2.com:8099/down/Converter.rar)
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
