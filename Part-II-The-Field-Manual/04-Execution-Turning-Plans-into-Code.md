## 7.3 Execution: Turning Plans into Code

Begin with the prompt, sent directly to your agent:
```
# Licensed under the MIT License
Execute Track 1 PR 1 in
 @/{tickt-id}/02-initial-plan.md
```

Your coding session operates as a repeatable cycle:
1.  **Generate:** Run the agent to produce code for the current PR scope.
2.  **Review:** Carefully read the generated code; validate correctness, style, and merge safety.
3.  **Correct:** Fix errors, add missing pieces, or tweak for clarity — either by:
    *   Making quick manual edits for trivial fixes, or
    *   Noting recurring or major gaps that merit a prompt update.
4.  **Decide:** If manual fixes become frequent or fundamental, update your prompt artifact to improve future output.
5.  **Stage & Commit:** Stage your changes to create a stable baseline before committing.
6.  **Open PR:** Submit pull requests incrementally for peer or lead review, emphasizing small, safe, and well-justified increments.
7.  **Repeat:** Move through each plan segment and pull request until the full track is complete.

**Tips for success:**
*   **Trust but verify:** Use your human judgment to balance prompt iteration with tactical manual edits.
*   **Play to your team’s culture:** Leverage feature flags and trunk-based development to safely integrate new code in production.
*   **Keep artifacts up-to-date:** Prompt updates are a force multiplier — invest time refining when it boosts productivity and safety.
*   **Iterate efficiently:** Don’t aim for perfect first attempts. Use the “three reads” mindset you practiced in Planning to guide code review and prompt tuning.
*   **Communicate:** Keep your team looped in by regularly pushing your prompt and code artifacts, enabling shared ownership and gradual improvement.

Why detail matters here: Execution may feel “just coding,” but in
practice it’s where your prompt engineering meets software
craftsmanship. You orchestrate LLM outputs, developer expertise, and
continuous feedback — all while maintaining velocity and quality in
complex enterprise systems.
