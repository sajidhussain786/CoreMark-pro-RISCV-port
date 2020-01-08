# CoreMark-pro-RISCV-port
RISCV port of coremark-pro embedded microprocessor benchmark 

To build give the name of target like "linux64". Inside the util/make/linux64.mak change the toolchaine link to point to required toolchain.mak file (like gcc or riscv toolchain). Using util/make/gcc-cross-linux file i have created a gcc-cross-ricv.mak and refer it into linux64.mak file to build RISCV compatible benchmarks. 
Note: In gcc-cross-ricv.mak you need to set the variables "TOOLS" and "TPREF" to point to your installed cross compiler directory. 

Then in parent directory run the command

$       make TARGET=linux64 build

 to make build the benchmarks
or 

$   make TARGET=linux64 XCMD='-c4' certify-all

you can change the link commnet/uncomment link to point ot your required toolchain for compiling the source code files and then run those benchmarks using appropriate simulator.
