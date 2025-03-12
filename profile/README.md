# nano-R1
Crowdsourcing the recipe search for compute-optimal LLM RL with verifiable rewards.

**\<think\>**

Okay, so we want to figure out the best way to train LLMs to do RL with verifiable rewards.

I remember from the DeepSeek R1 [paper](https://arxiv.org/abs/2501.12948) that GRPO with correctness and format rewards can learn to solve math and code problems. 

But, I don't think they've reported hyperparameter ablations for GRPO beyond the values used in the earlier DeepSeekMath [paper](https://arxiv.org/abs/2402.03300). It's also not clear how much this extends to problems beyond math and code, particularly with smaller models.

Hmm, so there's a number of LLM RL training libraries which might be useful here, each with their own different implementation choices:
- [axolotl](https://github.com/axolotl-ai-cloud/axolotl)
- [oat](https://github.com/sail-sg/oat/tree/main)
- [open-instruct](https://github.com/allenai/open-instruct)
- [OpenRLHF](https://github.com/OpenRLHF/OpenRLHF)
- [OpenPipe deductive-reasoning](https://github.com/OpenPipe/deductive-reasoning)
- [TRL](https://github.com/huggingface/trl/tree/main/trl)
- [TinyZero](https://github.com/Jiayi-Pan/TinyZero/tree/main)
- [Unsloth](https://github.com/unslothai/unsloth)
- [verifiers](https://github.com/willccbb/verifiers)
- [veRL](https://github.com/volcengine/verl)

There's also some benchmarks that are commonly studied in practice, but there isn't really an agreed-upon gold standard set:
- Math (MATH, AIME, FrontierMath)
- Coding (HumanEval, IOI, CodeForces)
- Logic puzzles (Alice in Wonderland, Sudoku, Temporal Clue)
- Hard knowledge tasks (MMLU-Pro, GPQA, HLE)

Wait, but there's also a lot of open training datasets for reasoning problems that might be useful, from teams like:
- [General Reasoning](https://gr.inc/)
- [HuggingFace Open-R1](https://huggingface.co/open-r1)
- [OpenThoughts](https://www.open-thoughts.ai/)
- [Prime Intellect](https://www.primeintellect.ai/blog/synthetic-1)

Additionally, I remember reading a number of [papers](https://arxiv.org/abs/2005.12729) and [blogs](https://iclr-blog-track.github.io/2022/03/25/ppo-implementation-details/) talking about how RL algorithms like PPO can be very sensitive to implementation details. This seems especially important figure out for LLMs, given how expensive and time-consuming they are to train.

I also remember that the [nanoGPT](https://github.com/karpathy/nanoGPT) project from Andrej Karpathy spawned a productive search for pretraining methods, and yielded a number of notable performance breakthroughs like Muon, documented in Keller Jordan's [modded-nanogpt](https://github.com/KellerJordan/modded-nanogpt).

What if we had a similar kind of competitive-collaborative leaderboard for RL and reasoning?

\[To be continued...\]

**\</think\>**
