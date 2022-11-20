# Client2
hi
import zmq

context= zmq.Context()
socket=context.socket(zmq.REQ)
socket.connect("tcp://127.0.0.1:12345")

while True:
    
    msg= input('You:   ')
    socket.send(msg.encode())
    smsg= socket.recv()
    print('From Resposta : ',smsg.decode())
    print('')
    
