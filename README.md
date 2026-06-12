# chatbot-POE-part-3
final Part of the POE(chatbot)



Part 1: Registration & Login
- **Registration**:
  - First name and last name input.
  - Username must contain an underscore (`_`) and be at most **5 characters**.
  - Password must be at least **8 characters**, with:
    - One capital letter
    - One number
    - One special character
  - South African phone number validation:
    - Must start with +27
    - Must have **9 digits**
    - Implemented using **regular expressions**.
- **Login**:
  - User has **3 attempts** to log in.
  - On success, a **personalised welcome message** is displayed.
- **Validation Methods**:
  - checkUserName()
  - checkPasswordComplexity()
  - checkCellPhoneNumber()
  
  **Part 2: Sending Messages
- After login, the **main menu** appears.
- **Message Sending**:
  - User chooses how many messages to send (using a **for loop**).
  - Each message requires:
    - Recipient number
    - Message text (≤ 250 characters)
  - If exceeded, error shows extra characters.
- **Message Management**:
  - Unique **10-digit Message ID** generated randomly.
  - **Message Hash** format:
    FirstTwoDigitsOfID : MessageNumber : FirstWord : LastWord
    (all uppercase)
  - User options:
    - **Send** → increases sent counter
    - **Discard**
    - **Store** → saves message to JSON file
- **Output**:
  - Displays full details: ID, hash, recipient, and text.
  - Shows total number of sent messages.


##Part 3: Stored Messages & Arrays
- On startup, loads **stored messages** from JSON file into arrays.
- **MessageManager** maintains:
  - Sent messages
  - Disregarded messages
  - Stored messages
- **Features**:
  1. Display sender & recipient of stored messages.
  2. Find longest stored message (string length comparison).
  3. Search by **10-digit Message ID**.
  4. Search by recipient number.
  5. Delete stored message using **message hash**.
  6. Generate full report of all stored messages.
