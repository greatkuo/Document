# INSTALL GCC
## 下載
先去 https://msys2.github.io/ 官網下載Shell安裝<br>
選擇 msys2-x86_64-20220904.exe 安裝, 官網會自動更新成最近檔案<br>
下載完執行安裝檔<br>
當 MSYS2 安裝完成後會有好幾個Shell
## 更新系統
安裝完成後，建議先更新系統。
```
pacman --needed -Sy bash pacman pacman-mirrors msys2-runtime
```
更新後務必重新啟動 MSYS2，否則使用時會發生錯誤。

## 更新套件
套件指的就是在 MSYS2 環境底下的所有軟體，透過 pacman 這個套件管理程式來統一管理，只要下達以下指令，就可以自動更新所有的套件。
```
pacman -Su
```

## 安裝 GCC(Gnu Compiler Collection)
套件前面顯示的就是提供給特定的 Shell 環境使用的版本，以下是我們需要的三個套件：
* mingw-w64-i686-gcc -> MinGW-w64 Win32 Shell
* mingw-w64-x86_64-gcc -> MinGW-w64 Win64 Shell
* gcc -> MSYS2 Shell

透過套件管理程式安裝 GCC

```
pacman -S mingw-w64-i686-gcc
pacman -S mingw-w64-x86_64-gcc
pacman -S gcc
```

可透過gcc --version 來確定安裝是否成功

## 使用 GCC 編譯程式

在 C:\test 資料夾底下新增一個文字檔 hello.c，並且輸入以下程式碼：
```C
#include <stdio.h>
int main() 
{
    printf("Hello, World");
    return 0;
}
```
如果要 MinGW-w64 Win32 Shell  的 Shell 內要切換到C槽，在MSYS2內的對應目錄為 /c
所以切換到 C:\test 底下則必須輸入：

```
cd /c/test
```
## Compiler程式
```
gcc -o hello32 hello.c
```

## 執行程式
```
./hello32
```
