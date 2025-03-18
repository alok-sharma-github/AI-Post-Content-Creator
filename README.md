# Agentic Search Tool - Instagram Post Generator

This repository contains a Python-based tool for generating and refining Instagram posts using AI. The tool leverages advanced language models and a structured workflow to create engaging, high-quality content tailored for Instagram. It includes features for planning, drafting, critiquing, and revising posts, as well as generating visual suggestions for images.

## Key Features

- **AI-Powered Post Generation**: Utilizes language models to create comprehensive outlines, drafts, and critiques for Instagram posts.
- **Structured Workflow**: Implements a stateful graph-based workflow to manage the post creation process, including planning, research, drafting, and revision.
- **Visual Suggestions**: Integrates with AI image generation models to provide visual prompts and suggestions for Instagram posts.
- **Gradio Interface**: Includes a user-friendly Gradio interface for easy interaction with the tool, allowing users to input topics, set revision limits, and view outputs.
- **Research Integration**: Uses the Tavily API to gather relevant information for post creation and refinement.

## Workflow Overview

1. **Planning**: Generates a detailed outline for the Instagram post, including core messages, visuals, hashtags, and call-to-actions.
2. **Research**: Conducts research using the Tavily API to gather relevant data for the post.
3. **Drafting**: Creates a draft of the Instagram post based on the outline and research.
4. **Critique**: Provides constructive feedback on the draft, focusing on engagement, clarity, visual appeal, and tone.
5. **Revision**: Iteratively refines the post based on feedback and additional research.
6. **Visual Generation**: Generates AI-based visual prompts for the post using image generation models.



## Code Structure

- **State Graph**: Manages the workflow using `StateGraph` and `SqliteSaver` for state persistence.
- **Prompt Engineering**: Defines prompts for planning, drafting, critiquing, and research.
- **Image Generation**: Integrates with AI image generation models to create visual suggestions.
- **Gradio Interface**: Provides a user-friendly interface for interacting with the tool.

## Requirements

- Python 3.8+
- Libraries: `langgraph`, `langchain`, `tavily`, `gradio`, `PIL`, `requests`, `base64`, `io`

## Example

```python
# Example usage of the workflow
states = run_workflow("How to Grow Your Personal Brand on LinkedIn", max_revisions=2)
plan, draft, critique = display_results(states)
print("Plan:", plan)
print("Draft:", draft)
print("Critique:", critique)
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## Reference DeeplLearning.ai course
