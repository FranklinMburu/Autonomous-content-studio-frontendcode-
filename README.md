# Candela Studio

Candela is an autonomous studio that turns true stories into short films. Researched, checked and painted on free tiers.

This application is built with **React 19 + TypeScript + Vite**, using Phosphor icons and pure CSS design tokens with a 2D Canvas Earth and Studio World rendering engine.

## Overview

- **Landing Experience (`/`)**:
  - **Section 1: Hero Globe**: Canvas 2D dotted Earth showing real continent projections, real story locations, and a scroll-driven sunrise transition.
  - **Section 2: Inside the Studio**: An interactive, live embedded browser panel displaying the real read-only studio workspace.
  - **Section 3: One Studio, Five Parts**: Product family overview (Studio, Brain, Lab, Guard, Channels) connected with animated vector flow lines.
  - **Section 4: How a Film is Made**: 5-step storyboard lifecycle from Topic and Script to 30 painted shots (with face locking and vision picture checks), Motion & Music, and Human Review.
  - **Section 5: The Studio World**: A 2D rotating sphere displaying real production steps and live weekly metrics with zero fake data.
  - **Section 6: Films & Trust**: Finished films gallery, production guardrails, and final call to action.

- **Studio App (`/app/*`)**:
  - **Films (`/app/films`)**: Film workspace with 4 stat tiles, 7-day activity bar chart, filter tabs, "Making now" live run steps, and coming schedule.
  - **Film Detail (`/app/films/:id`)**: 9:16 vertical video player, verified claims citation list, script beats, cast, and GitHub actions.
  - **Runs (`/app/runs`)**: GitHub Actions execution timeline, segmented step status bars, and scheduled daily slots.
  - **Review (`/app/review`)**: Gatekeeper queue for films held for inspection with weak shot comparisons, approve and repaint actions, and Claude polish prompts.
  - **Polish (`/app/polish`)**: Guided 4-step workflow to polish narration drafts using Claude.
  - **Upload (`/app/upload`)**: Ready-to-upload queue with 1-click links to YouTube Studio.
  - **Studio Channels (`/app/channels`)**: Channel management for Hidden Reasons and Explainer pipelines.
  - **Topics (`/app/topics`)**: Editorial story queue with geolocation coordinates and historical years.
  - **Schedule (`/app/schedule`)**: 3-day × 5-slot daily schedule planner converted to local user timezone.
  - **Memory (`/app/memory`)**: Cast, historical places, and soundtrack themes logged to prevent repetition.
  - **Brain (`/app/brain`)**: Multi-model script arbitration across free LLM tiers.
  - **Lab (`/app/lab`)**: Kaggle T4 dual-GPU painting specifications and experiment releases.
  - **Guard (`/app/guard`)**: Fact check, picture check, and review gate health status with pipeline alerts.
  - **Planned Features (`/app/analytics`, `/app/trends`, etc.)**: High-fidelity roadmap specifications.
  - **Settings (`/app/settings`)**: Theme switcher (Dark ink / Light / System), cache clear, and repository settings.

## Data Layer

The application operates in **read-only mode** with no seed or mock data:
- Reads real releases, issues, and Actions runs via GitHub REST APIs with `sessionStorage` caching.
- Reads raw episode files and topic queues directly from GitHub raw content endpoints.
- All mutating actions direct the user to the corresponding GitHub issue or Actions workflow.

## Development

```bash
npm install
npm run dev
```

Build for production:

```bash
npm run build
```
