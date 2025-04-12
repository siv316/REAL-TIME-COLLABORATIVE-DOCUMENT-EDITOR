# REAL-TIME-COLLABORATIVE-DOCUMENT-EDITOR
"COMPANY":CODTECH IT SOLUTIONS

"NAME":PALURU SIVANI

"INTERN ID":CT04WR46

"DOMAIN":FULL STACK DEVELOPMENT

"DURATION":4 WEEKS

"MENTOR":NEELA SANTOSH

"DESCRIPTION':

The Real-Time Collaborative Document Editor is a full-stack web application that allows multiple users to collaboratively edit documents in real-time. The system is built using a combination of modern web development technologies such as React.js for the frontend, Node.js and Express for the backend, MongoDB for database storage, and Socket.IO to enable real-time bidirectional communication between clients and the server.
At the core of the frontend is React.js, a popular JavaScript library used to build interactive user interfaces. It is paired with Quill.js, a powerful and customizable rich text editor that supports formatting features such as bold, italic, underline, bullet points, and headings. React is used to dynamically render the user interface and manage the application's state, while Quill provides the editing environment that users interact with. The frontend also uses the Socket.IO client library to establish a persistent connection with the backend server, allowing it to send and receive document changes instantly.
On the backend, Node.js is used to handle server-side logic, and Express simplifies the process of setting up server routes and middleware. A Socket.IO server is integrated into the backend, allowing for real-time communication. When a user opens a document, the frontend emits a get-document event along with the document ID. The backend responds by either retrieving the existing document from the MongoDB database or creating a new one if it doesn't exist. The server then sends the document content back to the client via the load-document event.
Once the document is loaded, any changes the user makes in the editor are captured as “deltas” — a data format used by Quill to represent document changes. These deltas are emitted to the server through the send-changes event and then broadcast to all other connected clients in the same document room using the receive-changes event. This mechanism allows all users to see each other's updates in real-time, providing a seamless collaborative editing experience.
In addition to handling real-time updates, the backend also saves the document contents periodically to MongoDB using the save-document event. This ensures that users’ changes are not lost in the event of a disconnection or system failure. MongoDB is well-suited for this kind of task due to its flexibility with storing JSON-like documents, which aligns well with the Quill delta format.
The backend includes a simple Mongoose schema to define how documents are stored in MongoDB. Each document has a unique ID (used as the MongoDB _id) and a data field that holds the Quill delta representing the document’s content. This minimal schema makes the backend efficient and easy to scale.
From a user experience perspective, the app starts by displaying a loading message until the document is fully fetched from the server. Once loaded, users can begin editing. All interactions, including text formatting and typing, are captured and synchronized across all connected users. The interface is kept intentionally clean and focused to allow distraction-free writing and editing.
In summary, this codebase demonstrates a practical and scalable implementation of a collaborative editing tool. It showcases how technologies like React, Socket.IO, and MongoDB can work together to create a real-time web application. Features like live synchronization, automatic document saving, and a rich-text editing environment make this project an excellent foundation for building more complex applications, such as team-based writing tools, code collaboration platforms, or educational note-sharing systems. Future enhancements might include authentication, role-based access control, document versioning, and integration with cloud storage providers.

"OUTPUT":

![Image](https://github.com/user-attachments/assets/d5a43bd2-3779-4f26-b514-60982e1d231a)
