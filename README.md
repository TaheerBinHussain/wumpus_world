Dynamic Wumpus Logic Agent

A web-based Dynamic Pathfinding Agent that navigates a Wumpus World-style grid using a formal Propositional Logic Knowledge Base (KB) and a Resolution Refutation engine. 

🚀 Live Demo
https://project-phfjt.vercel.app/

🧠 Core Features
Dynamic Grid & Hazards: Fully customizable grid dimensions (NxN) with randomized Pit, Wumpus, and Gold placements at the start of every episode.

Knowledge-Based Inference:The agent receives dynamic percepts (Breeze, Stench, Glitter) and automatically translates them into Conjunctive Normal Form (CNF) clauses.
Resolution Refutation Engine: Before moving, the agent queries its KB using automated resolution refutation (e.g., proving `¬P_2_2 ∧ ¬W_2_2` by asserting the negated goal and finding a contradiction).
Real-Time Metrics: Tracks inference steps, KB clause count, cells visited, and overall score via a custom UI dashboard.

🛠️ Technical Stack
Frontend: Vanilla JavaScript, HTML5, CSS3 (Custom Light Theme)
Deployment: Vercel

⚙️ How the Logic Engine Works
Instead of hardcoded heuristic rules, this agent uses formal propositional logic. 
1.  TELL: When a percept is received, the environment rules are converted into CNF and pushed to the KB array.
2.  ASK: To evaluate if an adjacent cell is safe, the engine negates the safety query, temporarily adds it to the KB, and loops through clause pairs resolving complementary literals until an empty clause `[]` (contradiction) is found.

👨‍💻 Local Setup
1. Clone the repository: `git clone [Your Repo URL]`
2. Open `index.html` in any modern web browser. No external dependencies or build steps required.
