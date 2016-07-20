Simulating Collaborative Agents
===============================

Simulating <=> Imitating the functioning of the real-world
Collaborative <=> Working together to achieve goals
Agents <=> Models of self-interested behaviour

---
Solving problems *without* cooperation

* Human expert defines the goals
* Centralized planner construts a plan (sequence of action to achieve goals)
* Each action in the plan is assigned to some hardware component (effectuator)

---
The Real-World is a Mess

* Centralized plan can become invalid if the environment changes
* There is imperfect and limited knowledge (partial observation) of the world
* Hardware components can fail and make the plan impossible to finish

---
The Real-World "Agent" Societies

* Living creatures
* Human tribes and societies
* Adaptable to the messiness of the real-world

---
Self-Interest

Living creatures (and simulated agents) maximize their own self-interest (maximize the utility function).

Utility Function Ω => u, where:

Ω = {w1, w2....wn} is the set of world states
u ∈ R is the utility value (real number value)

The agent will prefer world state w1, if u(w1) >= u(w2)

---
Joint utility

When the plan is executed by several agents, the next state of the world is determined by the joint action of all agents.

τ(Ai,Aj,Ak...) => Ω => utility

Therefore, if agent Ai wants to control the utility function Ω => u,
it must cooperate with the other agents.

---
Loosely-coupled Agents

Most of the time the agents follow their own goal, and in rare occasions
there are some interaction => The agents are loosely coupled.

* Wrongly assume that the agents are independent
* The plan will fail
* Fix the plan, by manually introducing constraints on the joint actions

Example:

Action: doOpen(Ai,door)
Condition: ¬ perceiveOpen(door), ¬ doOpen(Aj,door), i!=j
Effect: perceiveOpen(door)

This manual "fix" becomes difficult if there are many interactions.
It is also not flexible because all possible interaction must be described manually.

---
Cooperating Agents

If the system is "Multi-Agent" each agent has is own goals
and its own plan.

Each agent will choose a plan p ∈ P, where P is the set of all plans.
p1, p2... pn must be compatible with each other.

Solutions:
* Social convention (Drive on the left side) and social law
* Communicate ownership of sub-tasks
* Start executing a plan, and force other agents to choose compatible plans

---
Game Theory (plus Nash Equilibrium)

How can I get the most utility?
What is the best strategy?

∀v ∈ Ω1, ∀w ∈ Ω2  =>  u(v) > u(w), where:
Ω1: the set of outcome from playing Strategy1
Ω2: the set of outcomes from playing Strategy2
=> Strategy1 is the dominant

What is the best strategy for everyone?
Maximizing the sum total of agent happiness.

Agent i plays Strategy1
=> Agent j can do no better than Strategy2
=> Agent i can do no better than Strategy1
=> Strategy1 and Strategy2 are in "Nash Equilibrium"

---
Negotiating Things

* Nash equilibrium makes every agent happy
* If equilibrium doesn't emerge automatically, the agents they must negotiate
* Negotiation means each side makes a "concession" (give up some utility)
* Negotiation is mutually beneficial (maximising the sum total)

Negotiate task allocation => Use an "auction" model, where highest bidder gets the resource.

Exchange tasks => Imagine you have 3 children, and your neighboughr has 4. They need delivering to common location (School), at different times (Different time slots). You can exchange the tasks (the children), to bundle them by delivery time.

---
Delegating Things

* A classical plan is a sequence of actions
* Replace the simple actions with High-Level Actions (HLA)
* Task are assigned to each Agent
* Details of execution plan can be delegted to the Agent
* When the agent reaches the HLA it plans its own implementation

HLA => many refinements
HLA => the plan contains "angelic" non-determinism

---
Sub-Contractig Things

* Agent listens for announcements of "contracts" and evaluates its own hardware
* When the task is suitable it make a bid for the task
* The "manager" awards a "contract" to the highest bidder
* In the future the manager depends on the sub-contractor for that task

---
Summary
