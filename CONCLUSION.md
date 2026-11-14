# Lab 05 — Conclusion


## 1. Which layer changed your results the most?

Give the numbers before -> after for that layer (correct / wrong / no answer, out of 20) and say
whether it changed what the agent *can do* or only what it *admits*. If no layer changed the
number of correct answers, say so and explain what the layers did change instead.

I think that layer 1 changed the results the most.Before layer 1 the AI had 16 correct answers and 4 wrong answers and 4 no answers.After layer 1 it had 18 correct answers,6 wrong answers and 0 no answers.
layer 1 helped the AI when there was a tool error.Before this layer the AI stopped after an error.With layer 1 the AI could try again.
layer 2 do not change the results.
Layer 3 helped the AI give fewer wrong answers.Wrong answers went from 6 to 4.
I think that layer 1 helped the AI answer more questions.Layer 3 helped the AI stop when it could not give a good answer.

## 2. One failure the full harness did not fix

Pick one question that the full harness (layer 3) still gets wrong or refuses. Give its id
(q01 ... q20). Open its trace in the notebook: at which step did it go wrong, and what did
the model do instead? Name one thing you would add to the harness, and what it would cost
(extra model calls, tokens, time, or a new way to fail).

One problem was in question q18.The AI needed to calculate the number.First it used the get_series tool to get data.So it used the calculate tool.The calculate tool give the number 0.055.But the AI wrote 0.55 in its answer.This is a wrong.Layer 3 found this problem.It asked the AI to check the answer again.But the AI do the same mistake.At the end the AI gave unferified.It means the answer was not checked.I think that we need one more tool to check the math and the units. This can help the AI make fewer mistakes.But it can also take more time.

## 3. Workflow or agent for the monthly ranking?

Dala Insight wants to publish, every month, "which region is highest and which is lowest on one
indicator in one year". Would you ship the fixed workflow or the agent? Use the accuracy, the
number of model calls, the tokens and the time you measured in Part 1. Then say in one sentence
what kind of question would make you choose the other one.

I would choose Workflow for the monthly reports.In our test Workflow gave 13 correct answers out of 15.The AI agent gave only 9 correct answers out of 15.Workflow used 3,852 tokens. The agent used 19,835 tokens.Workflow was also faster. It took 17.7 seconds.The agent took 50.9 seconds.I think workflow is better for this job.The company does the same work every month. We know what steps we need to do.Workflow follows these steps. It is simple, fast and uses fewer tokens.But for difficult questions I would use an AI agent.This agent can choose different tools and do different tasks.


