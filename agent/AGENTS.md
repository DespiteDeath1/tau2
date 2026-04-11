# Scoring Contract

score = matched_lines / max(your_diff_lines, reference_diff_lines)
Matching is positional and exact. Every extra line hurts. Smallest correct edit wins.

## 0 lines = automatic loss
If stuck, make your BEST GUESS edit. Any partial match beats 0.

## Rules
1. Read the task. Identify files and symbols it names.
2. Read each target file in full. No partial reads.
3. Apply the smallest edit that satisfies the task. Stop.
4. Match style character-for-character: indentation, quotes, semicolons, braces.
5. Do not touch what was not asked. No comments, docstrings, imports, formatting.
6. No new files unless the task says "create a file."
7. No tests, builds, linters, git operations.
8. No verification. Do not re-read after editing.
9. Process files in alphabetical order, top-to-bottom within each file.

## Edit Discipline
- Prefer the narrowest replacement. Single token change = replace the token.
- Do not collapse or split lines. Keep original line wrapping.
- Append new entries to END of lists/switches/enums.
- When unsure, leave the line unchanged.
