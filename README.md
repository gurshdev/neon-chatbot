# Neon x Aceternity Chatbot Template

A modern, interactive chatbot template built with Next.js, AI SDK, Aceternity UI, and Neon's serverless Postgres.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?demo-description=A%20modern%2C%20interactive%20chatbot%20template%20built%20with%20Next.js%2C%20AI%20SDK%2C%20Aceternity%20UI%2C%20and%20Neon%27s%20serverless%20Postgres.&demo-image=%2F%2Fimages.ctfassets.net%2Fe5382hct74si%2F2cjDyEMUVtgdWBp9dXRXfv%2F548ea6a3ba0dc1b24677de482c28f9c3%2Fbanner.png&demo-title=Chatbot%20by%20Aceternity&demo-url=https%3A%2F%2Fneon-aceternity-chatbot.vercel.app%2F&env=OPENAI_API_KEY&from=templates&project-name=Chatbot%20by%20Aceternity&repository-name=chatbot-by-aceternity&repository-url=https%3A%2F%2Fgithub.com%2Fneondatabase%2Fneon-chatbot&skippable-integrations=1&stores=%255B%257B%2522type%2522%253A%2522integration%2522%252C%2522protocol%2522%253A%2522storage%2522%252C%2522productSlug%2522%253A%2522neon%2522%252C%2522integrationSlug%2522%253A%2522neon%2522%257D%255D)

![Banner](https://neon-chatbot.vercel.app/banner.png)

## Features

- 🤖 Real-time streaming responses
- 💾 Persistent chat history storage with Neon serverless Postgres
- ✨ Beautiful UI components from Aceternity UI
- 🎨 Fully customizable with Tailwind CSS
- 📱 Responsive design for all devices
- ⚡ Built on Next.js 14 with App Router

## Prerequisites

- Node.js 18+ 
- A [Neon](https://neon.tech/) account to create a Postgres database
- An [OpenAI](https://openai.com/) API key

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/neondatabase/neon-chatbot.git
cd neon-chatbot-template
```

2. Install dependencies:
```bash
npm install
# or
yarn install
# or
pnpm install
```

3. Create a `.env.local` file in the root directory with the following variables:
```bash
DATABASE_URL="your-neon-database-url"
OPENAI_API_KEY="your-openai-api-key"
```

4. Set up the database schema:
```sql
CREATE TABLE chat_history (
  id SERIAL PRIMARY KEY,
  user_message TEXT NOT NULL,
  assistant_message TEXT NOT NULL,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT CURRENT_TIMESTAMP
);
```

5. Run the development server:
```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Project Structure

- `/app` - Next.js 14 app directory containing routes and layouts
- `/components` - Reusable UI components
- `/lib` - Utility functions and shared code
- `/public` - Static assets
- `/styles` - Global styles and Tailwind CSS configuration

## Key Technologies

- [Next.js](https://nextjs.org/) - React framework
- [Neon](https://neon.tech/) - Serverless Postgres database
- [OpenAI](https://openai.com/) - GPT-4 language model
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [Framer Motion](https://www.framer.com/motion/) - Animation library
- [Aceternity UI](https://ui.aceternity.com/) - UI components

## Deployment

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new).

1. Push your code to a GitHub repository
2. Import your repository to Vercel
3. Add your environment variables in the Vercel dashboard
4. Deploy!

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

- [Aceternity UI](https://ui.aceternity.com/) for the beautiful UI components
- [Neon.tech](https://neon.tech/) for the serverless Postgres database
