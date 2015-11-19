# networkChat
Chat program running over TCP/IP

## Setup
To run the Dicrectory Server program, compile Directory.java, DirectoryThread.java,
ExpectedPacket.java and User.java, then run Directory.class. No further interaction with the
directory program is necessary.
To run the combination P2PClient and P2PServer program, compile Connection.java, Host.java,
HostConnectionHandler.java, and HostConnectionReceiver.java, then run Host.class. The
program is always in one of 3 states: offline, in their chatroom, or in another user’s chatroom.
The user will start in the offline state.

### Offline

When a user is Offline, they can select one of 3 options:

- **ONLINE:** Will prompt the user for a nickname, and will then place the user into their chatroom,
making themselves available for other users to join.
- **QUERY:** Will return a list of online users, with the following information, in order:
Nickname;
IP Address;
Server Protocol Port;
Chatroom Rating;
Current Chatroom;
Time Entered Current Chatroom
- **EXIT:** Will terminate the program

### In their chatroom

When a user is in their chatroom, they can enter messages to send to all other users in their
chatroom, or can select one of 3 options:
- **QUERY:** Same as above.
- **JOIN:** Will prompt the user for the nickname of the user whose chatroom they wish to join. All
other users in the chatroom will be kicked out, and the user will leave their chatroom band join
the chatroom of the specified user.
- **OFFLINE:** All other users in the chatroom will be kicked out, and the user will go offline.

### In another user’s chatroom

When a user is in another user’s chatroom, they can enter messages to send to all other users
in the same chatroom, or can select one of 3 options:
- **QUERY:** Same as above.
- **LEAVE:** The user will leave the current chatroom and return to their chatroom.
- **OFFLINE:** The user will leave the current chatroom and go offline.
