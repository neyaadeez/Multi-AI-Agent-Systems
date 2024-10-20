# Multi-Agent Content Creation with crewAI

This repository demonstrates the use of the **crewAI** framework to create a multi-agent system that researches, writes, and edits blog posts on various topics. The agents collaborate sequentially to produce high-quality content. The agents leverage OpenAI's `gpt-3.5-turbo` for language modeling, but other models like Hugging Face and Cohere can be integrated as well.

## Overview

In this project, three main agents work together:

1. **Planner Agent**: This agent plans the structure and key elements of the article.
2. **Writer Agent**: This agent writes the article based on the Planner's outline.
3. **Editor Agent**: This agent proofreads and ensures that the article aligns with editorial guidelines.

Each agent is assigned specific tasks to execute, and their collaboration results in a polished article.

## Features

- **Multi-agent collaboration**: Agents communicate and complete tasks in sequence.
- **Flexible LLM support**: Currently uses `gpt-3.5-turbo`, with support for other LLMs like Hugging Face, Mistral, and Cohere.
- **SEO optimization**: Articles are planned and written with SEO keywords in mind.
- **Customizable tasks**: Define roles and tasks for each agent, adjust the content generation process, and target specific topics.
