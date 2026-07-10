---
name: hello-world
description: A minimal example skill that greets the world. Demonstrates canonical SKILL.md frontmatter.
tags:
  - example
  - demo
group: example
version: 0.1.0
platforms:
  - any
---

# Hello World

This is the canonical example skill for the senselight/skills monorepo.

## Purpose

Prove that the SKILL.md schema and monorepo layout accept a minimal skill.

## Usage

Install:

`skillctl install hello-world --platform claude --scope project`

## Contract

- Frontmatter validates against `@senselight/skill-schema` v1
- No side effects, no external dependencies
