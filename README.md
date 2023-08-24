# 1-Up TunnelTalk: A Python Chatroom
- Topics Discussed Websockets, Threading and nGrok

# To Use This Repo
1.  Download and Sign Up for nGrok @ [https://ngrok.com/](https://ngrok.com/)
2.  Add ngrok to your PATH
3.  Connect your Account to your nGrok Install `ngrok config add-authtoken YOUR_TOKEN`
4.  Clone the Repo
5.  On the Host/Server run the server.py `python server.py`
6.  On the Host/Server in another terminal run nGrok `ngrok tcp 65432`
7.  Find the Forawrding address for your nGrok and change the SERVER/PORT in chat.py accordingly
7.  On the Client(s) run the chat.py `python chat.py`
8.  Enjoy Chatting