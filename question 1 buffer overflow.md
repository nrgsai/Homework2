# Homework2

Buffer overflow

{

char authorized=0*66;

char usr_pass[16];

cout<<"enter the password:"<<endl;
cin>>authorized;
if (authorized=='1'){

 **char *strcpy(char * authorized ,const char * usr_pass);**
 
cout<<"password is correct"<<endl;

}

**We can enter 15 characters - 16 spaces as input to get the answer (correct password).**

The buffer is defined as a character array of size 16.
We need to pass 16 bytes of character input (8 bytes) for the buffer array.


The return address is stored more than 16 bytes after the start of the buffer.

Since a 16-byte buffer is allocated to it, the remaining bytes are overflowed and placed right next to the return address.

If more than 16 bytes in the pass-user array, the excess overflows in the authorized pointer, then in the control commands,
and finally in the return address.
A variable is entered in the buffer to fill the amount of memory in the stack.
Now more data is entered than the memory is intended for, resulting in a buffer overflow.
Then they enter another variable in the buffer to override the previous value and tell the program what to run.
