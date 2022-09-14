# Batch Language
介紹Batch File的語法與應用

## 常用指令
### ECHO **(顯示字串)**

```
ECHO Hello
```
![demoecho](res/demoecho1.png)

#### ECHO off  **(所下的指令不會顯示)**
#### @ECHO off **(指令前加@也不會顯示該指令)**
#### ECHO on  **(恢復顯示指令)**

```
ECHO Hello
ECHO off
ECHO Hi, EveryBody
ECHO on
ECHO Good morning!
```
![demoecho](res/demoecho2.png)

### REM **(註解)**

REM是個指令所以用REM的方式註解如果沒有下ECHO off, 此時會把所寫的註解顯示出來. <br>

可用 :: 替代REM, 就可以不用下ECHO off狀態下也不會顯示出註解<br>

```
REM 顯示Hello
ECHO Hello 	
:: 不顯示指令, 連ECHO也不顯示
@ECHO off
REM 只會顯示Hi, EveryBody
ECHO Hi, EveryBody
ECHO on
:: 恢復顯示指令功能, :: 用的註解不會顯示出來
ECHO Good morning!
```
![demoecho](res/demoecho3.png)


### PAUSE **(暫停)**



### IF

比較運算子:<br>
EQU - 等於<br>
NEQ - 不等於<br>
LSS - 小於<br>
LEQ - 小於或等於<br>
GTR - 大於<br>
GEQ - 大於或等於<br>
