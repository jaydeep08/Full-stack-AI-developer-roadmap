# Full-Stack AI Developer — In-Depth 2-Month Roadmap

> **Target role:** **Full-Stack AI Developer** — a full-stack engineer (frontend + backend + database + APIs) who also builds AI features (LLM apps, RAG, agents) on top. AI is an "added layer", not a replacement — you need both.
> **Priority:** Full-Stack foundation is the base; AI is the specialty that makes you stand out.
> **Duration:** 8-week **core** track. **Daily budget:** 2-3 hrs (~15-18 hrs/week). The plan is **depth-first, not time-boxed** — if a topic needs longer, take longer. See the [optional extension (Weeks 9-12)](#optional-extension-weeks-9-12) for extra depth on Python, DSA, and system design if you can invest more time.
> **Python note:** you know Python syntax but lack interview-grade DSA practice and backend-writing fluency. A dedicated [Python Mastery track](#python-mastery-for-interviews--backend) is included — solve **all DSA in Python** and build **all backends in Python** so coding becomes automatic under interview pressure.
> **Interview reality for this role:** you WILL be tested on (1) DSA coding rounds, (2) LLD + HLD system design **including AI system design**, (3) AI fundamentals, and (4) full-stack project depth. This roadmap covers all four.

---

## Table of Contents
1. [What this role actually is](#1-what-this-role-actually-is)
2. [Your starting point & skill-gap map](#2-your-starting-point--skill-gap-map)
3. [How to use this roadmap](#3-how-to-use-this-roadmap)
4. [The 8-week plan at a glance](#4-the-8-week-plan-at-a-glance)
5. [Week-by-week in depth](#5-week-by-week-in-depth)
   - [Alternative 8-week track (Python backend + DSA in parallel)](#alternative-8-week-track-python-backend--dsa-in-parallel)
   - [Python Mastery for interviews & backend](#python-mastery-for-interviews--backend)
   - [Optional extension (Weeks 9-12)](#optional-extension-weeks-9-12)
6. [DSA master plan](#6-dsa-master-plan)
7. [LLD (Low-Level Design) master plan](#7-lld-low-level-design-master-plan)
8. [HLD (High-Level / System Design) master plan](#8-hld-high-level--system-design-master-plan)
9. [AI system design (the differentiator)](#9-ai-system-design-the-differentiator)
10. [Interview topic checklists](#10-interview-topic-checklists)
    - [Behavioral & soft-skills interview prep (complete package)](#behavioral--soft-skills-interview-prep-complete-package)
11. [Curated resource library (vetted links)](#11-curated-resource-library-vetted-links)
12. [Projects & portfolio](#12-projects--portfolio)
13. [Progress tracker](#13-progress-tracker)

---

## 1. What this role actually is

Think in layers. Every "AI Developer / AI Engineer" job today is a full-stack app with an AI layer wired in:

```text
+-------------------------------------------------------------+
| AI LAYER         LLM • prompts • RAG • agents • eval        | -> your differentiator
+-------------------------------------------------------------+
| FRONTEND         React • TypeScript • CSS • state           |
| BACKEND          FastAPI/Node • REST • auth • caching       | -> the full-stack base
| DATA             SQL + NoSQL • vector DB • modeling         |
+-------------------------------------------------------------+
| CS FOUNDATION    DSA • LLD • HLD (tested in interviews)     | -> the gate everyone passes
+-------------------------------------------------------------+
```

---

**AI Developer != ML Engineer.** You *use* pre-trained models via APIs (OpenAI, Azure OpenAI, Claude, Gemini). You do **not** train models, do heavy math, or build transformers. That distinction is confirmed on the [roadmap.sh AI Engineer roadmap](https://roadmap.sh/ai-engineer) — "AI Engineer vs ML Engineer." Skip model training; go deep on the application layer.

---

## 2. Your starting point & skill-gap map

**You already have (leverage these hard):**
- React + TypeScript (strong on logic: state, dynamic data, API calls, functions)
- Python + Azure Functions, building REST/first-party APIs consumed by React
- Azure: App registrations, Entra ID (Azure AD) auth/authorization, Storage, Cosmos DB (NoSQL)
- AI: Azure AI Foundry, Azure AI Search, RAG chatbots, Copilot Studio, SPFx front-ends
- Power Automate, Power BI, M365/SharePoint integration

**Gaps to close (where your hours go):**

| Area | Now | Target | Priority |
| :--- | :--- | :--- | :--- |
| CSS / responsive UI | Weak | Comfortable (Flexbox, Grid, Tailwind) | High |
| State management patterns | Basic | Redux Toolkit / Zustand + when to use | Medium |
| Backend framework depth | Azure Functions only | FastAPI + REST design | High |
| **SQL + relational modeling** | NoSQL-only | JOINs, indexing, normalization, ACID | High |
| **DSA** | College-rusty | ~120 problems, all patterns | **Critical** |
| **LLD (OOP design)** | Gap | SOLID + patterns + 6 designs | High |
| **HLD (system design)** | Gap | Scalability + 6 designs | High |
| **AI fundamentals** | Practical only | Tokens, embeddings, prompting theory | Medium |
| Agents / frameworks | Partial | LangChain/LangGraph, function calling | High |
| DevOps | Azure-partial | Docker, GitHub Actions, deploy | Medium |

---

## 3. How to use this roadmap

- **Daily rhythm (2-3 hrs):** ~40 min DSA • ~60 min full-stack topic • ~60 min AI topic. Rotate if short on time, but **never skip DSA**.
- **🟩 = refresh** (you know it, be able to explain). **🟧 = gap** (most of your time).
- Do the **weekend project** every week — projects + system-design stories are what get offers.
- Use the [Progress Tracker](#13-progress-tracker) and the deep-dive plans (sections 6-9) as your reference libraries.
- All links in [section 11](#11-curated-resource-library-vetted-links) are vetted and free unless noted.

---

## 4. The 8-week plan at a glance

| Week | Full-Stack | AI | DSA | Design |
| :--- | :--- | :--- | :--- | :--- |
| 1 | JS/TS deep dive + React internals | LLM fundamentals (tokens, embeddings, params) | Arrays, Hashing | — |
| 2 | CSS, Flexbox/Grid, Tailwind, state mgmt | Prompt engineering + RAG pipeline | Two pointers, Sliding window | — |
| 3 | FastAPI + REST design | Vector DBs + embeddings in practice | Stack, Queue, Linked List | LLD intro (SOLID) |
| 4 | SQL + data modeling | Function calling / tool use | Binary Search, Trees | LLD: patterns + Parking Lot |
| 5 | Auth, security, testing | Agents (LangChain/LangGraph) | Graphs (BFS/DFS), Backtracking | LLD: Rate Limiter, LRU |
| 6 | Docker + CI/CD + deploy | Agentic patterns + evaluation | Heap, 1-D DP | HLD basics + AI system design |
| 7 | **Full-stack capstone** | **AI capstone** | Intervals, Greedy, 2-D DP | HLD: 3 mock designs |
| 8 | Resume, portfolio, applications | Mock interviews (all tracks) | Mixed timed drills | Behavioral + design mocks |

---

## 5. Week-by-week in depth

### WEEK 1 — JS/TS Mastery + LLM Fundamentals

**Full-Stack (Mon-Fri)**
- **JavaScript:** event loop (call stack, task queue, microtask queue), closures, `this` binding, prototypes, hoisting, `async`/`await`, promises, error handling. 📌 *(The event loop is one of the most-asked FE interview questions.)*
- **TypeScript:** generics, `Partial`/`Pick`/`Omit`/`Record`/`Readonly`, discriminated unions, `keyof`, `typeof`, conditional types, `infer`, narrowing, `as const`. 📌
- **React internals:** render vs commit, reconciliation, keys, `useState` batching, `useEffect` dependency rules & cleanup, `useMemo`/`useCallback`/`useRef`, `React.memo`, why re-renders happen.
- **Build:** 3 custom hooks — `useDebounce`, `useFetch`, `useLocalStorage`.

**AI (Mon-Fri)**
- Transformer intuition (no math): next-token prediction, attention at a high level.
- **Tokens & tokenization:** what a token is, context windows, why long context costs more; try [OpenAI Tokenizer](https://platform.openai.com/tokenizer).
- **Embeddings:** vectors, cosine similarity, semantic vs keyword search.
- **Generation params:** temperature, top-p, top-k, max tokens, stop sequences, frequency/presence penalty.
- **Hands-on:** call Azure OpenAI / OpenAI from Python; log `usage` tokens; sweep temperature 0->1 and observe.

**DSA:** Big-O (time & space) • Arrays • Hashing (HashMap/Set).  
*Problems:* Two Sum, Valid Anagram, Contains Duplicate, Group Anagrams, Top K Frequent, Valid Palindrome, Best Time to Buy/Sell Stock. **(~8-10 problems)**

**Weekend project:** "Smart Notes" — React + TS app with an **AI Summarize** button calling Azure OpenAI. Clean types, loading/error states.

**Checkpoint:** explain the event loop (2 min) • explain what a token is and why context is limited.

---

### WEEK 2 — CSS/UI + Prompt Engineering & RAG

**Full-Stack**
- **CSS core:** box model, specificity, cascade, positioning, `display`, units (`rem`/`em`/`%`/`vh`/`vw`).
- **Flexbox** (1-D) & **CSS Grid** (2-D) — build 5 layouts until fluent. Use [Flexbox Froggy](https://flexboxfroggy.com/) & [Grid Garden](https://cssgridgarden.com/).
- **Responsive design:** mobile-first, media queries, container patterns.
- **Tailwind CSS:** fastest way past "CSS pain" for logic-first devs.
- **State management:** Context API vs Redux Toolkit vs Zustand — trade-offs & when to use each.

**AI**
- **Prompt engineering:** zero-shot, few-shot, chain-of-thought (CoT), ReAct, role/system prompts, structured/JSON output, delimiters, guardrails. Read [OpenAI prompt guide](https://platform.openai.com/docs/guides/prompt-engineering) + [Prompting Guide](https://www.promptingguide.ai/).
- **RAG pipeline end-to-end:** load -> **chunk** -> embed -> store (vector DB) -> retrieve (similarity/hybrid) -> rerank -> augment prompt -> generate -> cite.
- **Chunking:** fixed-size, overlap, semantic; why chunk size affects recall.
- **Hands-on:** build a from-scratch RAG in Python (PDF -> chunks -> embeddings -> in-memory cosine search -> answer). No framework yet.

**DSA:** Two pointers • Sliding window.  
*Problems:* Valid Palindrome, 3Sum, Container With Most Water, Two Sum II, Longest Substring Without Repeating Characters, Longest Repeating Character Replacement, Maximum Subarray, Minimum Size Subarray Sum. **(~8-10 problems)**

**Weekend project:** rebuild Week 1 UI in **Tailwind**, fully responsive; add **Chat with your notes (RAG)** using your pipeline.

**Checkpoint:** whiteboard the RAG pipeline • Flexbox vs Grid, when each.

---

### WEEK 3 — Backend Depth (FastAPI) + Vector Databases + LLD intro

**Full-Stack**
- **FastAPI:** path/query params, Pydantic models, request/response schemas, dependency injection, async endpoints, background tasks, routers. 📌 *(Natural upgrade from Azure Functions.)* Docs: [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/).
- **REST design:** resources vs verbs, status codes, pagination, filtering, versioning, idempotency, HATEOAS basics, error envelopes.
- Middleware, CORS, rate limiting; serverless (Functions) vs long-running service — when to use each.

**AI**
- **Vector databases:** Chroma / FAISS / Pinecone / **Azure AI Search** (your strength — frame it). Indexing, metadata filtering, **hybrid search** (keyword + vector), reranking.
- **Embedding models:** `text-embedding-3-small`/`large`, dimensions, cost, model choice.
- **Hands-on:** swap your in-memory store for **Chroma** locally, then mirror it in **Azure AI Search**.

**LLD intro:** OOP pillars, **SOLID** principles (see [section 7](#7-lld-low-level-design-master-plan)). 📌

**DSA:** Stack • Queue • Linked List.  
*Problems:* Valid Parentheses, Min Stack, Evaluate RPN, Daily Temperatures, Reverse Linked List, Merge Two Sorted Lists, Linked List Cycle, Reorder List, Remove Nth Node. **(~8-10 problems)**

**Weekend project:** **FastAPI backend** for your RAG app — `/upload`, `/query`, `/health`; connect React to it.

**Checkpoint:** design a REST API for a resource • vector vs keyword vs hybrid search.

---

### WEEK 4 — SQL & Data Modeling + Function Calling + LLD patterns

**Full-Stack**
- **SQL:** `SELECT`, `WHERE`, `JOIN` (inner/left/right/full), `GROUP BY`, `HAVING`, aggregates, subqueries, CTEs, window functions (intro). Practice on [SQLBolt](https://sqlbolt.com/) + [PGExercises](https://pgexercises.com/).
- **Data modeling:** normalization (1NF-3NF), PK/FK, indexes (B-tree), when to denormalize, ACID. *(Contrast with your Cosmos/NoSQL knowledge.)*
- **ORM:** SQLAlchemy (Python) — models, sessions, migrations (Alembic).

**AI**
- **Function calling / tool use:** JSON tool schemas, how the model chooses a tool, parallel tool calls, returning results. Read [OpenAI function calling](https://platform.openai.com/docs/guides/function-calling).
- **Structured outputs / JSON mode** for reliable parsing.
- **Hands-on:** LLM that calls your Python tools (calculator, weather, a DB query function).

**LLD:** design patterns — **Factory, Strategy, Observer, Singleton, Decorator**; composition vs inheritance. Practice: **design a Parking Lot** (class diagram + code). See [Refactoring.Guru](https://refactoring.guru/design-patterns).

**DSA:** Binary Search + Trees.  
*Problems:* Binary Search, Search Rotated Sorted Array, Koko Eating Bananas, Invert Binary Tree, Max Depth, Diameter, Balanced Binary Tree, Same Tree, Lowest Common Ancestor (BST), Level Order Traversal, Validate BST. **(~8-10 problems)**

**Weekend project:** add **PostgreSQL** to your backend (users, chat history, doc metadata) + a **function-calling agent** that answers by querying the DB in natural language.

**Checkpoint:** write a JOIN + GROUP BY query • explain SOLID with one example each • Parking Lot class model.

---

### WEEK 5 — Auth, Security, Testing + AI Agents + more LLD

**Full-Stack**
- **AuthN vs AuthZ** — formalize what you did with Entra ID. 🟩
- **JWT:** structure (header.payload.signature), signing, expiry, refresh tokens, storage (httpOnly cookie vs localStorage trade-offs).
- **OAuth 2.0 / OIDC:** authorization-code + PKCE flow (maps to your App registrations).
- **Security (OWASP Top 10):** XSS, CSRF, SQL injection, SSRF, secrets management, input validation, least privilege. Ref: [OWASP Top 10](https://owasp.org/www-project-top-ten/).
- **Testing:** unit (pytest / Jest), integration, mocking, React Testing Library, coverage. 📌

**AI**
- **Agents:** ReAct (reason+act) loop, planning, memory, tool orchestration, termination. 📌
- **LangChain / LangGraph:** chains, tools, agents, memory, graph state. Docs: [LangChain](https://python.langchain.com/docs/introduction/), [LangGraph](https://langchain-ai.github.io/langgraph/).
- **Hands-on:** an agent that chooses between RAG search, a SQL tool, and a web-search tool to answer.

**LLD:** design a **Rate Limiter** (token bucket / sliding window) and an **LRU Cache** (HashMap + doubly linked list). *(LRU also appears as a DSA problem — double win.)*

**DSA:** Graphs (BFS/DFS) + Backtracking.  
*Problems:* Number of Islands, Clone Graph, Course Schedule (I & II), Pacific Atlantic, Rotting Oranges, Subsets, Combination Sum, Permutations, Word Search. **(~8-10 problems)**

**Weekend project:** add **JWT auth** (login + protected routes) and **tests** to your app; upgrade the RAG into a **LangGraph agent**.

**Checkpoint:** JWT + refresh-token flow • ReAct pattern • BFS vs DFS.

---

### WEEK 6 — DevOps + Agentic Patterns/Eval + HLD & AI System Design

**Full-Stack**
- **Docker:** images vs containers, Dockerfile, layers, multi-stage builds, `docker-compose`, volumes, networks. 📌
- **CI/CD:** GitHub Actions — lint -> test -> build -> deploy pipeline. 📌
- **Deploy:** frontend (Azure Static Web Apps / Vercel) + backend (Azure Container Apps / App Service). Env config, secrets, logging, health checks.

**AI**
- **Agentic patterns:** reflection, planning, tool-use, multi-agent, human-in-the-loop.
- **LLM evaluation:** groundedness, relevance, faithfulness, answer correctness; hallucination mitigation; offline vs online eval. Tooling: [Ragas](https://docs.ragas.io/), [LangSmith](https://docs.smith.langchain.com/).
- **Guardrails & safety:** prompt injection, jailbreaks, content filtering, PII redaction, output constraints (see roadmap.sh AI-safety topics).
- **Cost/latency:** caching, model routing, streaming, batching.

**HLD basics + AI system design** — start [section 8](#8-hld-high-level--system-design-master-plan) & [section 9](#9-ai-system-design-the-differentiator). Read the [System Design Primer](https://github.com/donnemartin/system-design-primer).

**DSA:** Heap/Priority Queue + 1-D DP.  
*Problems:* Kth Largest Element, Top K Frequent (heap), Task Scheduler, Climbing Stairs, House Robber (I & II), Coin Change, Longest Increasing Subsequence, Word Break, Decode Ways. **(~8-10 problems)**

**Weekend project:** **Dockerize** the full app, add a **GitHub Actions** pipeline, and **deploy live** to Azure. Add a small **RAG eval** script (Ragas).

**Checkpoint:** how you'd Dockerize + deploy • how you'd evaluate a RAG system • caching + load balancing basics.

---

### WEEK 7 — Capstone Projects + System Design Mocks

**Build 2 deployable, resume-worthy projects.** Pick one from each:

**Full-stack capstone:**
- Multi-tenant SaaS dashboard (auth, RBAC, CRUD, SQL, charts, responsive).
- Real-time collaborative app (WebSockets, live updates, presence).
- Job board / marketplace (search, filters, pagination, roles).

**AI capstone (play to strengths):**
- **Enterprise RAG assistant** — upload docs, **hybrid search (Azure AI Search)**, agent with tools, chat history, **citations**, eval dashboard. *(Directly showcases your Foundry/AI Search edge.)*
- Workflow-automation agent — connects APIs/tools, function calling, multi-step.
- "Chat with your database" — natural language -> SQL over a real DB.

**HLD practice (parallel):** out-loud designs — **URL shortener**, **chat app (WhatsApp)**, **scalable RAG chatbot for 1M users**. Use the 4-step method in [section 8](#8-hld-high-level--system-design-master-plan).

**DSA:** Intervals, Greedy, 2-D DP (Merge Intervals, Insert Interval, Non-overlapping Intervals, Jump Game, Unique Paths, Longest Common Subsequence).

**Deliverables:** both projects **deployed with live URLs**, clean READMEs with architecture diagrams + screenshots, good commit history.

---

### WEEK 8 — Interview Prep, Portfolio & Applications

**Resume & portfolio (Mon-Tue)**
- Reframe from "SharePoint/M365 developer" -> **Full-Stack AI Developer**. Lead with AI + full-stack; M365 is context, not the headline.
- Quantify impact (users, latency, %, scale). Two variants: full-stack-leaning and AI-leaning.
- Portfolio site or strong GitHub profile README linking both capstones. Polish LinkedIn.

**Interview drills (Wed-Sun, daily)**
- **DSA:** 2-3 **medium** problems/day, timed; mix arrays/trees/graphs/DP.
- **LLD:** Library Management, Splitwise.
- **HLD:** 2 more mock designs (news feed, rate limiter, notification system).
- **AI Q&A:** tokens, embeddings, RAG, agents, hallucination, **RAG vs fine-tuning**, prompt injection, eval — crisp 2-min answers each.
- **Behavioral (STAR):** 6-8 stories (conflict, failure, leadership, hard bug, tight deadline, ownership).
- **Mock interviews:** >= 3-4 ([Pramp](https://www.pramp.com/) / [interviewing.io](https://interviewing.io/) / a peer).

**Apply (all week):** 5-10 tailored applications/day to **full-stack** and **AI developer/engineer** roles; track in a spreadsheet.

---

## Alternative 8-week track (Python backend + DSA in parallel)

> Use this if you want Python backend and DSA to be learned **inside each week in parallel**, not as separate day blocks.  
> This keeps everything combined in one weekly flow.

| Week | Combined focus (Full-Stack + AI + Python backend + DSA + Design) |
| :--- | :--- |
| 1 | JS/TS + React internals + LLM fundamentals + Python collections/complexity + DSA Arrays/Hashing |
| 2 | CSS/Flexbox/Grid/Tailwind + Prompt engineering/RAG basics + Python generators/itertools + DSA Two Pointers/Sliding Window |
| 3 | FastAPI fundamentals + REST design + vector DBs + Python backend structuring + DSA Stack/Queue/Linked List + LLD SOLID |
| 4 | SQL/data modeling + function calling/tool use + SQLAlchemy basics + DSA Binary Search/Trees + LLD patterns |
| 5 | Auth/Security/Testing + AI agents + Python JWT/testing practice + DSA Graphs/Backtracking + LLD Rate Limiter/LRU |
| 6 | Docker/CI/CD/deploy + AI eval/guardrails + async Python backend depth + DSA Heap/1-D DP + HLD basics |
| 7 | Full-stack + AI capstones with Python backend + timed DSA (Intervals/Greedy/2-D DP) + system design mocks |
| 8 | Portfolio/resume/applications + mixed Python DSA drills + mock interviews across full-stack, AI, LLD, HLD |

**Daily rhythm for this track (same day, parallel blocks, 2-3 hrs/day):**
- 40-45 min DSA in Python
- 45-60 min Python backend or full-stack implementation
- 45-60 min AI concepts/hands-on
- 15-20 min LLD/HLD design communication practice

---

## Python Mastery for interviews & backend

> You know Python syntax; the gap is **interview-grade fluency** (solving DSA in Python fast) and **backend-writing muscle memory**. Rule for the whole roadmap: **solve every DSA problem in Python** and **write every backend in Python** so the language stops being something you think about. Reference: [official docs](https://docs.python.org/3/), and read *Fluent Python* (book) if you want mastery depth.

### 5.1 • Python language depth (interview-critical)
These are the exact things interviewers probe and that make coding fast:
- **Core data structures & their APIs:** `list`, `tuple`, `dict`, `set`, `frozenset` — operations, mutability, and **time complexity** of each (e.g., `list.append` O(1), `x in list` O(n), `x in set` O(1)).
- **`collections` module (huge for DSA):** `deque` (O(1) queue/stack), `defaultdict`, `Counter`, `OrderedDict`, `namedtuple`.
- **`heapq`** (min-heap; simulate max-heap with negatives) and **`bisect`** (binary search on sorted lists) — used constantly in interviews.
- **Comprehensions & generators:** list/dict/set comprehensions, generator expressions, `yield`, lazy evaluation, memory trade-offs.
- **Iteration tools:** `enumerate`, `zip`, `sorted(key=..., reverse=...)`, `map`/`filter`, `itertools` (`product`, `permutations`, `combinations`, `accumulate`, `groupby`).
- **Strings:** immutability, slicing, `join`, `split`, f-strings, `ord`/`chr`, why building strings with `+` in loops is O(n^2) (use lists + `join`).
- **Functions:** `*args`/`**kwargs`, default-arg pitfalls (mutable defaults), closures, decorators, `functools` (`lru_cache`, `reduce`, `partial`), `lambda`.
- **OOP in Python (for LLD):** classes, `__init__`, `__repr__`/`__str__`, `__eq__`/`__hash__`, dunder methods, `@property`, `@classmethod`/`@staticmethod`, `@dataclass`, `abc`/`Protocol` for interfaces, `enum`.
- **Typing:** type hints, `Optional`, `Union`/`|`, `list[int]`, `dict[str, Any]`, `TypedDict`, `Literal`, generics — matters for backend + readable interview code.
- **Idioms & gotchas:** truthiness, `is` vs `==`, tuple unpacking, `for/else`, context managers (`with`, `contextlib`), EAFP vs LBYL, shallow vs deep copy, integer caching, default mutable args, late-binding closures.
- **Concurrency (know the concepts):** the **GIL**, threading vs multiprocessing vs `asyncio`, `async`/`await`, when each applies (I/O-bound vs CPU-bound). Important for backend + system-design answers.
- **Error handling:** exceptions, custom exception classes, `try/except/else/finally`, raising and chaining.
- **Testing:** `pytest`, fixtures, parametrize, mocking (`unittest.mock`), coverage.

### 5.2 • Python for DSA (solve fluently)
Map each pattern to its Python tool so you reach for the right one instantly:

| DSA pattern | Python tool of choice |
| :--- | :--- |
| Hashing / frequency | `dict`, `set`, `collections.Counter` |
| Stack | `list` (`append` / `pop`) |
| Queue / BFS | `collections.deque` |
| Heap / top-K | `heapq` (negate for max-heap) |
| Binary search | `bisect` or manual `lo/hi` |
| Sorting with key | `sorted(arr, key=lambda x: ...)` |
| Memoization / DP | `functools.lru_cache` or a `dict` |
| Graph adjacency | `defaultdict(list)` |
| Backtracking | recursion + list as path, `append` / `pop` |
| Intervals | `sorted` + tuple comparison |

**Practice cadence:** every DSA problem in [section 6](#6-dsa-master-plan) is solved in Python. After solving, **rewrite the clean version from memory** — this builds writing speed. Do a weekly "blank editor" drill: reimplement 3 solved problems with no references.

### 5.3 • Python for backend (writing muscle)
Since your backend thinking is in Python, go deep here (Weeks 3-6):
- **FastAPI** end-to-end: routers, Pydantic v2 models, dependency injection, async endpoints, background tasks, middleware, exception handlers, `BackgroundTasks`, streaming responses. [Tutorial](https://fastapi.tiangolo.com/tutorial/).
- **Pydantic:** validation, field constraints, `model_validator`, settings management (`pydantic-settings`).
- **DB access:** SQLAlchemy (2.0 style) + Alembic migrations; async drivers (`asyncpg`); connection pooling.
- **Auth:** hashing (`passlib`/`bcrypt`), JWT (`python-jose`), OAuth2 password/bearer flows in FastAPI.
- **Project structure:** routers/services/repositories layering, config via env, dependency wiring, `.env` + `pydantic-settings`.
- **Async HTTP:** `httpx` for calling external/AI APIs; retries, timeouts.
- **Packaging & env:** `venv`, `pip`/`poetry`/`uv`, `requirements.txt`/`pyproject.toml`, `ruff` (lint+format), `mypy` (type-check).
- **Testing backend:** `pytest` + FastAPI `TestClient`, fixtures for DB, mocking external/AI calls.

### 5.4 • Python week-by-week focus (overlay on the main plan)

| Week | Python focus |
| :--- | :--- |
| 1 | Data structures + complexity, comprehensions, `collections`, `heapq`/`bisect`, f-strings, slicing |
| 2 | Generators, `itertools`, `sorted(key=)`, string-building patterns, `functools.lru_cache` |
| 3 | FastAPI basics, Pydantic models, project structure, `httpx`, OOP dunders |
| 4 | SQLAlchemy + Alembic, dataclasses/`abc`/`Protocol` for LLD, typing depth |
| 5 | Auth (JWT/passlib), pytest + TestClient, decorators, context managers |
| 6 | `asyncio` + async FastAPI, GIL/threading vs multiprocessing, packaging & tooling (`ruff`/`mypy`) |
| 7-8 | Capstone backends in Python; timed Python DSA drills; explain your code out loud |

### 5.5 • Python interview question bank (be ready to explain)
- What's the time complexity of `in` on a list vs a set? Why?
- List vs tuple vs set vs dict — when to use each?
- How does `dict` maintain insertion order (3.7+)? How do hashing collisions work?
- What is the GIL? How does it affect threading? When use multiprocessing vs asyncio?
- `deepcopy` vs `copy` vs assignment? Mutable default argument trap?
- `is` vs `==`? When can `==` be True but `is` False?
- Generators vs lists — memory and use cases? What does `yield` do?
- How do decorators work? Write a timing/`lru_cache`-style decorator.
- `@staticmethod` vs `@classmethod` vs instance method?
- How would you make a class hashable / usable as a dict key? (`__eq__` + `__hash__`)
- Simulate a max-heap with `heapq`. Use `bisect` to insert into a sorted list.
- EAFP vs LBYL — which is "Pythonic" and why?

---

## Optional extension (Weeks 9-12)

The 8-week core makes you interview-ready. If you can invest more time, these weeks add depth and polish (do the ones matching your target companies):

- **Week 9 — DSA reinforcement:** Tries, Advanced Graphs (Dijkstra, Union-Find, topological sort), Bit Manipulation, harder 2-D DP; ~25 more mediums + first hards. Re-solve your weakest patterns from memory.
- **Week 10 — System design depth:** 4 more HLD designs (Uber, Dropbox, YouTube, notification system), 3 more LLD (Chess, Vending Machine, Logging framework); practice back-of-envelope estimation and drawing architecture diagrams fast.
- **Week 11 — AI depth:** advanced RAG (query rewriting, HyDE, reranking models, GraphRAG), multi-agent systems, structured-output reliability, production eval + guardrails, cost/latency optimization, streaming; a small **fine-tuning / adapters** overview so you can compare RAG vs fine-tuning credibly.
- **Week 12 — Polish & scale applications:** 2 more mock interviews per track, refine both capstones (add tests, monitoring, docs), write a short technical blog post per capstone (great signal), and ramp applications to 10+/day with tailored resumes.

> Guiding principle: **don't sacrifice depth for the calendar.** If Week 4 SQL or Week 5 graphs needs an extra few days, take it. Mastery + working projects beat rushing to a deadline.

---

## 6. DSA master plan

> **How to use this section:** follow it **top to bottom**. Do **Phase 0** first (build each data structure yourself in Python), then work the **problem checklist** in order. Every problem is named and checkboxed — you never need to go search "what's next" or "how many." When you finish the last box, you're done. Solve everything **in Python**.
>
> **Where to solve:** each problem below is a real LeetCode problem — search its exact name on [leetcode.com](https://leetcode.com/) (all are in the free tier or NeetCode's list). That's the only external step; the *what* and the *order* live here.

### Phase 0 — Build the data structures from scratch in Python (Week 1, before problems)
You know Python syntax, but interviewers expect you to **implement** these, not just use the built-ins. Build each one in a file, with the listed operations, and test it. This is your "zero level" foundation.

- [ ] **Dynamic array** — implement `append`, `get(i)`, `set(i)`, `pop`, `insert(i)`, `delete(i)`. Understand why `append` is amortized O(1). *(Python `list` is already this — reimplement to understand it.)*
- [ ] **Stack** (LIFO) — `push`, `pop`, `peek`, `is_empty`. Use a Python `list`. O(1) ops.
- [ ] **Queue** (FIFO) — `enqueue`, `dequeue`, `peek`. Use `collections.deque` (O(1)); understand why a plain `list` dequeue is O(n).
- [ ] **Deque** — double-ended; `append`, `appendleft`, `pop`, `popleft`.
- [ ] **Singly linked list** — `Node` class + `add_front`, `add_back`, `delete(val)`, `find(val)`, `reverse`, `print_list`.
- [ ] **Doubly linked list** — `prev`/`next` pointers; `add`, `remove(node)` in O(1). *(Foundation for LRU Cache.)*
- [ ] **Hash map** (from scratch) — array of buckets + hashing + collision handling (chaining). `put`, `get`, `remove`. Understand average O(1) vs worst O(n).
- [ ] **Binary tree** — `TreeNode` class; build a small tree; write all 4 traversals: inorder, preorder, postorder (recursive), and level-order (BFS with a `deque`).
- [ ] **Binary search tree (BST)** — `insert`, `search`, `delete`, `find_min`, in-order traversal (gives sorted order). Understand O(log n) vs O(n) when unbalanced.
- [ ] **Min-heap** (from scratch) — array-backed; `push` (bubble up), `pop` (bubble down), `peek`. Then learn to use `heapq`; simulate a max-heap by negating values.
- [ ] **Graph** — represent with `defaultdict(list)` (adjacency list); write **BFS** (deque) and **DFS** (recursive + iterative with a stack).
- [ ] **Trie** (prefix tree) — `TrieNode` with children dict; `insert`, `search`, `starts_with`.

> After building each: write down its operations' **time/space complexity** on a cheat card. This is directly asked in interviews.

---

### The problem checklist (work in this order)
Target = **~120 problems**. Order matches the [NeetCode roadmap](https://neetcode.io/roadmap). Check each box as you solve it in Python; re-solve any you struggled with after 2-3 days.

#### 1. Arrays & Hashing (Week 1)
- [ ] Contains Duplicate
- [ ] Valid Anagram
- [ ] Two Sum
- [ ] Group Anagrams
- [ ] Top K Frequent Elements
- [ ] Product of Array Except Self
- [ ] Valid Sudoku
- [ ] Longest Consecutive Sequence

#### 2. Two Pointers (Week 2)
- [ ] Valid Palindrome
- [ ] Two Sum II (sorted input)
- [ ] 3Sum
- [ ] Container With Most Water
- [ ] Trapping Rain Water

#### 3. Sliding Window (Week 2)
- [ ] Best Time to Buy and Sell Stock
- [ ] Longest Substring Without Repeating Characters
- [ ] Longest Repeating Character Replacement
- [ ] Permutation in String
- [ ] Minimum Window Substring

#### 4. Stack (Week 3)
- [ ] Valid Parentheses
- [ ] Min Stack
- [ ] Evaluate Reverse Polish Notation
- [ ] Generate Parentheses
- [ ] Daily Temperatures
- [ ] Car Fleet

#### 5. Linked List (Week 3)
- [ ] Reverse Linked List
- [ ] Merge Two Sorted Lists
- [ ] Linked List Cycle
- [ ] Reorder List
- [ ] Remove Nth Node From End of List
- [ ] Copy List with Random Pointer
- [ ] Add Two Numbers
- [ ] LRU Cache

#### 6. Binary Search (Week 4)
- [ ] Binary Search
- [ ] Search a 2D Matrix
- [ ] Koko Eating Bananas
- [ ] Find Minimum in Rotated Sorted Array
- [ ] Search in Rotated Sorted Array
- [ ] Median of Two Sorted Arrays

#### 7. Trees (Week 4)
- [ ] Invert Binary Tree
- [ ] Maximum Depth of Binary Tree
- [ ] Diameter of Binary Tree
- [ ] Balanced Binary Tree
- [ ] Same Tree
- [ ] Subtree of Another Tree
- [ ] Lowest Common Ancestor of a BST
- [ ] Binary Tree Level Order Traversal
- [ ] Validate Binary Search Tree
- [ ] Kth Smallest Element in a BST
- [ ] Construct Tree from Preorder and Inorder

#### 8. Tries (Week 5)
- [ ] Implement Trie (Prefix Tree)
- [ ] Design Add and Search Words Data Structure
- [ ] Word Search II

#### 9. Backtracking (Week 5)
- [ ] Subsets
- [ ] Combination Sum
- [ ] Permutations
- [ ] Subsets II
- [ ] Word Search
- [ ] Palindrome Partitioning
- [ ] N-Queens

#### 10. Graphs (Week 5)
- [ ] Number of Islands
- [ ] Clone Graph
- [ ] Pacific Atlantic Water Flow
- [ ] Course Schedule
- [ ] Course Schedule II
- [ ] Rotting Oranges
- [ ] Graph Valid Tree
- [ ] Number of Connected Components in an Undirected Graph

#### 11. Heap / Priority Queue (Week 6)
- [ ] Kth Largest Element in a Stream
- [ ] Last Stone Weight
- [ ] K Closest Points to Origin
- [ ] Kth Largest Element in an Array
- [ ] Task Scheduler
- [ ] Find Median from Data Stream

#### 12. 1-D Dynamic Programming (Week 6)
- [ ] Climbing Stairs
- [ ] Min Cost Climbing Stairs
- [ ] House Robber
- [ ] House Robber II
- [ ] Longest Palindromic Substring
- [ ] Coin Change
- [ ] Longest Increasing Subsequence
- [ ] Word Break
- [ ] Decode Ways

#### 13. 2-D Dynamic Programming (Week 7)
- [ ] Unique Paths
- [ ] Longest Common Subsequence
- [ ] Edit Distance
- [ ] Coin Change II
- [ ] 0/1 Knapsack (study the pattern)

#### 14. Intervals (Week 7)
- [ ] Insert Interval
- [ ] Merge Intervals
- [ ] Non-overlapping Intervals
- [ ] Meeting Rooms
- [ ] Meeting Rooms II

#### 15. Greedy (Week 7)
- [ ] Maximum Subarray
- [ ] Jump Game
- [ ] Jump Game II
- [ ] Gas Station
- [ ] Hand of Straights

#### 16. Advanced (bonus) (Week 8 / extension)
- [ ] Number of 1 Bits (bit manipulation)
- [ ] Counting Bits
- [ ] Reverse Bits
- [ ] Network Delay Time (Dijkstra)
- [ ] Number of Provinces (Union-Find)
- [ ] Alien Dictionary (topological sort)

> **Method for every problem:** read -> try brute force -> optimize -> code in Python -> state time/space Big-O out loud -> if stuck >30 min, read the solution, understand it, then **re-solve from scratch the next day**. Weekly: reimplement 3 past problems in a blank file to build writing speed.

---

## 7. LLD (Low-Level Design) master plan

### Concepts (Weeks 3-5)
- **OOP pillars:** encapsulation, abstraction, inheritance, polymorphism.
- **SOLID:** Single Responsibility • Open/Closed • Liskov Substitution • Interface Segregation • Dependency Inversion — be able to give one concrete example each.
- **Composition over inheritance**, DRY, KISS, YAGNI.
- **Design patterns** (learn on [Refactoring.Guru](https://refactoring.guru/design-patterns)):
  - *Creational:* Factory, Abstract Factory, Builder, Singleton
  - *Structural:* Adapter, Decorator, Facade, Proxy
  - *Behavioral:* Strategy, Observer, State, Command
- **UML basics:** class diagrams, relationships (association, aggregation, composition, inheritance).

### Practice designs (do 6)
**Parking Lot • Rate Limiter • LRU Cache • Elevator System • Library Management • Splitwise.**  
For each: requirements -> core classes/interfaces -> relationships -> key methods -> extendability.  
*References:* [system-design-primer OOD questions](https://github.com/donnemartin/system-design-primer#object-oriented-design-interview-questions-with-solutions) and [awesome-low-level-design](https://github.com/ashishps1/awesome-low-level-design).

---

## 8. HLD (High-Level / System Design) master plan

- **Primary resource:** [System Design Primer](https://github.com/donnemartin/system-design-primer) (371k★).  
- **Supplement:** [ByteByteGo](https://bytebytego.com/) / Alex Xu's *System Design Interview* books.

### Core concepts to master (Weeks 6-8)
- **Scaling:** vertical vs horizontal, stateless services, load balancers (L4/L7), reverse proxy.
- **Caching:** client / CDN / server / DB; strategies — cache-aside, write-through, write-behind, refresh-ahead; eviction (LRU); Redis/Memcached.
- **Databases:** SQL vs NoSQL choice, replication (master-slave/master-master), **sharding**, federation, denormalization, indexing, ACID vs BASE.
- **CAP theorem** (CP vs AP), consistency models (strong/eventual/weak).
- **CDN** (push vs pull), **DNS**.
- **Asynchronism:** message queues (Kafka/RabbitMQ/SQS), task queues (Celery), back-pressure.
- **Communication:** HTTP verbs & idempotency, REST vs RPC vs GraphQL, WebSockets, gRPC.
- **Availability:** (9s), fail-over, rate limiting, idempotency keys.
- **Estimation:** back-of-the-envelope (QPS, storage, bandwidth); powers-of-two & latency numbers.

### The 4-step interview method (from the Primer)
1. **Requirements & constraints** — users, use cases, QPS, read/write ratio, data size.
2. **High-level design** — main components + connections; justify.
3. **Core components** — deep-dive APIs, data model, algorithms.
4. **Scale** — find bottlenecks; add LB, caching, sharding, queues; discuss trade-offs.

### Practice designs (do 6)
**URL shortener (Bit.ly) • Twitter timeline / news feed • Chat app (WhatsApp) • Rate limiter • Notification system • Web crawler.**

---

## 9. AI system design (the differentiator)

This extra round is where your background wins. Be ready to design **LLM-powered systems at scale**:

- **Design a scalable RAG chatbot (1M users):** ingestion pipeline (chunk -> embed -> index), vector DB choice & sharding, retrieval + reranking, prompt assembly, LLM gateway, **caching** (semantic cache), **streaming** responses, **rate limiting & cost control**, **evaluation/guardrails**, observability/tracing, fallbacks.
- **Design an AI agent platform:** tool registry, function-calling orchestration, state/memory store, retries/timeouts, human-in-the-loop, safety filters.
- **Key trade-offs to discuss:**
  - **RAG vs fine-tuning** (freshness, cost, control)
  - Chunk size vs recall
  - Context window vs cost
  - Latency vs quality (model routing)
  - Hallucination mitigation (grounding + citations + eval)
- **Ops concerns unique to AI:** token cost budgeting, prompt versioning, PII handling, prompt-injection defense, model/version pinning, A/B evals.

Grounding topics from [roadmap.sh AI Engineer](https://roadmap.sh/ai-engineer): LLM inference, vector DBs, RAG, prompt engineering, AI agents, AI safety & ethics, observability.

---

## 10. Interview topic checklists

### Full-Stack
- [ ] JS event loop, closures, async, prototypes
- [ ] TS generics & utility types
- [ ] React rendering, hooks, memoization, performance
- [ ] State management trade-offs
- [ ] CSS: Flexbox, Grid, responsive
- [ ] REST design, status codes, idempotency
- [ ] SQL: JOINs, indexing, normalization, ACID
- [ ] NoSQL vs SQL trade-offs
- [ ] Auth: JWT, OAuth2/OIDC, sessions
- [ ] Security: OWASP Top 10
- [ ] Testing (unit/integration/mocking)
- [ ] Docker & CI/CD

### DSA
- [ ] All 16 patterns in [section 6](#6-dsa-master-plan)

### LLD
- [ ] SOLID (one example each)
- [ ] Composition vs inheritance
- [ ] Factory, Strategy, Observer, Singleton, Decorator
- [ ] 6 practiced designs

### HLD
- [ ] Scaling, LB, caching, CDN
- [ ] Replication, sharding, CAP, consistency
- [ ] Message queues, async
- [ ] Estimation
- [ ] 6 practiced designs

### AI
- [ ] Tokens, context windows, tokenization
- [ ] Embeddings & vector similarity
- [ ] Prompting (few-shot, CoT, structured output)
- [ ] RAG pipeline (chunking, retrieval, hybrid, rerank)
- [ ] Vector DBs (Azure AI Search)
- [ ] Function calling / tool use
- [ ] Agents (ReAct, LangGraph)
- [ ] Agentic patterns (reflection, planning, multi-agent)
- [ ] Evaluation & hallucination mitigation
- [ ] RAG vs fine-tuning
- [ ] Prompt injection & guardrails
- [ ] AI system design at scale

---

## Behavioral & soft-skills interview prep (complete package)

> This is your **first interview ever**, so read this whole section twice and practice the answers **out loud**. Technical skill gets you in the room; **how you communicate** gets you the offer. Everything here is self-contained — templates, sample answers tailored to your background, and vetted links at the end.

### A. The golden rule for every behavioral question: STAR
Answer stories in four beats so you never ramble:
- **S — Situation:** 1-2 sentences of context (what/where).
- **T — Task:** what *you* were responsible for.
- **A — Action:** what *you specifically* did (say "I", not "we"). This is 60% of the answer.
- **R — Result:** the outcome, ideally with a number or clear impact. Add what you learned.

Keep each STAR answer to **~90 seconds**. Prepare **6-8 stories** from your real work and reuse them across questions.

**Your story bank (fill these from your real experience — write them once, reuse everywhere):**
1. A technical challenge you solved (e.g., a tricky RAG/Azure AI Search retrieval or performance issue).
2. A project you're proud of end-to-end (React + Azure Functions + AI feature).
3. A time you handled a tight deadline.
4. A conflict or disagreement (with a colleague/stakeholder) and how you resolved it.
5. A failure or mistake and what you learned.
6. A time you learned something new fast (great for your "broadening beyond M365" story).
7. A time you took ownership / went beyond your role.
8. A time you improved a process (Power Automate automation, reusable component, etc.).

---

### B. "Tell me about yourself" (your opening — rehearse this cold)
Structure: **Present -> Past -> Future**, ~60-90 seconds. Talk about work only, not personal life.

> *Sample (adapt the specifics):* "I'm a developer with **3 years of experience** building web applications, mostly with **React and TypeScript on the frontend and Python on the backend**. A lot of my work has been building **UI and REST APIs with Azure Functions** inside the Microsoft 365 ecosystem, and more recently **AI features** — I've built **RAG chatbots using Azure AI Foundry and Azure AI Search**, wired up authentication with Entra ID, and worked with Cosmos DB and storage services. *(Past)* Over these years I've become strong at the **logical side of development** — data flow, API integration, and turning requirements into working features. *(Future)* Now I'm focused on growing into a **full-stack AI developer** role where I can own features end-to-end — frontend, backend, and the AI layer — which is exactly why this role interests me."

Tip: end "tell me about yourself" by pointing at **why you want *this* role** — it hands the interviewer the next question.

---

### C. The most-asked behavioral questions + how to answer (with samples)

#### 1. "Why are you looking to change / leave your current job?"
Rule: **stay positive**, never bad-mouth your employer. Frame it as growth.
> *Sample:* "I've learned a lot building solutions in the Microsoft 365 space, but my work has been fairly focused on that ecosystem. I want to grow as a **broader full-stack and AI engineer** — work across more of the stack, different databases, and modern AI systems — and this role gives me exactly that scope."

#### 2. "Why do you want to work here / this role?"
Do 15 minutes of research on the company first. Connect **their needs -> your skills**.
> *Sample:* "You're building [product/AI feature], and I've spent the last while building exactly this kind of thing — React frontends, Python APIs, and RAG-based AI features. I'm excited to bring that and keep growing on a team that's [something specific you found]."

#### 3. "What are your strengths?"
Pick 2-3 with evidence.
> *Sample:* "My biggest strength is **logical problem-solving and integration** — taking dynamic data, APIs, and business rules and turning them into working features. I'm also a **fast learner** — I picked up Azure AI Foundry and RAG on the job and shipped working chatbots. And I take **ownership** — I follow a feature from UI through the API to the data."

#### 4. "What's your weakness?"
Give a **real** one + what you're actively doing about it. Don't use a fake humble-brag.
> *Sample:* "Because my work centered on the Microsoft 365 stack, my exposure to things like **relational databases and broad system design** was limited. I'm actively closing that — I'm working through SQL, data modeling, and system design and building full-stack projects outside that ecosystem." *(Alt: "I used to jump into coding before fully clarifying requirements; now I confirm scope and edge cases first, which has cut my rework.")*

#### 5. "Where do you see yourself in 3-5 years?" / future goals
Show ambition + commitment to growing *as an engineer* (not "I want your job" or "I don't know").
> *Sample:* "In a few years I want to be a **strong full-stack AI engineer** who can own complex features end-to-end — architecture, backend, frontend, and the AI layer — and mentor others. AI is moving fast, so I want to keep growing with it and take on more technical ownership over time."

#### 6. "Tell me about a challenging project."
Use STAR story #1 or #2.
> *Skeleton:* **(S)** We were building a RAG chatbot over company documents. **(T)** I owned the retrieval quality, which was returning irrelevant answers. **(A)** I diagnosed it to poor chunking and pure keyword search, so I redesigned the chunking with overlap, switched to **hybrid search in Azure AI Search**, and added a re-ranking step. **(R)** Answer relevance improved noticeably and user complaints dropped. I learned how much retrieval design drives RAG quality.

#### 7. "Tell me about a conflict / disagreement."
Show maturity: listen, use data, find common ground.
> *Skeleton:* **(S)** A stakeholder wanted a feature one way; I thought it'd cause performance issues. **(T)** I needed to deliver something that worked without dismissing them. **(A)** I listened to their goal, explained my concern with a quick prototype showing the trade-off, and proposed an alternative that met their need. **(R)** We aligned on the alternative and shipped it; the relationship stayed strong.

#### 8. "Tell me about a failure / mistake."
Own it, don't blame, focus on the lesson.
> *Skeleton:* **(S/T)** I once pushed a change that broke a shared list integration. **(A)** I owned it immediately, rolled back, added validation and a test, and communicated clearly to the team. **(R)** It was fixed quickly and I added tests that prevented similar issues. I learned to guard integration points with tests.

#### 9. "How do you handle tight deadlines / pressure?"
STAR story #3: prioritize, communicate early, cut scope smartly.

#### 10. "Tell me about a time you learned something quickly."
Your AI/Azure Foundry ramp-up. Perfect fit.

---

### D. During the technical interview — how to communicate
- **Think out loud.** Interviewers score your *reasoning*, not just the final answer.
- **Clarify first:** restate the problem, ask about inputs, edge cases, and constraints before coding.
- **Start simple:** state a brute-force approach, then optimize — don't sit silent hunting for the perfect solution.
- **Narrate trade-offs:** "I'll use a hash set for O(1) lookups at the cost of O(n) space."
- **If you're stuck:** say what you're thinking and what you'd try; it's fine to ask for a hint. Silence is the enemy.
- **If you don't know something:** say "I haven't used that directly, but here's how I'd reason about it / find out." Never bluff — interviewers can tell.
- **Test your code:** walk through an example, check edge cases, state the Big-O.
- **Stay calm and positive** even if it's hard — composure is part of the score.

---

### E. Questions YOU should ask them (always have 3-4 ready)
Not asking questions signals low interest. Good ones:
- "What does a typical day/week look like for this role?"
- "What are the biggest technical challenges the team is tackling right now?"
- "How is success measured in the first 3-6 months?"
- "What does the tech stack and deployment process look like?"
- "How does the team approach code reviews, testing, and learning/growth?"
- "How is AI being adopted on the team / in the product?" *(shows forward thinking)*

*Avoid leading with salary/vacation in the first technical round.*

---

### F. Salary negotiation (you *can* do this — here's how)
> Read **Patrick McKenzie's "Salary Negotiation"** (link below) once fully — it's the best free guide and will make you far more confident.

**Before:** research the range for your role, level, and city on **Levels.fyi**, **Glassdoor**, and **LinkedIn Salary**. Know three numbers: your **walk-away minimum**, your **target**, and an **ambitious anchor**.

**Core rules:**
1. **Don't say a number first if you can avoid it.** If asked "what's your expectation?" early, deflect: *"I'd like to learn more about the role and level first — what range do you have budgeted for this position?"*
2. **If you must give one, give a researched range** with your target near the bottom: *"Based on my research for this role and my experience, I'm looking in the range of X to Y."* Anchor slightly high; they'll negotiate down.
3. **Never accept on the spot.** Say: *"Thank you, I'm excited about this. Can I take a day to review the full offer?"* This is normal and expected.
4. **Negotiate the whole package**, not just base: signing bonus, stock, joining date, learning budget, remote flexibility.
5. **Counter once, politely, with justification:** *"I'm really enthusiastic about joining. Based on my experience with full-stack and AI development and the market range, could we get the base to Z? If we can reach that, I'm ready to sign."*
6. **Get the final offer in writing** before resigning anywhere.
7. **Stay warm and collaborative** — negotiation is not a fight; you'll work with these people.

---

### G. Logistics — before, during, after
- **Before:** research the company + interviewers, re-read the job description, prepare your STAR stories and questions, test your camera/mic/internet (for virtual), dress neatly, have water and your resume nearby.
- **During:** arrive/join 5 min early, smile, be concise, be honest, take a breath before answering hard questions.
- **After:** send a short **thank-you email** within 24 hours to each interviewer ("Thanks for your time — I enjoyed discussing X and I'm even more excited about the role"). It's a small edge many candidates skip.

---

### H. Behavioral prep resources (vetted)
- Tech Interview Handbook – Behavioral guide: https://www.techinterviewhandbook.org/behavioral-interview/
- STAR method (Indeed): https://www.indeed.com/career-advice/interviewing/how-to-use-the-star-interview-response-technique
- "Tell me about yourself" (Indeed): https://www.indeed.com/career-advice/interviewing/interview-question-tell-me-about-yourself
- Amazon Leadership Principles (great behavioral question bank): https://www.amazon.jobs/content/en/our-workplace/leadership-principles
- Patrick McKenzie – Salary Negotiation (must-read): https://www.kalzumeus.com/2012/01/23/salary-negotiation-make-more-money-be-more-valued/
- Levels.fyi (compensation data): https://www.levels.fyi/
- Glassdoor (salaries + company reviews + real interview questions): https://www.glassdoor.com/
- Exponent (behavioral + system design practice): https://www.tryexponent.com/
- Big Interview / your local career center for mock behavioral practice

---

## 11. Curated resource library (vetted links)

**Roadmaps**
- Full-Stack: https://roadmap.sh/full-stack
- AI Engineer: https://roadmap.sh/ai-engineer

**Frontend / TS**
- MDN Web Docs: https://developer.mozilla.org/
- TypeScript Handbook: https://www.typescriptlang.org/docs/handbook/intro.html
- React docs: https://react.dev/
- Tailwind: https://tailwindcss.com/docs
- Flexbox Froggy: https://flexboxfroggy.com/ • Grid Garden: https://cssgridgarden.com/
- The Odin Project: https://www.theodinproject.com/

**Python (language + backend)**
- Official docs / tutorial: https://docs.python.org/3/tutorial/
- Real Python (guides): https://realpython.com/
- `collections` • `heapq` • `bisect` • `itertools` • `functools` — study these std-lib pages directly
- Pydantic: https://docs.pydantic.dev/
- SQLAlchemy: https://docs.sqlalchemy.org/ • Alembic: https://alembic.sqlalchemy.org/
- pytest: https://docs.pytest.org/
- Ruff: https://docs.astral.sh/ruff/ • mypy: https://mypy.readthedocs.io/
- Python patterns for DSA (LeetCode discuss + NeetCode solutions are in Python)

**Backend / DB**
- FastAPI: https://fastapi.tiangolo.com/tutorial/
- SQLBolt: https://sqlbolt.com/ • PGExercises: https://pgexercises.com/
- SQLAlchemy: https://docs.sqlalchemy.org/

**DSA**
- NeetCode (roadmap + patterns): https://neetcode.io/roadmap
- LeetCode Top Interview 150: https://leetcode.com/studyplan/top-interview-150/
- Grokking the Coding Interview (paid): https://www.educative.io/

**LLD / HLD**
- System Design Primer: https://github.com/donnemartin/system-design-primer
- Refactoring.Guru (patterns): https://refactoring.guru/design-patterns
- Awesome Low-Level Design: https://github.com/ashishps1/awesome-low-level-design
- ByteByteGo: https://bytebytego.com/
- Grokking the System Design Interview (paid): https://www.educative.io/

**AI**
- OpenAI docs: https://platform.openai.com/docs/
- OpenAI Tokenizer: https://platform.openai.com/tokenizer
- Prompt engineering guide: https://www.promptingguide.ai/
- Azure AI Foundry docs: https://learn.microsoft.com/azure/ai-studio/
- Azure AI Search: https://learn.microsoft.com/azure/search/
- LangChain: https://python.langchain.com/docs/introduction/
- LangGraph: https://langchain-ai.github.io/langgraph/
- Ragas (eval): https://docs.ragas.io/
- LangSmith (tracing): https://docs.smith.langchain.com/
- DeepLearning.AI short courses (free): https://www.deeplearning.ai/short-courses/

**Security**
- OWASP Top 10: https://owasp.org/www-project-top-ten/

**Mock interviews**
- Pramp / interviewing.io: https://www.pramp.com/ • https://interviewing.io/

---

## 12. Projects & portfolio

| Week | Project | Combines |
| :--- | :--- | :--- |
| 1 | Smart Notes + AI summarize | React/TS + OpenAI |
| 2 | Tailwind responsive UI + RAG chat | CSS + RAG |
| 3 | FastAPI backend for RAG | Backend + REST |
| 4 | PostgreSQL + function-calling agent | SQL + tools |
| 5 | JWT auth + tests + LangGraph agent | Auth + agents |
| 6 | Dockerized + CI/CD + deployed + eval | DevOps + eval |
| 7 | **Full-stack capstone** + **AI capstone** | Everything |

**Portfolio must-haves:** live URLs, READMEs with architecture diagrams + screenshots, clean commits, and a one-line "what/why/stack" per project.

---

## 13. Progress tracker

| Week | Full-Stack 🟩 | AI 🟩 | DSA (n) | LLD/HLD | Project | Notes |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| 1 | [ ] [ ] | [ ] | /10 | — | [ ] | |
| 2 | [ ] [ ] | [ ] | /10 | — | [ ] | |
| 3 | [ ] [ ] | [ ] | /10 | SOLID [ ] | [ ] | |
| 4 | [ ] [ ] | [ ] | /10 | Patterns + Parking Lot | [ ] | |
| 5 | [ ] [ ] | [ ] | /10 | Rate Limiter + LRU [ ] | [ ] | |
| 6 | [ ] [ ] | [ ] | /10 | HLD + AI design [ ] | [ ] | |
| 7 | [ ] [ ] | [ ] | Capstones | 3 HLD mocks [ ] | [ ] | |
| 8 | [ ] [ ] | [ ] | Timed | Behavioral + mocks [ ] | [ ] | |

**End-state targets:** ~120 DSA solved • 6 mini-projects + 2 deployed capstones • 6 LLD + 6 HLD designs practiced • resume + portfolio ready • applying daily.

---

## Your positioning (read before every interview)

Your **unfair advantage** is real, shipped **enterprise AI** on Azure (Foundry, AI Search, RAG, Entra ID auth, Cosmos). Most candidates only have toy OpenAI demos. Lead with that. This roadmap fills your breadth gaps (CSS, SQL, DSA, LLD, HLD) so you can confidently call yourself a **Full-Stack AI Developer** — not a SharePoint developer.
