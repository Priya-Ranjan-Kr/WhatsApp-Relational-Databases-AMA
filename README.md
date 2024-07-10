
# WhatsApp Product Dissection and Relational Database Schema

## Project Overview

This project analyzes WhatsApp, focusing on its features, real-world problem-solving capabilities, and a relational database schema description.

### Company Overview

WhatsApp, founded in 2009 and acquired by Facebook in 2014, is a leading messaging application with over 2 billion users globally.

### Product Dissection

WhatsApp solves various real-world problems through its features:

- **Instant Communication**: Enables real-time messaging and calls.
- **Cost-Effective International Communication**: Uses internet for calls and messages.
- **End-to-End Encryption**: Ensures message privacy.
- **Business Communication**: Facilitates efficient customer interactions.

### Case Study: Real-World Problems and Solutions

1. **Emergency Situations**: Instant messaging aids in timely communication.
2. **Costly International Communication**: Provides affordable global communication.
3. **Privacy and Security**: Implements end-to-end encryption.
4. **Business Efficiency**: WhatsApp Business enhances customer service.

### Top Features of WhatsApp

- Instant Messaging
- Voice and Video Calls
- End-to-End Encryption
- Group Chats
- File and Location Sharing

## Relational Database Schema

### Schema Description

#### User Schema

```plaintext
- user_id (Primary Key)
- phone_number
- display_name
- status_message
- profile_picture

#### **Chat Schema**
- chat_id (Primary Key)
- chat_type
- participants (Many-to-Many)
- last_message
- unread_count


**#### Message Schema**
- message_id (Primary Key)
- chat_id (Foreign Key)
- sender_id (Foreign Key)
- content
- timestamp
- is_read

**Attachment Schema**
- attachment_id (Primary Key)
- message_id (Foreign Key)
- attachment_type

**Relationships**
**User-Chat**: One-to-Many
**Chat-Message**: One-to-Many
**User-Message**: One-to-Many
**Chat-Participant**: Many-to-Many
**Message-Attachment**: One-to-Many
