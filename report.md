# OrderBot Report

## Objective

To experiment with prompt engineering by adapting the OrderBot exercise to a real-world food delivery scenario using my custom menu. The goal was to:

* Build 3 creative dialogue versions
* Generate structured JSON summaries from user inputs

## Versions

### Version 1: Basic Order

* **Order**: Jollof Rice + Chicken + Fried Plantains
* **Output**: JSON summary
* **Issue**: GPT initially guessed prices (10 EUR for rice), but was corrected with clearer system prompts.
* **Fix**: Prompt was rewritten to say "ONLY use prices from the menu. DO NOT guess."

### Version 2: Pickup Order with Add-On

* **Order**: Medium Box + Pepper Sauce (pickup)
* **Output**: GPT kept hallucinating lower prices (e.g. 10 EUR instead of 14 EUR for Medium Box)
* **Fix**: System prompt rewritten multiple times with stricter constraints; still struggled.
* **Conclusion**: This version showed how GPT may default to prior assumptions if instructions aren't explicit or reinforced.

### Version 3: Complex Order

* **Order**: 2 Coconut Rice + Chicken, 1 Medium Box, 2 Pepper Sauces, delivery
* **Output**: JSON summary
* **Result**: Correct prices used, total computed accurately (12.5 + 12.5 + 14 + 1.5 + 1.5 = 54 EUR)
* **Success**: This succeeded because I followed a clearly defined and tested prompt format, which helped guide GPT's response more reliably.


## What I Learned

* Prompt clarity is EVERYTHING. The more specific you are, the better the outcome.
* GPT tends to hallucinate or invent prices unless explicitly told not to.
* Using examples or structure similar to what works helps reduce error drastically
* Iteration is part of the process. Several prompts failed before a good one worked.

## Final Notes

For future projects, I will:

* Include strict rules in system prompts
* Add sample menu data clearly inside the prompt
* Use markdown to document iterations and findings in my repos
