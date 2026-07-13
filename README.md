# Context Bombs

<img width="640" height="640" alt="context_bomb" src="https://github.com/user-attachments/assets/be7fb001-549a-47ba-8aba-4472187b983e" />


### Strings that can stop AI attackers by tripping their safety guardrails.
When used as the content of canary resources in your environment, context bombs can both detect (raising an alert) and stop an offensive AI agent.  
Effectiveness of those strings can vary by model provider: dangerous biological content stops the leading Western models, while politically sensitive content stops Chinese models served by Chinese providers.

### How we tested context bombs
Strings in this repo have been tested against five frontier models performing a red team engagement in a realistic AWS environment.  
Deploying a single context bomb inside the environment (as an AWS secret) had a huge impact on stopping offensive AI agents. For instance, admin privilege escalation went from 57% of runs to 5%.  

Models tested:
| Model           | Provider  |
|-----------------|-----------|
| Claude Opus 4.8 | Anthropic |
| Gemini 3.1 Pro  | Google    |
| GLM 5.2         | GMI Cloud |
| DeepSeek 4 Pro  | DeepSeek  |
| Kimi K2.6       | Novita AI |

**Full research:** [https://agentic.tracebit.com/context-bombs](https://agentic.tracebit.com/context-bombs)
