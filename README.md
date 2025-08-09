# Technical_Task_SatyaBhaskar
Task: Full-Stack Wallet Authentication using Alchemy Wallet SDK
Goal:
 Implement a full-stack dApp that uses Alchemy Wallet SDK to authenticate users and create wallets, with session persistence across frontend and backend.

Requirements
1. Frontend (React + Vite or Next.js)
Integrate Alchemy Wallet SDK for:


Wallet creation (EOA or Smart Account).


User login/authentication flow.


Sign a random nonce provided by backend for login verification.


Show connected wallet address in UI.


Implement "Login with Wallet" button that triggers SDK authentication.


On successful authentication, send signature to backend for verification.



2. Backend (Node.js / Express)
Expose API endpoints:


GET /auth/nonce → returns a random nonce for signing.


POST /auth/verify → verifies wallet signature against nonce, returns JWT session token.


GET /me → returns user details if JWT token is valid.


Store nonces temporarily (in-memory or Redis).


Store user sessions securely using JWT.


Validate wallet ownership using EIP-191 signature verification (ethers.verifyMessage).



3. Functional Flow
User opens frontend → clicks "Login with Wallet".


Frontend requests nonce from backend (/auth/nonce).


Wallet signs nonce using Alchemy Wallet SDK.


Frontend sends signature to backend (/auth/verify).


Backend verifies signature → issues JWT token.


Frontend stores JWT in memory or localStorage.


User data is fetched via /me endpoint with JWT authentication.


4. Deliverables
Frontend:


React/Next.js project with functional login UI.


Integration with Alchemy Wallet SDK for authentication and wallet creation.


Backend:


Node.js/Express/Fastify server with authentication routes.


Ethers.js for signature verification.


JWT-based session management.






Support both EOA and Alchemy Smart Account wallets.


Store wallet details in a database (PostgreSQL/MongoDB).


Add logout functionality.


Implement role-based access for API endpoints

