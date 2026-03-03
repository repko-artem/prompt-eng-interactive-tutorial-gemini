# Gemini Prompt Engineering Interactive Tutorial

This repository now includes a Gemini-first notebook track in `Gemini 1P`.

## Quick start (Gemini)
1. Open `Gemini 1P/00_Tutorial_How-To.ipynb`.
2. Create a free API key in Google AI Studio: https://aistudio.google.com/apikey
3. Set `API_KEY` and run notebook cells top-to-bottom.

Default model in the Gemini track: `gemini-2.5-flash`.
Optional model: `gemma-3-27b-it` (Gemma 3).

## Free-tier limits

Official free-tier limits can change. Check the latest table:
- https://ai.google.dev/gemini-api/docs/quota

Your effective limits are shown in AI Studio and can be lower than generic documentation:
- https://aistudio.google.com/rate-limit

Current limits shown in your screenshot:
- `Gemini 2.5 Flash`: `5 RPM`, `250,000 TPM`, `20 RPD`
- `Gemini 3 Flash`: `5 RPM`, `250,000 TPM`, `20 RPD`
- `Gemma 3 27B` (`gemma-3-27b-it`): `30 RPM`, `15,000 TPM`, `14,400 RPD`

Generic doc references (may differ by account/project):
- `gemini-2.5-flash`: often listed higher in docs
- `Gemma 3 & 3n`: `30 RPM`, `15,000 TPM`, `14,400 RPD` (matches your screenshot)

Preview models are usually more restricted and can be unstable:
- `gemini-3-flash-preview` has a free tier, but limits and availability can vary (and can return temporary `503 UNAVAILABLE` during high demand).

## Avoid rate-limit overruns

1. Start with `gemini-2.5-flash` for the tutorial.
2. If you hit `429 RESOURCE_EXHAUSTED` on Flash (`5 RPM / 20 RPD`), switch to `gemma-3-27b-it`.
3. If a preview model returns `503 UNAVAILABLE`, retry later or switch back to a stable non-preview model.
4. Throttle requests to your AI Studio limits (currently `<=5 RPM` for Flash in your project).

Quick switch in notebooks:
- `MODEL_NAME = "gemini-2.5-flash"`
- `MODEL_NAME = "gemma-3-27b-it"`
- `MODEL_NAME = "gemini-3-flash-preview"` (preview behavior may vary)

## What this course covers

After completing this course, you will be able to:
- Master the basic structure of a strong prompt
- Recognize common failure modes and apply practical fixes
- Understand model strengths and limitations
- Build robust prompts from scratch for common use cases

The course includes 9 chapters with exercises and an appendix of advanced methods.

## Table of contents

### Beginner
- Chapter 1: Basic Prompt Structure
- Chapter 2: Being Clear and Direct
- Chapter 3: Assigning Roles

### Intermediate
- Chapter 4: Separating Data from Instructions
- Chapter 5: Formatting Output
- Chapter 6: Precognition (Thinking Step by Step)
- Chapter 7: Using Examples

### Advanced
- Chapter 8: Avoiding Hallucinations
- Chapter 9: Building Complex Prompts (Industry Use Cases)
- Appendix: Chaining Prompts, Tool Use, Search and Retrieval

## Notes

- `Gemini 1P` contains the Gemini API version.
- `Anthropic 1P` and `AmazonBedrock` folders are kept for reference/original variants.
