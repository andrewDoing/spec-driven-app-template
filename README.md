# Fork of spec-driven-app-template
This is a template for using agent mode with MCP servers to do research driven development based on specs

See it in action here: https://www.youtube.com/live/Pv5DU1nwp6U?si=Zqt2LNjxGxU8MIpC&t=4806

## How To Use This

1. Make sure you're on vs-code 1.100.x or vs-code insiders latest
1. Make sure you're in Agent mode and you have GPT 4.1 selected (fastest for documentation)
1. Prompt the agent: `/new <explain your app idea>`
1. Go and edit the high level design or iterate with the agent and have it edit the plan to your liking. A simple react web app is a good choice.
1. Pass in this high level design as context, and prompt the agent `/plan`
1. Switch to Claude 3.7 sonnet (good in general, especially for UI, slower than 4.1) or Gemini 2.5 Pro (not as good at UI, otherwise solid)
1. Pass in the plan it generated as context, and have it go to work! Prompt something like `Start implementing`
1. When you run the code, you can pass it any errors and have it try to fix them.
1. Strategically pausing, stopping and creating a new chat with the agent to babysit it and make sure its doing what you want. A new chat is great to wipe out the context for a fresh issue like errors.

## My opinions on which models to use

**NOTE: These are my opinions, not objective truths. Experiment on your own and develop your own opinions. Expect that these will change over time. If a model is unlisted, I haven't used it yet.**

- **GPT-4.1**
  - Fastest option
  - Good for documentation and debugging
  - 1 million token context window
- **Claude 3.7 Sonnet**
  - A bit slower, writes good UI designs
  - Good general use for agent
  - 200k token context window
- **Gemini 2.5 Pro**
  - Also a bit slower, not as good at UI (probably would be better with better prompting)
  - Good general use for agent
  - 1 million token context window (2 million in the future)

## Contributing

Please open PRs to contribute prompts, instructions, and useful MCP servers.
