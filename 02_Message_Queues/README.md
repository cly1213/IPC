# message queue
## receiver
```
gcc -g -c recvr.c -o recvr.o
gcc -g recvr.o -o recvr -lrt 

./recvr
provide a reciepient msgQ name : format </msgq-name>

./recvr /msgq1
Reciever blocked on select()....
Msg recvd msgQ /msgq1
Msg recieved from Queue = hello
Reciever blocked on select()....

```

## sender
```
gcc -g -c sender.c  -o sender.o
gcc -g sender.o  -o sender -lrt

./sender
provide a reciepient msgQ name : format </msgq-name>

./sender /msgq1
Enter msg to be sent to reciever /msgq1
hello

```
