---
name: python-echo-cli
description: "Text analysis CLI — word frequency, sentence split, character stats, Levenshtein distance, palindrome check"
version: "1.0.0"
author: "yz06276"
tags:
  - python
  - text-analysis
  - nlp
---

# python-echo-cli

## Overview

This skill provides a text analysis CLI built in Python. It can analyze word frequency, split sentences, show character statistics, compute Levenshtein distance between strings, and check for palindromes.

## Pre-flight Checks

Before using this skill, ensure:

1. The `python-echo-cli` package is installed (via `pip install python-echo-cli` or `plugin-store install python-echo-cli`)

## Commands

### Echo text (plain)

```bash
python-echo-cli "Hello World"
```

**When to use**: When the user wants to simply echo text back.

### Word Frequency

```bash
python-echo-cli --mode freq "the cat sat on the mat the cat"
```

**When to use**: When the user wants to count word occurrences in text.
**Output**: Word frequency table sorted by count.

### Sentence Split

```bash
python-echo-cli --mode sentences "Hello world. How are you? I am fine."
```

**When to use**: When the user wants to split text into individual sentences.
**Output**: Numbered list of sentences.

### Character Stats

```bash
python-echo-cli --mode chars "Hello World 123!"
```

**When to use**: When the user wants character-level statistics (letters, digits, spaces, punctuation).
**Output**: Character count breakdown by type.

### Levenshtein Distance

```bash
python-echo-cli --mode distance "kitten" --compare "sitting"
```

**When to use**: When the user wants to measure edit distance between two strings.
**Output**: Integer edit distance.

### Palindrome Check

```bash
python-echo-cli --mode palindrome "racecar"
```

**When to use**: When the user wants to check if text is a palindrome.
**Output**: `true` or `false`.

## Error Handling

| Error | Cause | Resolution |
|-------|-------|------------|
| "Unknown mode" | Invalid --mode value | Use one of: freq, sentences, chars, distance, palindrome |
| "No input provided" | Missing text argument | Provide text as a positional argument |
| "--compare required" | Missing second string for distance mode | Provide --compare argument |
