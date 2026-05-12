---
layout: page
title: "Resume Builder"
permalink: /projects/resume-builder/
---

<div class="project-meta">
  <strong>Role:</strong> Developer &nbsp;·&nbsp;
  <strong>Timeline:</strong> January 2026 – May 2026 &nbsp;·&nbsp;
  <strong>Type:</strong> User Design Project — University of Maine
</div>

## Overview

Our team was initially provided a project proposal requesting a product design of a tool to assist SCIS students with building portfolios. After conducting the interviews, we found that hiring managers didn’t encounter or value portfolios enough for a portfolio builder to benefit SCIS students, and we pivoted our tool to a resume builder tool instead.

## Design Process

The design process was split into four milestones.For Milestone 1, we constructed research questions to guide our project design, then we conducted interviews with SCIS students and hiring managers, coded the transcripts, and derived themes to determine the scope and implementation plan for the project.

Over the course of Milestone 2 we created user personas, key scenarios, and drafted low-fi wireframes. During Milestone 3, our team created a hi-fi prototype, received a heuristic analysis of our prototype from a peer review team, conducted usability testing with students, and created a coded prototype based off of evaluated product issues. Future implementation will need to connect an API tool to a generative AI. In its current state, our current project is beta quality client side prototype with user flows complete and generative AI use mocked.

Milestone 4 consisted of a client handoff package along with a 30 "teaser" video and an 8 minute presentation of the process and a walkthrough.

## Key Features

- Inline editing: Click any field on the Review screen to edit. Add/remove experience, education, projects, skills, and bullets.
- Enrichment triage:  Add sources (GitHub, PDF/doc upload, free-text descriptions), then assign extracted bullets to specific resume entries.
- Prompt-based bullet refinement: Type what you want ("make it shorter", "add metrics") or click suggestion chips. Compare refined vs original with revert.
- Job tailoring:  Each match shows a proposed bullet with rationale. Apply directly, edit first, skip, or undo. Changes are real:  they modify the actual resume.
- Animated transitions:  Page transitions (AnimatePresence), parsing spinner-to-check animation, smooth progress bar, stepper with spring physics.
- State persistence:  All state saves to localStorage. Refresh and pick up where you left off. "Start over" resets everything.

## Technologies Used

- Figma - Design
- Claude Code - Initial coded prototype
- iMovie - Editing the teaser video

## Gallery

<div class="project-gallery">
  <!-- ![Resume builder interface](/assets/images/resume-builder/mockup.png) -->
</div>

## Links

<div class="project-links">
  <a href="https://github.com/grelmu/resume-builder" target="_blank">GitHub Repo</a>
  <a href="https://www.youtube.com/watch?v=CwDJD7g_Iqc&list=PLkl3Uttdpu_jw0_pCa9NtBtnI1fgV5RNg&index=6" target="_blank">Final Presentation</a>
  <a href="https://resumebuilder.ethanmor.in/" target="_blank">Coded Prototype</a>
</div>