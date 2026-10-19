# AGENTS.md — Operating and publication rules

This is the **public, student-facing materials repository** for Advanced Statistics — Probabilistic Machine Learning (BGU 367-2-5561, 2027-1, instructor Opher Donchin).

- Student repository: `opherdonchin/AdvancedStatisticsCourse_36725561`
- Development repository: `opherdonchin/ProbabilisticMachineLearning`

This repository is a **publication destination, not a source of teaching content**. Materials are authored and reviewed in the development repository, and not everything there is safe to publish.

## Publication rules

- Publish only explicitly approved student-facing materials.
- Never publish solved InClass notebooks, answer keys, grading rubrics, grading scripts, assessment API credentials, instructor-only documents, unpublished drafts, or identifiable student records.
- Do not copy the development repository's directory tree wholesale; transfer only a curated set of files.
- Preserve links and filenames when publishing updated materials, so Colab links keep working.
- Do not claim that notebooks or other materials are available or validated until they actually are.
- Do not create placeholder lecture material or empty directory hierarchies in anticipation of future content.
- Future automated publication (curated transfer from the development repository, with checks and instructor approval) is to be designed separately. Do not build it without being asked.

## Git workflow

- Work directly on `main` for authorized changes.
- Never create branches or pull requests without the instructor's explicit, task-specific permission.
- Do not force-push, rewrite history, or replace repository contents wholesale.
- Do not install automation (e.g. GitHub Actions), change repository settings, or add secrets without asking first.

## Student-facing facts

- Students generally run notebooks in Google Colab; local execution is possible where supported.
- Completed InClass notebooks are submitted through Moodle by Wednesday 23:59 Israel time, not through GitHub.

## Other agent instructions

This file is the single source of rules. Tools that read other instruction files should follow this one; do not maintain duplicate copies that could conflict.
