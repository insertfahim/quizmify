# 🧠 Quizmify - AI-Powered Quiz Application

> **"Quiz yourself on anything!"** - The ultimate AI-driven quiz platform that transforms any topic into an engaging learning experience.

![Next.js](https://img.shields.io/badge/Next.js-13.5.5-black?style=for-the-badge&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.1.6-blue?style=for-the-badge&logo=typescript)
![Tailwind](https://img.shields.io/badge/Tailwind-3.3.3-38B2AC?style=for-the-badge&logo=tailwind-css)
![Prisma](https://img.shields.io/badge/Prisma-5.0.0-2D3748?style=for-the-badge&logo=prisma)

## ✨ Features

### 🎯 **Smart Quiz Generation**

-   **AI-Powered Questions**: Leverages OpenAI to generate intelligent questions on any topic
-   **Dual Quiz Modes**:
    -   📝 **Multiple Choice (MCQ)**: Quick-fire questions with instant feedback
    -   💭 **Open-Ended**: Thoughtful questions that test deeper understanding
-   **Customizable Difficulty**: Tailor quiz length and complexity to your needs

### 📊 **Comprehensive Analytics**

-   **Real-time Statistics**: Track accuracy, time taken, and performance trends
-   **Detailed Breakdowns**: Question-by-question analysis with correct answers
-   **Progress Tracking**: Monitor your learning journey over time
-   **Visual Insights**: Beautiful charts and progress indicators

### 🎨 **Modern User Experience**

-   **Responsive Design**: Seamless experience across all devices
-   **Dark/Light Theme**: Toggle between themes for comfortable studying
-   **Intuitive Dashboard**: Clean, organized interface for easy navigation
-   **Real-time Feedback**: Instant results and explanations

### 🔐 **Secure & Personalized**

-   **NextAuth Integration**: Secure authentication with multiple providers
-   **Personal History**: Track all your quiz attempts and progress
-   **User Profiles**: Personalized experience with avatar support

## 🛠️ Tech Stack

### **Frontend & Framework**

-   **[Next.js 13](https://nextjs.org/)** - React framework with App Router
-   **[TypeScript](https://www.typescriptlang.org/)** - Type-safe development
-   **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first styling
-   **[Shadcn/ui](https://ui.shadcn.com/)** - Beautiful, accessible components

### **Backend & Database**

-   **[Prisma ORM](https://www.prisma.io/)** - Type-safe database client
-   **[PlanetScale](https://planetscale.com/)** - Serverless MySQL database
-   **[NextAuth.js](https://next-auth.js.org/)** - Authentication solution

### **AI & External Services**

-   **[OpenAI API](https://openai.com/)** - AI-powered question generation
-   **[React Query](https://tanstack.com/query)** - Data fetching and caching

### **UI & Styling**

-   **[Lucide React](https://lucide.dev/)** - Beautiful icons
-   **[Radix UI](https://www.radix-ui.com/)** - Unstyled, accessible components
-   **[React Hook Form](https://react-hook-form.com/)** - Performant forms

## 🚀 Getting Started

### Prerequisites

-   **Node.js** 18+ and npm/yarn/pnpm
-   **Database** (MySQL/PlanetScale)
-   **OpenAI API Key**

### Installation

1. **Clone the repository**

    ```bash
    git clone <repository-url>
    cd quizmify
    ```

2. **Install dependencies**

    ```bash
    npm install
    # or
    yarn install
    # or
    pnpm install
    ```

3. **Environment Setup**
   Create a `.env.local` file in the root directory:

    ```env
    # Database
    DATABASE_URL="your-database-url"

    # NextAuth
    NEXTAUTH_SECRET="your-nextauth-secret"
    NEXTAUTH_URL="http://localhost:3000"

    # OpenAI
    OPENAI_API_KEY="your-openai-api-key"

    # OAuth Providers (optional)
    GOOGLE_CLIENT_ID="your-google-client-id"
    GOOGLE_CLIENT_SECRET="your-google-client-secret"
    ```

4. **Database Setup**

    ```bash
    npx prisma generate
    npx prisma db push
    ```

5. **Run the development server**

    ```bash
    npm run dev
    # or
    yarn dev
    # or
    pnpm dev
    ```

6. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000) to see the application.

## 📱 Usage Guide

### Creating a Quiz

1. **Sign in** to your account
2. **Navigate** to the Dashboard
3. **Click** "Quiz me!" card
4. **Enter** your desired topic
5. **Choose** quiz type (MCQ or Open-ended)
6. **Select** number of questions
7. **Start** your personalized quiz!

### Taking a Quiz

-   **MCQ Mode**: Select the best answer from multiple choices
-   **Open-ended Mode**: Type your answer and get AI-powered evaluation
-   **Real-time feedback** on your performance
-   **Detailed explanations** for each question

### Tracking Progress

-   **Dashboard Overview**: See your recent activity and statistics
-   **History Page**: Review all past quiz attempts
-   **Statistics Page**: Dive deep into your performance metrics

## 🏗️ Project Structure

```
src/
├── app/                    # Next.js 13 App Router
│   ├── api/               # API routes
│   ├── dashboard/         # Dashboard page
│   ├── history/           # Quiz history
│   ├── play/              # Quiz playing interface
│   ├── quiz/              # Quiz creation
│   └── statistics/        # Performance analytics
├── components/            # Reusable UI components
│   ├── dashboard/         # Dashboard-specific components
│   ├── forms/             # Form components
│   ├── statistics/        # Statistics components
│   └── ui/                # Base UI components (Shadcn)
├── lib/                   # Utility libraries
├── schemas/               # Zod validation schemas
└── prisma/                # Database schema
```

## 🌐 Deployment

### Vercel (Recommended)

1. **Connect** your repository to [Vercel](https://vercel.com)
2. **Configure** environment variables
3. **Deploy** with automatic CI/CD

### Docker

```bash
# Build the image
docker build -t quizmify .

# Run the container
docker run -p 3000:3000 quizmify
```

### Fly.io

```bash
# Deploy to Fly.io
fly deploy
```

## 🎨 Customization

### Themes

The application supports both light and dark themes using `next-themes`. Users can toggle between themes using the theme switcher in the navigation.

### Styling

Built with Tailwind CSS and Shadcn/ui components. Customize the design system by modifying:

-   `tailwind.config.js` - Tailwind configuration
-   `src/app/globals.css` - Global styles
-   Component-level styling in individual files

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

-   **OpenAI** for providing powerful AI capabilities
-   **Vercel** for the excellent Next.js framework
-   **Shadcn** for the beautiful UI components
-   **The open source community** for amazing tools and libraries

---

<div align="center">

**Built with ❤️ by developers who love learning**

[Report Bug](../../issues) • [Request Feature](../../issues) • [Documentation](../../wiki)

</div>
