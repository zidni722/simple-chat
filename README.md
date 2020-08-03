# simple-chat

- Type on the terminal ./simple-chat

- Run following command below on console web browser or website client :

# Add user
let socket = new WebSocket("ws://localhost:8080/chat?username=user1");
socket.onmessage = function(event) {
  console.log(`[message] Data received from server: ${event.data}`);
};

Do the same thing for user2, user3, etc.

# Register user to channel chat room
socket.send('{"command": 0, "channel": "channel-talk"}')

Do the same thing with same channel name for user2, user3, etc.

# Send message to the channel
socket.send('{"command": 2, "channel": "channel-talk", "content": "holla!"}')
check message sent on other channel 

# Endpoint
- /chat -> for get all chat (printed on terminal)
- /users -> for get all user 
- /user/{user}/channels -> for get channel list belongs to user 

