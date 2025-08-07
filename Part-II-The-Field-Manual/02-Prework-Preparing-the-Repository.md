## 7.1 Prework: Preparing the Repository

The Prework Phase is about crafting a set of guardrails unique to your
codebase. This grounds prompt-driven generation in your team’s unique
architecture and standards — key for avoiding hallucinations and
ensuring the AI acts within meaningful guardrails.

To begin, create a folder at the root level of your Git repository:
`.development-context/research`.

Now, create a file within that folder called
`01-architectural-research-prompt.md`. This file will contain the
instructions for your AI agent to analyze your repository and generate
an architectural research document.

```
# Licensed under the MIT License
Create a document 02-architectural-research.md
 which details the tools, frameworks and design
 patterns used across the repository.
Pay particular attention to highlight any
 standards and practices that appear to deviate
 from those that one would expect to find given
 the recommended advice of the language and
 framework.
The description should include but not be
 limited to highlighting data models, api
 design & versioning, as well as any other
 insights that seem relevant within the
 current state of the repository.
(for legacy systems)
When more than one or conflicting architecture
 or pattern is being used, call this out in the
 document and provide recommendations on the
 best direction forward. Use references to
 external sources which can qualify known best
 practices from software experts.
When it is clear when there is an old or a new
 way of doing things, call out which one is the
 newer pattern.
```

Next, inside your agent, use this prompt to execute the instructions
you’ve just created:

```
# Licensed under the MIT License
Execute the instructions found within
 @01-architectural-research-prompt.md
```

Now, carefully read the artifact that was produced
(`02-architectural-research.md`). Does it seem accurate? Are there things
you think you should correct? Some inaccuracies (‘hallucinations’) are
expected in early iterations and can be corrected through iterative
prompt refinement. For simple errors, feel free to edit them manually.

For things that appear to be more systemic or outright mind-blowingly
wrong, don’t panic.Go back and edit the
`01-architectural-research-prompt.md` to include additional context or
directives it shouldn’t forget. Focus on capturing the most significant
errors for targeted prompt improvements rather than exhaustive
corrections. We’re building these systems for the long haul and expect
to to be iteratively improving them for years to come. It is a mistake
at this point to sacrifice velocity in favor of perfection. Simple
errors can and should be manually corrected, keeping the focus on
meaningful prompt refinement over exhaustive fixes.

You’re going to keep both of these documents
(`01-architectural-research-prompt.md` and `02-architectural-research.md`)
and check them into your repository. They form the foundation of your
architectural context.

We’re not quite ready to get rolling on an actual project yet. Your
next step is to execute another agentic command to codify these
insights into reusable rules:

```
# Licensed under the MIT License
Read @02-architectural-research.md and create
 a series of cursor rules using their
 documentation
 https://docs.cursor.com/en/context/rules#rules
Save each in a separate file in the folder
 .development-context/rules and include a
 readme.md document which describes each
 rule and explains when it is appropriate
 to use them.
For example, planning a task without data
 migrations would not need to include any
 database rules. But if it were modifying
 an endpoint it might be appropriate to
 include api design rules.
```

Review those rules carefully and check them into your repository after
you agree with all of them. Now, you’re ready to proceed to the
Planning phase.
