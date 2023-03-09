# assign01kernelprog-NizELITe
assign01kernelprog-NizELITe created by GitHub Classroom

Step-01
after downloading a kernel  extract it  and then go inside the linux folder
create a new folder and name it hello (since we are making a hello world system call)
then go inside that folder

Step-02
open the terminal in folder and make a c code file by typing gedit hello.c
and type the following code
#include <linux/kernel.h>
asmlinkage long sys_hello(void)
{
printk("Hello world\n");
return 0;
}

Step-03
now create a makefile  by typing makefile and put obj-y:=hello.o
![step3](https://user-images.githubusercontent.com/125905421/224109197-ece5ad1f-4695-48e2-8de3-caddfbf907e0.jpg)

