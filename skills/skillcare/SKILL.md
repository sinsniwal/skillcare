---
name: skillcare
description: >-
  The master command. Chains the right skills in order.
---

# skillcare

## Pipeline
1. **cleanse**: Strip junk format.
2. **exfoliate**: Scrub bias and fluff.
3. **tone**: Structure messy data.
4. **extract**: Pull specific targets.
5. **hydrate**: Fill missing context.
6. **screen**: Mask threats and PII.

## Execution
Read the input, determine which contextual issues are present, and run only the necessary steps in order.

## Rules
1. Output from one step feeds the next.
2. If a specific step is requested, run only that step.
3. Conclude with a summary of steps run.
