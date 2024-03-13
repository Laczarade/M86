# M86
A MIPS-to-x86 assembly transpiler

## Some notes on implementation
To my knowledge, MIPS assembly has 32 general-use registers. In comparison, x86 only has 8 -- including the Stack Pointer.
As such, it will be necessary to make some compromises.
My implementation will likely allocate a fixed amount of stack memory for the MIPS registers that cannot translate directly to x86 registers.
I acknowledge that the resulting program will run more slowly than an equivalent program using only registers. I will attempt to remedy this in later updates.

The following is a table of MIPS registers and their planned counterparts in x86:
| MIPS | x86 |
| ---- | --- |
| $0   |     |
| $at  | N/A |
| $v0  |     |
| $v1  |     |
| $a0  |     |
| $a1  |     |
| $a2  |     |
| $a3  |     |
| $t0  |     |
| $t1  |     |
| $t2  |     |
| $t3  |     |
| $t4  |     |
| $t5  |     |
| $t6  |     |
| $t7  |     |
| $s0  |     |
| $s1  |     |
| $s2  |     |
| $s3  |     |
| $s4  |     |
| $s5  |     |
| $s6  |     |
| $s7  |     |
| $t8  |     |
| $t9  |     |
| $k0  | N/A |
| $k1  | N/A |
| $gp  |     |
| $sp  | esp |
| $fp  |     |
| $ra  |     |

Note: this table is incomplete.