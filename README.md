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

Step-04
go into the directory in /arch/x86/entry/syscalls/syscall_64.tbl.
and edit a system call 
![step4](https://user-images.githubusercontent.com/125905421/224112656-b4ec7bc0-ce57-4f8a-b4ba-31c9f29425d2.jpg)

Step-05
type gedit include/linux/syscalls.h and paste the prototype of function hello in end of file
![step5](https://user-images.githubusercontent.com/125905421/224113144-a5bb84d9-537d-433b-bd11-d78797eccdde.jpg)

Step-06
changing version and editing hello system call type make file and edit extraversion=-214744
and edit hello/ after core-y
![step6](https://user-images.githubusercontent.com/125905421/224113472-aa6451c8-1bce-4263-bd03-fe588808ce44.jpg)

![step6 2](https://user-images.githubusercontent.com/125905421/224113692-3aba9344-819e-4086-8c5e-d35727ed719a.jpg)

Step-07
type ls /boot |grep config
![step7](https://user-images.githubusercontent.com/125905421/224114035-e8358a03-f2a3-42e7-a660-ce1158f19437.jpg)

![step7 2](https://user-images.githubusercontent.com/125905421/224114206-763bf9ca-653b-400b-947e-7a20b1d185e2.jpg)

copy the config of current kernel into new one

![step7 3](https://user-images.githubusercontent.com/125905421/224114535-d0c986b0-bc4e-4cde-9268-0f235748d6ad.jpg)

Step-08
clean kernel by typing make clean -j2 and then type make -j2

![step8](https://user-images.githubusercontent.com/125905421/224114967-f8ff0cc8-eff5-400f-8dae-139bde777593.jpg)

Step-09
now we have to install kernel
type sudo make modules_install install

![step9](https://user-images.githubusercontent.com/125905421/224115294-1d9149f7-d0c4-427e-aa43-7816cff56fe1.jpg)

now restart by shutdown -r

Step-10
enter uname-r in terminal

![step10](https://user-images.githubusercontent.com/125905421/224115544-5c7ccc29-7f7e-4250-913c-cf748337a8ef.jpg)

Step-11
make a userspace file and type the following code in screenshot

![step11](https://user-images.githubusercontent.com/125905421/224115804-197fc437-bfc9-44de-ae74-c1b87086b3a4.jpg)

![step12](https://user-images.githubusercontent.com/125905421/224115927-2b6b3ae6-5b75-45fb-b2dd-d4999981232b.jpg)

![step13](https://user-images.githubusercontent.com/125905421/224116051-967626e2-53cb-45a4-a631-2f386fdaa16a.jpg)


