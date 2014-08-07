Simple socket server / client. 
Encrypt data with AES 

Server: 

:> ./pyserv -s 127.0.0.1 1234 
server password: test 
Please use this server password: test000000000000 

password should be 16 simbols, if is not pyserv add 0's or cut it

Client: 

:> ./pyserv -c 127.0.0.1 1234 TEST MSG 
server password: sdf
ERROR: server password should be 16 symbols, current is: 3 
server password: sdfdfssdffdsdfsfdfsddsdfsfdsfsdfdsff 
ERROR: server password should be 16 symbols, current is: 36 
server password: test000000000000 


Result: 

:> ./pyserv -s 127.0.0.1 1234 
server password: test 
Please use this server password: test000000000000 
('Connected by', ('127.0.0.1', 19335)) 
cVU+M5tn/j34rTNPNwxlH3+75mSC7YNZ93k8lrMQh9I= 
loNHQd78KKL78Lf5nfFdNn+75mSC7YNZ93k8lrMQh9I= 
 
['TEST', 'MSG'] 
