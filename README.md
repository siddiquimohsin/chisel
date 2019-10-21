# QUAID CORE
### Designed by Muhammad Mohsin siddiqui
First of all get started by cloning this repository on your machine.  
```ruby
git clone https://github.com/siddiquimohsin/chisel.git
```
Create a .txt file and place the ***hexadecimal*** code of your instructions simulated on ***Venus*** (RISC-V Simulator)\
Each instruction's hexadecimal code must be on seperate line as following. This program consists of 9 instructions.
```
00500113
00500193
014000EF
00120293
00502023
00002303
00628663
00310233
00008067
```
Then perform the following step
```ruby
cd Quaid_core/src/main/scala/datapath
```
Open **InstructionMem.scala** with this command. You can also manually go into the above path and open the file in your favorite text editor.
```ruby
open InstructionMem.scala
```
Find the following line
``` python
loadMemoryFromFile(mem, "/Users/mbp/Desktop/data.txt")
```
Change the .txt file path to match your file that you created above storing your own program instructions.\
After setting up the InstructionMem.scala file, go inside the Nano-H folder.
```ruby
cd practice/Quaid_core
```
And enter
```ruby
sbt
```
When the terminal changes to this type
```ruby
sbt:Quaid_core>
```
Enter this command
```ruby
sbt:Quaid_core> test:runMain datapath.Launcher Top
```
After you get success
```ruby
sbt:Quaid_core> test:runMain datapath.Launcher Top --backend-name verilator
```
After success you will get a folder ***test_run_dir*** on root of your folder. Go into the examples folder inside.\
There you will find the folder named Top. Enter in it and you can find the Top.vcd file which you visualise on **gtkwave** to\
see your program running.
