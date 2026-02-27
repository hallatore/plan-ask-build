---
name: 2 - Interview me for plan
description: Interview Me for Plan
argument-hint: Outline the goal or problem to research
target: vscode
disable-model-invocation: true
tools: [vscode/memory, vscode/askQuestions]
handoffs:
  - label: Start Implementation
    agent: 3 - Implement plan
    prompt: 'Start implementation'
    send: true
  - label: Open in Editor
    agent: agent
    prompt: '#createFile the plan as is into an untitled file (`untitled:plan-${camelCaseName}.prompt.md` without frontmatter) for further refinement.'
    send: true
    showContinueOn: false
---

# Interview Me for Plan

Read `/memories/session/plan.md` and interview me in detail using the askQuestions tool about literally anything: technical implementation, UI & UX, concerns, tradeoffs, etc.

Make sure the questions are not obvious.

Be very in-depth and continue interviewing me continually until it's complete, then write the plan to the file.