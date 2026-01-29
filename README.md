
# Smart Do Journey 🚀

A modern, gamified and intelligent todo application built with React, TypeScript, Supabase, and AI. Transform your daily tasks into an engaging journey with XP, levels, streaks, beautiful animations, and AI-powered suggestions.


## ✨ Features

### 🎯 Core Functionality
- **Task Management**: Create, edit, delete, and organize tasks with categories and priorities
- **Smart Categories**: Personal, work, shopping, and custom categories
- **Priority System**: High, medium, and low priority levels
- **Date & Time**: Set start/end dates, times, and reminders
- **Voice Input**: Speech-to-text task creation
- **AI Suggestions**: Gemini AI and OpenAI-powered task suggestions and priority
- **Real-time Sync**: Live updates with Supabase backend

### 🎮 Gamification
- **XP System**: Earn experience points for completing tasks
- **Level Progression**: Level up as you complete more tasks
- **Streak Tracking**: Maintain daily task completion streaks
- **Confetti Celebrations**: Visual rewards for task completion

### 🎨 User Experience
- **Dark/Light Theme**: Toggle between themes
- **Multiple Color Themes**: Ocean, Forest, Sunset, and more
- **Responsive Design**: Works seamlessly on desktop and mobile
- **Animated Backgrounds**: Beautiful visual effects
- **Blast Effects**: Satisfying animations for task completion
- **Responsive Sidebar**: Easy navigation and task filtering

### 🔐 Authentication & Data
- **Supabase Integration**: Secure user authentication and data storage
- **Guest Mode**: Try the app without signing up
- **Data Sync**: Tasks sync across devices for authenticated users
- **Local Storage**: Offline support for guest users


## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern React with hooks and functional components
- **TypeScript** - Type-safe development
- **Vite** - Fast build tool and dev server
- **React Router** - Client-side routing
- **React Query** - Server state management
- **shadcn/ui** - Beautiful, accessible UI components
- **Radix UI** - Headless UI primitives
- **Lucide React** - Beautiful icons
- **Tailwind CSS** - Utility-first CSS framework

### Backend & Database
- **Supabase** - Open-source Firebase alternative
- **PostgreSQL** - Reliable database
- **Row Level Security** - Secure data access
- **Supabase Edge Functions** - AI-powered priority suggestions (OpenAI)
- **Gemini API Server** - Node.js Express server for Gemini AI suggestions

### Development Tools
- **ESLint** - Code quality and consistency
- **PostCSS** - CSS processing
- **TypeScript ESLint** - TypeScript-specific linting


## 🚀 Getting Started

### Prerequisites
- **Node.js** 18+ and npm
- **Git** for version control

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd smart-do-journey
   ```

2. **Install dependencies**
   ```bash
   cd client && npm install
   cd ../server && npm install
   ```

3. **Set up environment variables**
   - For the frontend, create a `.env` file in `client/`:
     ```env
     VITE_SUPABASE_URL=your_supabase_url
     VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
     ```
   - For the server, create a `.env` file in `server/`:
     ```env
     GEMINI_API_KEY=your_gemini_api_key
     PORT=3000
     ```

4. **Start the development servers**
   - Frontend:
     ```bash
     cd client
     npm run dev
     ```
   - Backend (Gemini server):
     ```bash
     cd ../server
     npm start
     ```



## 📱 Available Scripts

### Frontend (client/)
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run build:dev` - Build for development
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Backend (server/)
- `npm start` - Start the Gemini server
- `npm run dev` - Start in development mode

src/

## 🏗️ Project Structure

```
smart-do-journey/
├── client/                 # React frontend application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── contexts/       # React contexts (Auth, etc.)
│   │   ├── hooks/          # Custom React hooks
│   │   ├── integrations/   # External service integrations
│   │   ├── pages/          # Application pages
│   │   ├── types/          # TypeScript type definitions
│   │   └── lib/            # Utility functions
│   ├── public/             # Static assets
│   └── package.json        # Frontend dependencies
├── server/                 # Gemini AI Node.js backend
│   ├── gemini-server.js    # Gemini API Express handler
│   └── package.json        # Backend dependencies
├── supabase/               # Database and edge functions
│   ├── functions/          # Supabase Edge Functions (OpenAI)
│   └── config.toml         # Supabase configuration
└── README.md               # Project documentation
```


## 🔧 Configuration

### Supabase Setup
1. Create a new project at [supabase.com](https://supabase.com)
2. Get your project URL and anon key
3. Add them to your `.env` file in `client/`
4. Set up the database schema (see `supabase/` directory)

### Supabase Edge Functions
- The project includes a function for AI priority suggestions using OpenAI. See `supabase/functions/ai-priority-suggestion/`.
- Deploy with:
   ```bash
   supabase functions deploy ai-priority-suggestion
   ```

### Gemini AI Server
- The Node.js server in `server/` provides Gemini-powered suggestions for tasks.
- Requires a Google Gemini API key.

### Tailwind CSS
- The project uses Tailwind CSS with custom configuration. See `client/tailwind.config.ts` for theme customization.


## 🎨 Customization

### Themes
- Modify `client/src/components/ThemeSwitcher.tsx` for custom themes
- Update `client/tailwind.config.ts` for color schemes

### Components
- All UI components are in `client/src/components/ui/`
- Based on shadcn/ui for easy customization
- Use Radix UI primitives for accessibility

### Styling
- Tailwind CSS classes for styling
- CSS variables for theme colors
- Custom animations in `client/src/components/AnimatedBackground.tsx`


## 🚀 Deployment

### Build for Production
```bash
cd client
npm run build
```

### Deploy to Vercel/Netlify
1. Connect your repository
2. Set environment variables in your hosting platform
3. Deploy automatically on push

### Supabase Edge Functions
See above for deploying AI priority suggestion function.


## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request


## 📄 License

This project is licensed under the MIT License.


## 🙏 Acknowledgments

- **shadcn/ui** for beautiful UI components
- **Supabase** for backend services
- **Tailwind CSS** for styling utilities
- **React community** for amazing libraries
- **Google Gemini** and **OpenAI** for AI features

---

**Happy tasking! 🎉**
