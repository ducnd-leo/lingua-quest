# LinguaQuest — Project Overview

> **Personal Full-stack + Language Learning Project**
> Build a real product to improve Software Engineering skills while simultaneously learning English and Japanese.

---

## 1. Project Summary

**LinguaQuest** is a personal language-learning web application focused on **English and Japanese**.

The project is intentionally designed as a learning system for its owner:

- Improve **Full-stack development** skills.
- Strengthen **Software Engineering fundamentals**.
- Improve **English from approximately IELTS 5.0 toward a stronger B1/B1+ foundation**.
- Start **Japanese from beginner level (near zero)**.
- Build a portfolio project that demonstrates practical engineering ability.
- Potentially connect the project with **Salesforce** in a later phase.

The core principle is:

> **Build the product in order to learn, and use the product in order to keep learning.**

---

## 2. Vision

Create a lightweight, enjoyable language-learning platform that turns daily study into a measurable progression system.

Instead of trying to reproduce a large product such as Duolingo, LinguaQuest will focus on a small set of highly useful learning loops:

```text
Learn
  ↓
Practice
  ↓
Review
  ↓
Measure
  ↓
Earn XP / Streak
  ↓
Return tomorrow
```

At the same time, the development process follows the same loop:

```text
Learn a technical concept
  ↓
Implement a real feature
  ↓
Test it
  ↓
Refactor it
  ↓
Document it
  ↓
Deploy it
```

---

## 3. Current Developer Profile

| Area | Current Level | Project Goal |
|---|---|---|
| Salesforce Development | Fresher / ~6 months | Continue strengthening professional experience |
| Node.js | Internship experience | Become comfortable building production-style APIs |
| React.js | Internship experience | Become comfortable building maintainable frontends |
| TypeScript | Basic → Intermediate target | Use throughout the project |
| Backend Architecture | Beginner / Intermediate | Learn practical API and service design |
| SQL / Database | Needs strengthening | Build solid PostgreSQL fundamentals |
| Testing | Needs strengthening | Introduce unit/integration testing |
| Git / GitHub | Working knowledge | Use professional workflow |
| English | ~IELTS 5.0 | Stronger B1/B1+ foundation and better technical English |
| Japanese | Beginner / near zero | Build beginner foundation |

---

## 4. Project Objectives

### 4.1 Development Objectives

By the end of the first 2-month MVP phase, the project should demonstrate practical experience with:

- React + TypeScript
- Node.js + Express + TypeScript
- REST API design
- PostgreSQL
- Prisma ORM
- Authentication and authorization basics
- Validation and error handling
- Business logic separation
- Reusable frontend components
- Client/server data fetching
- Basic testing
- Git/GitHub workflow
- Deployment
- Technical documentation

### 4.2 English Objectives

The first phase is **not** about making an unrealistic jump from IELTS 5.0 to a high IELTS score.

The focus is to build a sustainable foundation:

- Daily vocabulary acquisition and review.
- Everyday + workplace + programming vocabulary.
- Core grammar.
- Short reading practice.
- Short writing practice.
- Better ability to read technical documentation without relying heavily on translation.

### 4.3 Japanese Objectives

Start from zero and build the foundation in the following order:

```text
Hiragana
  ↓
Katakana
  ↓
Basic vocabulary
  ↓
Basic sentence patterns
  ↓
Basic particles
  ↓
Basic grammar
```

The first phase should prioritize recognition and basic usage rather than rushing toward an advanced JLPT level.

---

# 5. Product Principles

## 5.1 MVP First

The product must be useful before it becomes large.

Every new feature must answer at least one question:

- Does it improve learning?
- Does it improve engineering skill?
- Does it improve the portfolio value of the project?

If the answer is no, postpone it.

## 5.2 No Feature Explosion

The first 8 weeks should **not** attempt to build:

- Mobile application
- Social network
- Real-time chat
- Full AI tutor
- Voice recognition system
- Complex recommendation engine
- Microservice architecture
- Kubernetes infrastructure
- Large-scale event-driven architecture

These are candidates for later phases only.

## 5.3 Consistency Over Intensity

The project should support a minimum daily mode so that a busy day does not become a zero day.

### Normal mode

- Coding: ~90 minutes
- English: ~45 minutes
- Japanese: ~30 minutes

### Minimum mode

- Coding: ~30 minutes
- English: ~15 minutes
- Japanese: ~10 minutes

The goal is to maintain continuity rather than maximize daily hours.

## 5.4 English as a Development Skill

English should appear naturally inside the development workflow:

- Read official documentation in English.
- Write code comments and technical notes in English where practical.
- Write Git commits in English.
- Write the project README in English.
- Use English learning content related to programming and work.

## 5.5 Japanese as a Built-in Learning Loop

Japanese learning should become a feature of the product instead of a completely separate activity.

Example:

```text
Japanese vocabulary
      ↓
Flashcard
      ↓
Quiz
      ↓
Sentence building
      ↓
Review
```

---

# 6. Target Users

## Primary User

The first and most important user is the project owner.

The system should therefore optimize for:

- Fast daily usage.
- Low cognitive overhead.
- Clear progress feedback.
- Small achievable tasks.
- Consistent review.
- Visible rewards.

## Future Users

After the MVP becomes stable, the architecture may be extended to support:

- Other English learners.
- Beginner Japanese learners.
- Multiple learner profiles.
- Additional languages.

This is **not required for the first 8-week phase**.

---

# 7. MVP Scope

The MVP contains six primary product capabilities.

| Module | Priority | Purpose |
|---|---:|---|
| Authentication | P0 | Secure user access |
| Vocabulary | P0 | Store and study vocabulary |
| Flashcards / Review | P0 | Repeated practice |
| Quiz | P0 | Measure recall |
| Progress Dashboard | P0 | Show learning progress |
| Gamification | P1 | Encourage consistency |

Additional but smaller modules:

| Module | Priority | First-phase role |
|---|---:|---|
| English Writing | P1 | Short daily writing practice |
| Japanese Foundations | P1 | Hiragana, Katakana, beginner vocabulary |
| Sentence Builder | P1 | Basic Japanese sentence construction |
| Grammar | P2 | Small curated lessons |

---

# 8. Core User Flow

```text
Register / Login
       ↓
Dashboard
       ↓
Today's Mission
       ↓
Choose Language
   ┌─────┴─────┐
   │           │
English      Japanese
   │           │
   └─────┬─────┘
         ↓
Vocabulary / Lesson
       ↓
Flashcards
       ↓
Quiz
       ↓
Result
       ↓
XP / Streak / Progress
       ↓
Next Review Scheduled
```

---

# 9. Main Product Modules

## 9.1 Authentication

Capabilities:

- Register
- Login
- Logout
- Password hashing
- JWT-based authentication
- Protected routes
- Current-user endpoint

Suggested API:

```text
POST /auth/register
POST /auth/login
POST /auth/logout
GET  /auth/me
```

---

## 9.2 Vocabulary

Each vocabulary item may contain:

```text
id
language
word
meaning
pronunciation
exampleSentence
level
category
createdAt
updatedAt
```

Example — English:

```text
Word: improve
Meaning: cải thiện
Example: I want to improve my English.
Level: B1
Category: Work
```

Example — Japanese:

```text
Word: 改善する
Reading: かいぜんする
Meaning: cải thiện
Level: Beginner
Category: Work
```

Basic capabilities:

- List vocabulary
- Search
- Filter by language
- Filter by category
- Filter by level
- View detail
- Add/edit/delete content during development/admin phase

---

## 9.3 Flashcards / Spaced Review

Flashcards are the main daily practice loop.

Example:

```text
┌────────────────────────────┐
│                            │
│          improve           │
│                            │
│            🔊              │
│                            │
└────────────────────────────┘
```

User reveals the answer:

```text
cải thiện

I want to improve my English.
```

Then chooses:

```text
Again | Hard | Good | Easy
```

### Initial review schedule

Keep the first implementation intentionally simple:

```text
Again → 10 minutes
Hard  → 1 day
Good  → 3 days
Easy  → 7 days
```

The algorithm can later evolve into a more sophisticated spaced-repetition model.

---

## 9.4 Quiz Engine

Initial question types:

### Multiple Choice

```text
What does "improve" mean?

A. phá hủy
B. cải thiện ✓
C. quên
D. bắt đầu
```

### Vocabulary Recall

```text
______ means "cải thiện".
```

### Translation

```text
I want to improve my English.
→ Tôi muốn cải thiện tiếng Anh.
```

### Japanese Character Quiz

```text
あ

A. a ✓
B. i
C. u
D. e
```

### Quiz Result

```text
Correct: 8 / 10
Accuracy: 80%
XP: +80
```

---

## 9.5 Progress Dashboard

The dashboard should answer three questions quickly:

1. What should I study today?
2. How am I progressing?
3. Am I staying consistent?

Example layout:

```text
Good Evening 👋

🔥 8 Day Streak
⭐ 1,240 XP

Today's Goal
██████████ 80%

English
Vocabulary: 72%
Quiz: 81%

Japanese
Hiragana: 64%
Vocabulary: 21%
```

Potential metrics:

- Daily goal progress
- XP
- Current streak
- Vocabulary learned
- Quiz accuracy
- Review backlog
- English progress
- Japanese progress

---

## 9.6 Gamification

Initial system:

- XP
- Levels
- Daily goals
- Streaks
- Achievements

Example achievements:

```text
🏆 First 100 Words
🔥 7 Day Streak
🎯 100% Quiz
🇯🇵 Hiragana Master
```

The gamification system should encourage consistency without becoming a distraction from learning.

---

# 10. English Learning Module

## Initial Learning Tracks

```text
Vocabulary
Grammar
Reading
Writing
```

### Vocabulary

Target:

- 10–15 useful words/day.
- Prioritize high-frequency and work-related vocabulary.

Suggested categories:

- Daily Life
- Work
- Programming
- Technology
- Communication

### Grammar

Start with high-value core topics:

- Present Simple
- Present Continuous
- Past Simple
- Present Perfect
- Future forms
- Modal verbs
- Conditionals

### Reading

Daily short reading practice:

- Technical documentation
- Short articles
- Developer-related English
- Simple general English content

### Writing

Daily micro-writing is preferred over occasional long essays.

Example prompt:

> Describe what you did at work today in five English sentences.

Store:

```text
writingId
userId
language
content
createdAt
```

Later, AI can be added for:

- Grammar correction
- Better phrasing
- Vocabulary recommendations
- Writing feedback

AI is **not required for the MVP**.

---

# 11. Japanese Learning Module

## Stage 1 — Hiragana

Example:

```text
あ い う え お
か き く け こ
さ し す せ そ
```

## Stage 2 — Katakana

Example:

```text
ア イ ウ エ オ
```

## Stage 3 — Basic Vocabulary

Examples:

```text
人
学生
友達
会社
仕事
日本
英語
学校
```

## Stage 4 — Basic Expressions

Examples:

```text
こんにちは
おはよう
こんばんは
ありがとう
すみません
```

## Stage 5 — Basic Grammar

Start with:

```text
は
を
が
に
で
です
ます
```

## Sentence Builder

The first interactive Japanese-specific learning feature:

```text
私は + 学生 + です
```

↓

```text
私は学生です
Watashi wa gakusei desu.
I am a student.
```

This feature also provides useful React practice through:

- Drag and drop / ordering
- State management
- Validation
- Feedback UI

---

# 12. Technical Architecture

## High-level Architecture

```text
                  ┌───────────────────────┐
                  │      React App        │
                  │   TypeScript/Vite     │
                  └───────────┬───────────┘
                              │
                          REST API
                              │
                  ┌───────────┴───────────┐
                  │   Node.js / Express   │
                  │      TypeScript       │
                  └───────────┬───────────┘
                              │
                          Prisma ORM
                              │
                  ┌───────────┴───────────┐
                  │      PostgreSQL       │
                  └───────────────────────┘
```

Future optional integrations:

```text
                 ┌───────────────────────┐
                 │   AI / LLM Service    │
                 └───────────┬───────────┘
                             │
              Writing / Explanation / Practice

                 ┌───────────────────────┐
                 │      Salesforce       │
                 └───────────┬───────────┘
                             │
                  Progress Integration
```

---

# 13. Proposed Technology Stack

## Frontend

- React
- TypeScript
- Vite
- React Router
- TanStack Query
- Tailwind CSS

## Backend

- Node.js
- TypeScript
- Express
- Zod for validation
- JWT authentication

## Database

- PostgreSQL
- Prisma ORM

## Development Tools

- Git
- GitHub
- ESLint
- Prettier
- API testing tool
- Unit/integration testing framework

## Deployment

Initial deployment can use a simple managed stack:

```text
Frontend → Vercel
Backend  → Render / Railway / similar
Database → Managed PostgreSQL
```

The deployment provider is not part of the product architecture and can be changed later.

---

# 14. Initial Domain Model

The database should start small.

Core entities:

```text
User
Language
Vocabulary
Category
UserVocabulary
Quiz
QuizQuestion
QuizAttempt
LearningSession
Achievement
UserAchievement
```

Potential later entities:

```text
Writing
GrammarLesson
Sentence
ReviewLog
UserGoal
Notification
SalesforceSyncLog
```

### Relationship concept

```text
User
 │
 ├──< UserVocabulary >── Vocabulary ── Category
 │
 ├──< QuizAttempt >── Quiz ──< QuizQuestion
 │
 ├──< LearningSession
 │
 └──< UserAchievement >── Achievement
```

The detailed ERD will be created before database implementation.

---

# 15. Frontend Page Map

```text
/
├── /login
├── /register
├── /dashboard
├── /vocabulary
├── /vocabulary/:id
├── /review
├── /quiz
├── /quiz/:id
├── /progress
└── /settings
```

Possible future pages:

```text
/english
/japanese
/grammar
/writing
/achievements
/admin
```

---

# 16. Backend API Areas

```text
/auth
/users
/vocabulary
/review
/quiz
/progress
/gamification
/learning-sessions
```

Example vocabulary API:

```text
GET    /vocabulary
GET    /vocabulary/:id
POST   /vocabulary
PUT    /vocabulary/:id
DELETE /vocabulary/:id
```

Example review API:

```text
GET  /review/today
POST /review/:vocabularyId
```

Example progress API:

```text
GET /progress/summary
GET /progress/daily
GET /progress/weekly
```

---

# 17. Repository Structure

Proposed monorepo structure:

```text
lingua-quest/
│
├── apps/
│   ├── web/
│   │   ├── src/
│   │   │   ├── components/
│   │   │   ├── features/
│   │   │   ├── pages/
│   │   │   ├── hooks/
│   │   │   ├── lib/
│   │   │   ├── services/
│   │   │   └── types/
│   │   └── ...
│   │
│   └── api/
│       ├── src/
│       │   ├── modules/
│       │   ├── middleware/
│       │   ├── lib/
│       │   ├── config/
│       │   └── app.ts
│       └── ...
│
├── packages/
│   ├── shared/
│   └── config/
│
├── docs/
│   ├── PRODUCT.md
│   ├── ARCHITECTURE.md
│   ├── DATABASE.md
│   ├── API.md
│   └── ROADMAP.md
│
├── .github/
├── README.md
├── PROJECT_OVERVIEW.md
└── package.json
```

A simpler `frontend/` + `backend/` repository is also acceptable for the first version. Architecture should remain simple enough to avoid spending time on tooling instead of product development.

---

# 18. Eight-Week Delivery Plan

## Week 1 — Foundation

### Product

- Define MVP
- Define user flow
- Initial database model

### Engineering

- Repository setup
- React + TypeScript
- Node + Express + TypeScript
- PostgreSQL
- Prisma
- Basic API
- Authentication foundation

### English

- Daily vocabulary
- Technical English
- Reading documentation

### Japanese

- Hiragana
- Basic greetings

### Definition of Done

```text
Register → Login → Dashboard → API → Database
```

---

## Week 2 — Vocabulary

### Engineering

- Vocabulary schema
- CRUD API
- Search
- Filter
- Frontend vocabulary page

### English

- 10–15 words/day
- Work + technology vocabulary

### Japanese

- Continue Hiragana
- Basic expressions

### Definition of Done

User can browse and interact with vocabulary in the application.

---

## Week 3 — Flashcards + Review

### Engineering

- Flashcard UI
- Review actions
- `nextReviewAt`
- Review history / counters
- Daily review queue

### Language

- Daily review becomes the main habit.

### Definition of Done

User can complete a review session and receive a next review schedule.

---

## Week 4 — Quiz Engine

### Engineering

- Quiz model
- Question model
- Multiple-choice questions
- Scoring
- Quiz result screen
- XP calculation

### Japanese

- Hiragana quiz
- Basic vocabulary quiz

### Definition of Done

User can take a quiz and receive score + XP.

---

## Week 5 — Dashboard + Gamification

### Engineering

- Dashboard metrics
- XP
- Level
- Streak
- Achievements
- Daily goals

### Definition of Done

User can clearly see progress and consistency.

---

## Week 6 — English Module

### Engineering

- English learning categories
- Grammar content structure
- Writing practice
- Progress metrics

### Language

- Core grammar
- Short reading
- Daily writing

### Definition of Done

English learning has a repeatable daily workflow.

---

## Week 7 — Japanese Module

### Engineering

- Hiragana content
- Katakana content
- Japanese vocabulary
- Character quiz
- Sentence builder

### Language

- Hiragana mastery
- Katakana foundation
- Basic vocabulary
- Basic sentence patterns

### Definition of Done

Japanese beginner learning is usable from inside the application.

---

## Week 8 — Polish + Deploy + Portfolio

### Engineering

- Refactor
- Validation
- Error handling
- Tests
- UI polish
- Deployment
- README
- Architecture documentation

### Portfolio

Document:

- Problem
- Product idea
- Architecture
- Database design
- Key technical challenges
- Solutions
- What was learned
- Future roadmap

### Definition of Done

```text
Production URL
        +
GitHub Repository
        +
README
        +
Architecture Docs
        +
Demo-ready MVP
```

---

# 19. Daily Operating System

## Normal Day

```text
Coding        90 min
English       45 min
Japanese      30 min
---------------------
Total         2h45m
```

## Minimum Day

```text
Coding        30 min
English       15 min
Japanese      10 min
---------------------
Total         55 min
```

The minimum mode exists specifically to prevent a zero day.

---

# 20. Weekly Scorecard

Each week should be measured using four dimensions.

| Dimension | Example KPI |
|---|---|
| Coding | Feature completed |
| English | 60–70 useful words + practice days |
| Japanese | Weekly milestone |
| Consistency | 6/7 active days |

Weekly completion rule:

> **Aim for 80–90% completion rather than perfection.**

Do not restart a week because one task is incomplete.

---

# 21. Git Strategy

Use meaningful commits.

Good examples:

```text
feat: implement authentication
feat: add vocabulary crud
feat: add flashcard review flow
feat: implement quiz scoring
fix: handle expired jwt
refactor: extract quiz service
chore: configure eslint
```

Avoid:

```text
update
fix
final
final2
working
```

Recommended habit:

```text
Small feature
   ↓
Commit
   ↓
Run tests
   ↓
Continue
```

---

# 22. Definition of MVP Success

The first 2-month phase is successful if all of the following are true:

### Product

- User can log in.
- User can study English vocabulary.
- User can study Japanese vocabulary.
- User can review flashcards.
- User can complete quizzes.
- User can see progress.
- User can earn XP and maintain a streak.
- User can complete simple English writing practice.
- User can practice beginner Japanese characters/sentences.

### Engineering

- Frontend and backend are separated cleanly.
- API is documented.
- Database relationships are understood.
- Authentication is implemented safely.
- Core business logic has tests.
- Project is deployed.
- GitHub repository is presentable.

### Personal Growth

- Coding was practiced consistently.
- English was practiced consistently.
- Japanese was practiced consistently.
- The application is actually used by its creator.

---

# 23. Portfolio Value

The project should demonstrate more than framework knowledge.

It should show the ability to:

```text
Understand a problem
        ↓
Design a product
        ↓
Design data
        ↓
Design APIs
        ↓
Build frontend
        ↓
Build backend
        ↓
Test
        ↓
Deploy
        ↓
Measure usage
        ↓
Improve
```

The project story should eventually become:

> "I built LinguaQuest because I wanted to solve my own language-learning problem while improving my full-stack engineering skills."

This is a stronger portfolio narrative than building an arbitrary tutorial application.

---

# 24. Future Phase — After MVP

Only after the MVP is stable should the project expand.

Potential Phase 2 features:

- AI grammar correction
- AI writing feedback
- AI conversation practice
- Pronunciation practice
- Listening exercises
- More advanced English / IELTS tracks
- JLPT-oriented Japanese tracks
- Kanji learning
- Personalized review recommendations
- Notifications
- Offline/PWA support
- Salesforce integration

Possible Salesforce integration:

```text
LinguaQuest
    │
    │ REST API
    ▼
Salesforce
    │
    ├── Learning Progress
    ├── Learning Session
    ├── Achievement
    └── User Progress
```

This can later become a strong bridge between the user's Salesforce experience and full-stack development experience.

---

# 25. Anti-Goals

The project will **not** attempt to become:

- A commercial language platform during the first phase.
- A replacement for professional English/Japanese courses.
- A complete AI language tutor.
- A social network.
- A production-scale distributed system.

The first mission is much simpler:

> **Build a small, well-engineered product that is genuinely useful to its creator.**

---

# 26. Final Success Picture

After 8 weeks, the target state is:

```text
                  LINGUAQUEST
                       │
          ┌────────────┼────────────┐
          │            │            │
       English      Japanese       Dev
          │            │            │
      Vocabulary    Hiragana     React
      Grammar       Katakana     Node.js
      Reading       Vocabulary   TypeScript
      Writing       Sentences    PostgreSQL
          │            │          Prisma
          └────────────┼────────────┘
                       │
                Progress / XP
                       │
                   Daily Habit
```

The real deliverable is not only the application.

It is the combination of:

```text
Product
+
Engineering skill
+
English skill
+
Japanese foundation
+
Consistency
+
Portfolio evidence
```

---

# 27. Immediate Next Documents

After this overview is approved, the project documentation should be broken into smaller documents:

1. `PRODUCT.md` — detailed product requirements and MVP scope.
2. `ROADMAP.md` — detailed 8-week plan broken into daily tasks.
3. `ARCHITECTURE.md` — application architecture and folder/module design.
4. `DATABASE.md` — ERD, entities, relationships, indexes, and Prisma schema decisions.
5. `API.md` — API endpoints, request/response contracts, errors, authentication.
6. `LEARNING_PLAN.md` — English + Japanese curriculum for the first 8 weeks.
7. `DEV_GUIDE.md` — Git workflow, coding conventions, testing, and Definition of Done.

---

# 28. Project Rule

> **Do not optimize for how much code is written. Optimize for how much capability is built and how consistently the product is used.**

---

**Document:** `PROJECT_OVERVIEW.md`
**Version:** 1.0
**Phase:** 8-week MVP
**Status:** Planning
