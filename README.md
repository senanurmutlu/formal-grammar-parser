# formal-grammar-parser
# Formal Grammar & Automata Parser Engine

A robust, dual-mode Python syntax analyzer and parser engine developed to process formal grammars, context-free grammars (CFGs), natural language syntax structures, and epsilon ($\varepsilon$) transitions with precise error reporting and AST generation.

## Overview
This project bridges theoretical computer science (Formal Languages and Automata Theory) with practical software implementation. It evaluates grammar rules dynamically, tokenizes input strings (both word-level natural language sentences and character-level formal strings), and builds Abstract Syntax Trees (ASTs) while providing granular, index-based syntax error reporting.

---

## Key Features & Architecture

### 1. Dual-Mode Detection (`detect_mode`)
- **Natural Language Mode (`grammar1`):** Word-level tokenization and parsing designed for analyzing English sentence structures (noun phrases, verb phrases, determiners, nouns, verbs).
- **Formal Grammar / Symbol Mode (`grammar2`):** Character-level tokenization and parsing capable of handling formal language rules, recursive productions, and empty string ($\varepsilon$) derivations.

### 2. Granular Error Handling (`ParseError` & Tokens)
- Tracks precise token indices during recursive descent parsing.
- Identifies exact failure points in invalid strings, returning detailed diagnostic messages (e.g., *Expected '...', found '...'* or structural mismatch reasons).

### 3. Abstract Syntax Tree (AST) Generation
- Constructs hierarchical `Node` structures for valid inputs.
- Serializes syntax trees into clean, indented JSON format for structural verification and debugging.

---

## Project Structure
```text
formal-grammar-parser/
│
├── main.py              # Core parser engine, tokenization, grammar parser, and CLI runner
├── grammar1.txt         # Natural language grammar rules (CFG)
├── grammar2.txt         # Formal language grammar rules with epsilon transitions
├── sentences.txt        # Test suite for natural language sentences
├── sentences2.txt       # Test suite for formal strings and formal language tokens
└── README.md            # Project documentation
