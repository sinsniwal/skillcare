---
name: extract
description: >-
  Pulls out exact targets like metrics, code, and entities.
---

# extract

## Target
Specific high-value data requested by the user or implied by the context (e.g., code blocks, financial metrics, named entities, endpoints).

## Goal
An isolated collection of the requested data types, discarding all surrounding prose and context.

## Rules
1. Extract verbatim. Do not summarize or paraphrase.
2. Group and structure the extracted data logically.
3. State clearly if the requested data type is not found in the text.
