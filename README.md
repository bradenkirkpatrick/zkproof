# 🔐 zkAuth - Zero-Knowledge Authentication System

A decentralized web application that enables users to prove membership in a group (such as Student, Employee, or VIP Member) without revealing their identity or private data, leveraging Aleo's zero-knowledge proofs for private access verification.

## 📝 Overview

zkAuth demonstrates how zero-knowledge proofs can be used to create privacy-preserving authentication systems. The application allows users to:

1. Select a role (e.g., Student, Employee, VIP Member)
2. Generate a zero-knowledge proof of their role
3. Verify access rights without revealing identity
4. Receive an "Access Granted" or "Access Denied" result with visual feedback

## 🚀 Features

- **Role-based Access Control**: Validate membership in predefined groups
- **Zero-Knowledge Verification**: Prove access rights without revealing identity
- **Client-side Implementation**: No backend needed - all verification happens in the client
- **Realistic ZK Proof Simulation**: Uses simulated Groth16 proofs with proper structure
- **Interactive Animated UI**: Visually engaging proof generation and vault access animation
- **Real-time Progress Tracking**: Step-by-step visualization of the proof generation process

## 💻 Tech Stack

### Backend / ZK Logic
- **Leo**: Aleo's zero-knowledge programming language
- **Web Cryptography API**: For cryptographic operations in browser
- **Simulated ZK Proofs**: Structured similar to Aleo's snarkVM outputs

### Frontend
- **HTML & TailwindCSS**: Modern, responsive UI components
- **JavaScript**: Client-side proof generation and verification
- **GSAP**: Advanced animations for visual feedback
- **Custom Animations**: Interactive vault open/close and verification effects

## 🛠️ Project Structure

```
├── README.md               # Project documentation
├── src/
│   ├── frontend/           # Web interface
│   │   ├── index.html      # Main application with TailwindCSS styling
│   │   └── js/             # JavaScript modules
│   │       └── aleoProof.js # ZK proof generation and verification
│   └── leo/                # Zero-knowledge proof code
│       └── zkAuth.leo      # Leo program for role verification
```

## 🧩 How It Works

1. **Role Selection**: User selects a role (Student, Employee, VIP Member)
2. **Access Request**: User selects the type of access they want to verify
3. **Animated Proof Generation**: 
   - User sees visual feedback of the proof generation process
   - Floating encryption symbols and progress bar show real-time status
4. **Verification Visualization**:
   - A vault animation shows the verification result
   - On success: Vault door opens with sparkle effects
   - On failure: Vault shakes and remains closed
5. **Result Report**: Detailed cryptographic verification report shows proof structure

## 📋 Proof Generation & Verification

The simulated zero-knowledge proof system includes:

- **Key Generation**: Creates simulated Aleo private key, view key, and address
- **Pedersen Commitments**: Hides the user's role in commitment values
- **Groth16 Proof Structure**: Mimics the three-part structure (a, b, c) of zk-SNARKs
- **Private Verification**: Validates access rights without revealing the actual role
- **Proof Report**: Generates detailed verification outputs with circuit information

## 🎨 UI/UX Features

- **Animated Vault**: Visual metaphor for access control with open/close animations
- **Progress Indicators**: Multi-step progress bar showing proof generation stages
- **Floating Encryption Symbols**: Visual representation of cryptography in action
- **Success/Failure Effects**: Sparkles for granted access, shaking for denied access
- **Responsive Design**: Works across different screen sizes
- **Gradient Effects**: Modern visual styling with smooth color transitions

## 🧪 Real-World Use Cases

- **Private access to internal tools/resources**: Verify employee access without exposing their identity
- **Token-gated content**: Allow access to paywalled content based on membership status
- **Anonymous DAO/group participation**: Participate in governance without revealing identity
- **KYC/AML compliance**: Verify regulatory requirements while preserving privacy

## 🏁 Getting Started

1. **Prerequisites**:
   - A modern web browser with JavaScript enabled
   - (Optional) Aleo SDK for running the Leo program

2. **Running the Frontend**:
   - Open `src/frontend/index.html` in a web browser
   - No server setup required - everything runs client-side

3. **Using the Application**:
   - Select your role (Student, Employee, or VIP Member)
   - Choose an access type to request (Student Portal, Employee Dashboard, or VIP Content)
   - Click "Generate Proof & Verify Access"
   - Watch the animated proof generation process
   - See the vault animation show your access result
   - Review the detailed cryptographic proof report

## 📊 Demo Scenarios

For demonstration purposes, try these scenarios:

1. **Access Granted**: Select the same role and access type (e.g., Student role + Student Portal)
2. **Access Denied**: Select different role and access type (e.g., Student role + Employee Dashboard)
3. **Different Visualizations**: Try all combinations to see the different animations

## 🔍 Technical Details

- **Proof Structure**: Follows Aleo's approach to zero-knowledge proofs
- **Key-pair Generation**: Simulates Aleo's key generation process using Web Crypto API
- **Circuit Simulation**: Represents constraints and gates like a real ZK circuit
- **Privacy Guarantees**: Demonstrates zero-knowledge property where verifier learns nothing but validity

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- Aleo for providing the tools for zero-knowledge proofs
- The zero-knowledge proof community for advancing privacy-preserving technologies
- TailwindCSS and GSAP for enabling modern UI/UX