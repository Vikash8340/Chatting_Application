# Chatting Application

A simple Java-based chat application with a graphical user interface that allows two users to communicate in real-time.

## Project Structure

```
📂 Chatting Application/
  📄 manifest.mf
  📄 build.xml
  📂 nbproject/
    📄 project.xml
    📄 build-impl.xml
    📄 genfiles.properties
    📄 project.properties
    📂 private/
      📄 private.xml
      📄 private.properties
  📂 build/
    📂 classes/
      📂 icons/
        📄 video.png
        📄 arrow.jpg
        📄 bunty.jpeg
        📄 phone.png
        📄 gaitonde.jpeg
        📄 2.png
        📄 3.png
        📄 logo.png
        📄 1.jpeg
        📄 3icon.png
      📂 chatting/
        📂 application/
          📄 Client.class
          📄 Server$1.class
          📄 Server.class
          📄 Client$1.class
  📂 src/
    📂 icons/
      (same icon files as above)
    📂 chatting/
      📂 application/
        📄 Client.java
        📄 Server.java
```

## Features

- Real-time text messaging between two users
- Clean graphical user interface with:
  - User profile pictures
  - Message timestamps
  - Send button functionality
- Server-client architecture
- Custom message formatting with:
  - Colored message bubbles
  - Proper text wrapping
  - Time display

## How to Run

1. First, start the Server application:
   ```bash
   java chatting.application.Server
   ```

2. Then, start the Client application:
   ```bash
   java chatting.application.Client
   ```

3. The applications will open two separate windows where you can:
   - Type messages in the text field
   - Click "Send" to send messages
   - Received messages will appear in the chat area

## Technical Details

- **Server.java**: 
  - Creates a server socket on port 6001
  - Handles incoming client connections
  - Processes and displays received messages

- **Client.java**:
  - Connects to the server at 127.0.0.1:6001
  - Provides the user interface for sending messages
  - Displays messages from the server

- **Networking**:
  - Uses Java's Socket and ServerSocket classes
  - DataInputStream and DataOutputStream for message transmission

- **GUI**:
  - Built with Swing components
  - Custom message formatting with HTML in JLabels
  - Responsive layout with BoxLayout and BorderLayout

## Requirements

- Java JDK 8 or later
- Basic understanding of Java networking concepts

## Customization

You can easily customize:
- The user interface colors in the source code
- The port number (currently 6001)
- The user names displayed ("Vikash" and "Mayank")
- The profile pictures by replacing the icon files

## Known Issues

- No message history persistence (messages are lost when closing the application)
- No user authentication
- Limited to one-on-one chat

## Future Enhancements

- Add multi-user chat capability
- Implement message history saving
- Add file sharing functionality
- Improve error handling and user feedback

## License

This project is open-source and available for educational purposes.
