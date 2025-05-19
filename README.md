# 🔐 zkAuth - Zero-Knowledge Authentication System

A decentralized web application that enables users to prove membership in a group (such as Student, Employee, or VIP Member) without revealing their identity or private data, leveraging Aleo's zero-knowledge proofs for private access verification.

## 📝 Overview

zkAuth demonstrates how zero-knowledge proofs can be used to create privacy-preserving authentication systems. The application allows users to:

1. Select a role (e.g., Student, Employee, VIP Member)
2. Generate a zero-knowledge proof of their role
3. Verify access rights without revealing identity
4. Receive an "Access Granted" or "Access Denied" result

## 🚀 Features

- **Role-based Access Control**: Validate membership in predefined groups
- **Zero-Knowledge Verification**: Prove access rights without revealing identity
- **Client-side Implementation**: No backend needed - all verification happens on the client
- **Simple UI**: Clean interface for selecting roles and viewing results

## 💻 Tech Stack

### Backend / ZK Logic
- **Leo**: Aleo's zero-knowledge programming language
- **snarkVM**: For proof generation & verification (simulated in this demo)

### Frontend
- **HTML/CSS/JavaScript**: Simple client-side UI
- **No backend required**: All verification happens in the browser

## 🛠️ Project Structure

```
├── README.md               # Project documentation
├── src/
│   ├── frontend/           # Web interface
│   │   └── index.html      # Single-page app with HTML/CSS/JS
│   └── leo/                # Zero-knowledge proof code
│       └── zkAuth.leo      # Leo program for role verification
```

## 🧩 How It Works

1. **Role Selection**: User selects a role (Student, Employee, VIP Member)
2. **Access Request**: User selects the type of access they want to verify
3. **Proof Generation**: A zero-knowledge proof is generated (simulated in this demo)
4. **Verification**: The proof is verified against the required access level
5. **Result Display**: "Access Granted" or "Access Denied" is shown based on verification

## 📋 Leo Program Explanation

The `zkAuth.leo` program contains:

- **AccessCredential**: A struct representing user credentials with role and timestamp
- **AccessRight**: A record representing proven access rights
- **issue_access**: A function that issues access rights to a user
- **verify_access**: A function that verifies access without revealing the role
- **Role-specific checkers**: Functions for verifying specific access rights (student, employee, VIP)

## 🧪 Real-World Use Cases

- **Private access to internal tools/resources**: Verify employee access without exposing their identity
- **Token-gated content**: Allow access to paywalled content based on membership status
- **Anonymous DAO/group participation**: Participate in governance without revealing identity

## 🏁 Getting Started

1. **Prerequisites**:
   - A modern web browser
   - (Optional) Aleo SDK for running the Leo program

2. **Running the Frontend**:
   - Open `src/frontend/index.html` in a web browser

3. **Simulating Proof Generation**:
   - Select a role in the dropdown
   - Select an access type
   - Click "Generate Proof & Verify Access"
   - The result will appear after simulating proof generation

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- Aleo for providing the tools for zero-knowledge proofs
- The zero-knowledge proof community for advancing privacy-preserving technologies