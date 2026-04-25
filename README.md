# FindBest EV Agent

FindBest EV Agent is an AI-powered new energy vehicle recommendation system. It helps users describe their car-buying needs, retrieves matching vehicles from a structured EV database, supplements missing information through web search, and supports sales lead collection through Lark webhook notifications.

## Core Flow

### 1. Fill in needs, then get personalized recommendations

Before the conversation starts, users provide their basic requirements, such as:

- Usage scenario
- Purchase budget
- Preferred body type, such as SUV or sedan
- Requirements for intelligent driving features

The Agent then searches the new energy vehicle database and recommends models with a high matching score.

### 2. No result in database, then search online

If a model or requirement is not covered by the internal database, the Agent automatically calls Perplexity during the conversation to search the web and return authoritative information and key details.

This keeps the recommendation experience continuous even when the local database does not contain enough information.

### 3. Interested models are added to Favorites

When users show interest in a vehicle, the Agent can automatically add it to the user's Favorites list and save it in the user-side database.

This creates a shortlist for later comparison, review, and purchase decision-making.

### 4. Sales lead collection with Lark webhook notification

One of the core goals of this Agent is to help new energy vehicle sales teams understand user needs earlier and more accurately.

During the conversation, the Agent can ask whether the user wants one-on-one service. If the user agrees and leaves a phone number, the system sends the lead information to a sales group through a Lark webhook as a bot message, so the sales team can follow up in time.

## Tech Stack

- Next.js
- React
- TypeScript
- Tailwind CSS

## Getting Started

Install dependencies:

```bash
pnpm install
```

Start the development server:

```bash
pnpm dev
```

Build for production:

```bash
pnpm build
```

## Project Structure

- `app/` - Next.js app routes and global styles
- `components/` - Reusable UI and page sections
- `public/` - Static image assets
- `lib/` - Shared utilities

