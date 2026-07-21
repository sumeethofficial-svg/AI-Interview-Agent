# AI Interview Agent

An AI-powered mock interview platform that conducts realistic, adaptive interviews and gives candidates live, actionable feedback — helping them practice and improve before the real thing.

## ✨ Features

- **AI-Driven Mock Interviews** — Dynamic, role-specific questions generated and adapted in real time based on the candidate's responses
- **Live Streaming Responses** — AI feedback and follow-up questions stream token-by-token via Server-Sent Events (SSE) for a natural, low-latency conversational feel
- **Instant Feedback** — Structured evaluation of answers (clarity, technical accuracy, communication) delivered immediately after each response
- **Secure Authentication** — JWT-based auth for protected user sessions
- **Payments & Subscriptions** — Razorpay integration for premium interview packs / subscription tiers
- **Interview History** — Track past sessions and review progress over time

## 🛠️ Tech Stack

**Frontend**
- React

**Backend**
- Node.js / Express
- MongoDB

**AI & Real-Time**
- OpenAI API
- Server-Sent Events (SSE) for streaming responses

**Auth & Payments**
- JWT (JSON Web Tokens)
- Razorpay

## 🏗️ Architecture

```
Client (React)
   │
   ▼
Express API ──── JWT Auth Middleware
   │
   ├──► OpenAI API (streamed via SSE) ──► Real-time interview Q&A + feedback
   │
   ├──► MongoDB ──► Users, sessions, interview history
   │
   └──► Razorpay ──► Subscription / payment handling
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v18+)
- MongoDB instance (local or Atlas)
- OpenAI API key
- Razorpay API keys

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/ai-interview-agent.git
   cd ai-interview-agent
   ```

2. Install dependencies
   ```bash
   # backend
   cd server
   npm install

   # frontend
   cd ../client
   npm install
   ```

3. Configure environment variables

   Create a `.env` file in `/server`:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   OPENAI_API_KEY=your_openai_api_key
   RAZORPAY_KEY_ID=your_razorpay_key_id
   RAZORPAY_KEY_SECRET=your_razorpay_key_secret
   ```

4. Run the app
   ```bash
   # from /server
   npm run dev

   # from /client, in a separate terminal
   npm run dev
   ```

5. Open `http://localhost:3000` in your browser

## 📖 Usage

1. Sign up / log in
2. Choose an interview role or topic
3. Start the mock interview — the AI asks questions and streams responses live
4. Answer via text (or voice, if enabled)
5. Receive instant, structured feedback after each answer
6. Review your session history to track improvement

## 🗺️ Roadmap

- [ ] Voice-based interview mode
- [ ] Resume-based question personalization
- [ ] Detailed analytics dashboard
- [ ] Multi-language support

## 🤝 Contributing

Contributions are welcome! Please open an issue first to discuss what you'd like to change.

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## 📬 Contact

Sumeeth — feel free to reach out via GitHub Issues or [your preferred contact method].
