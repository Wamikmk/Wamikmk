Wamiq Mushtaq

Final-year BS in Data Science & Applications at IIT Madras.
I build ML systems, Python automation, AI agents, and interactive explainers. When a project teaches me something about how to build or how to learn, I write the playbook so the next one doesn't start from zero.

Selected work

__[Customer Activation Engine](https://github.com/Wamikmk/activation-engine)__   FastAPI · Claude API · Python
A scoring and routing system for fintech users who finish KYC but never deposit, the 85% to 95% drop-off that is simultaneously the industry's biggest revenue leak and an underbuilt problem. Five-factor priority score: exponential decay for recency, log scaling for engagement, weighted combination tunable without rewriting logic. The router reads the score breakdown, not the total. Two customers at 65/100 rarely need the same action. Graceful degradation all the way down: LLM emails fall back to templates when the API key is missing.

__[Multi-Domain Support Triage Agent](https://github.com/Wamikmk/hackerrank-orchestrate-may26)__   Python · Claude API · fastembed · 149th place, HackerRank Orchestrate May 2026
A terminal agent that reads a support ticket and decides whether to answer it from documentation or escalate. Built solo in about 10 hours. Five stages in sequence: regex safety net, Haiku 4.5 classifier, cosine retrieval over 4,026 embedded doc chunks (HackerRank, Claude, Visa), pure-Python decision layer, Sonnet 4.5 generator. Haiku does the classifying because Sonnet is roughly 15x more expensive per token and the task is enum-constrained JSON; Sonnet only runs on tickets that actually need a grounded reply. Retrieval is `np.dot` over an L2-normalized 6.2 MB array, which beats a vector DB on startup time at this scale. Three-layer escalation: regex catches prompt injection and fraud before any LLM call, a hard sensitivity ceiling escalates topics like fraud and account compromise even when the corpus has relevant docs, and a soft gate escalates when sensitivity is moderate and retrieval grounding is weak. Real test run: 29 tickets, $0.39 total cost, 41% escalation by design.

__[interactive-educator](https://github.com/Wamikmk/interactive-educator)__   Claude skill · React
A Claude skill that builds 3Blue1Brown-style interactive lessons on demand. Type `/aha gradient descent`, answer three quick questions about your background, and get a four-screen React artifact that teaches through guided discovery instead of lecture. The four screens are fixed in order: Puzzle (form a hypothesis by manipulating the visual), Explore (discover the pattern through Socratic questioning), Name (the formal definition arrives and every symbol maps back to something you already moved), Challenge (a new scenario where the visualization itself tells you whether you got it right). The structure is enforced because flexibility produced inconsistent artifacts; the "aha" must be stateable in one sentence before any code is written, or the scope gets rejected. No multiple-choice quizzes in the artifact: verification happens through the visualization itself. Shipped as a `.skill` file you upload to Claude in one click. Live demo from the system's output: [Gradient Descent](https://claude.ai/public/artifacts/9b3778bc-f30c-4537-9319-84e22c464685).

__[BDM Capstone: Customer Segmentation & Sales](https://github.com/Wamikmk/Bdm-Capstone_Project)__   pandas · scikit-learn · statsmodels
1,000 supermarket transactions across 3 branches, 17 variables. K-Means (Elbow + Silhouette) surfaced five distinct customer segments; time-series decomposition on daily sales surfaced weekday/weekend patterns invisible in the raw feed. Output: concrete recommendations on loyalty tiers, inventory reorder windows, and branch-specific payment behavior.

Stack

Python · pandas · NumPy · scikit-learn · statsmodels · Pydantic · Flask · FastAPI · SQLAlchemy · SQL · Claude API · React · Git · Bash
Learning: C, NLP

Currently

* Learning Natural Language Processing.
* Learning C, starting from a word-frequency counter and working up to a tiny memory allocator. The goal isn't another project; it's losing the fear of `malloc`.
* Extending Book of Artifacts with interactive explainers for concepts that textbook notation tends to butcher.

Writing

__[Project Playbook](https://github.com/Wamikmk/project-playbook)__   Methodology · 13 parts
A manual for building portfolio-grade projects with AI without falling into the copy-paste trap or the solo grind. Extracted from the Activation Engine build. Thesis: Claude teaches the reasoning, you write the code. Covers session rhythm, the five context anchors (CLAUDE.md, PROGRESS.md, git log, KNOWLEDGE.md, session rituals), and how to offload work to side chats without fragmenting the architecture.

__[Learning Playbook](https://github.com/Wamikmk/learning-playbook)__   Methodology · v1.0
A protocol for learning any subject from zero to fluency. Three load-bearing ideas: automaticity before understanding, mastery before advancement, confusion as diagnostic. Setup protocol, daily 30-minute engine, weekly feedback loop. Rule of thumb: use AI to sharpen questions, not to answer them.

Elsewhere

__[LinkedIn](https://www.linkedin.com/in/wamiq-mushtaq-079a07242/)__  
__[wamikmk@gmail.com](mailto:wamikmk@gmail.com)__
