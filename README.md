# Homemade Regex Engine

A pure regular expression engine built from scratch in Java.

## What is this?

This project is a minimal, educational, and functional implementation of a regex engine. It focuses strictly on **regular** regex features — the kind that can be implemented with finite automata. No backtracking, no lookaheads, no backreferences — just clean, true regular expressions.

## Why?

I’m building this to:
- Understand how regular expressions work under the hood. Practicing theoretical computer science (TCS) course in university.
- Learn and implement the full process: tokenization, parsing, NFA construction, and simulation
- Create a lightweight, dependency-free regex library in Java

## Features (Planned)

- Basic pattern compilation
- Regex tokenizer
- AST-based parser
- NFA builder from AST
- NFA simulator
- Core features:
  - Character matching (`a`, `b`, etc.)
  - Alternation (`|`)
  - Quantifiers (`*`, `+`, `?`, `{n,m}`)
  - Grouping with parentheses (`(...)`)
  - Character classes (`[a-z]`, `[^abc]`)

## Not Supported (By Design)

This engine intentionally does **not** support:
- Backreferences (e.g. `(a)\1`)
- Lookaheads / lookbehinds
- Recursive or context-sensitive features

These go beyond the capabilities of finite automata and are not part of regular languages. Build-in java package for Regex supports them, but it is regex++, rather than classic pure regular expressions (requiring memory, etc).

## Package Structure

I mimic original java package structure for better UX.

- `Regex.java`: Static entry point for quick matching
- `Pattern.java`: Compiled representation of a regex pattern
- `Matcher.java`: Applies a pattern to an input string
- `internal/`: Tokenizer, parser, NFA components (not exposed to users)
- `exceptions/`: Custom exceptions for syntax errors, etc.

## Example (Coming Soon)

```java  
Pattern pattern = Pattern.compile("a*b");  
Matcher matcher = pattern.matcher("aaab");  
boolean result = matcher.matches(); // true  
```  
# Homemade Regex Engine

A pure regular expression engine built from scratch in Java.

## What is this?

This project is a minimal, educational, and functional implementation of a regex engine. It focuses strictly on **regular** regex features — the kind that can be implemented with finite automata. No backtracking, no lookaheads, no backreferences — just clean, true regular expressions.

## Why?

I’m building this to:
- Understand how regular expressions work under the hood. Practicing theoretical computer science (TCS) course in university.
- Learn and implement the full process: tokenization, parsing, NFA construction, and simulation
- Create a lightweight, dependency-free regex library in Java

## Features (Planned)

- Basic pattern compilation
- Regex tokenizer
- AST-based parser
- NFA builder from AST
- NFA simulator
- Core features:
  - Character matching (`a`, `b`, etc.)
  - Alternation (`|`)
  - Quantifiers (`*`, `+`, `?`, `{n,m}`)
  - Grouping with parentheses (`(...)`)
  - Character classes (`[a-z]`, `[^abc]`)

## Not Supported (By Design)

This engine intentionally does **not** support:
- Backreferences (e.g. `(a)\1`)
- Lookaheads / lookbehinds
- Recursive or context-sensitive features

These go beyond the capabilities of finite automata and are not part of regular languages. Build-in java package for Regex supports them, but it is regex++, rather than classic pure regular expressions (requiring memory, etc).

## Package Structure

I mimic original java package structure for better UX.

- `Regex.java`: Static entry point for quick matching
- `Pattern.java`: Compiled representation of a regex pattern
- `Matcher.java`: Applies a pattern to an input string
- `internal/`: Tokenizer, parser, NFA components (not exposed to users)
- `exceptions/`: Custom exceptions for syntax errors, etc.

## Example (Coming Soon)

```java  
Pattern pattern = Pattern.compile("a*b");  
Matcher matcher = pattern.matcher("aaab");  
boolean result = matcher.matches(); // true  
```  
