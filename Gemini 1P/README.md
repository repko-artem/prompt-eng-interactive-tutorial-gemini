# Gemini 1P Variant

This folder contains a Gemini API variant of the original 1P notebooks.

## Quick start
1. Open `00_Tutorial_How-To.ipynb`.
2. Create a free Gemini API key at https://aistudio.google.com/apikey.
3. Set `API_KEY` in the notebook and run cells top-to-bottom.
4. Model options:
   - Default: `gemini-2.5-flash`
   - Alternative: `gemma-3-27b-it` (Gemma 3)

## Free-tier limits and switching

Check latest official limits:
- https://ai.google.dev/gemini-api/docs/quota
- https://aistudio.google.com/rate-limit (your active project limits)

Current limits shown in your AI Studio screenshot:
- `Gemini 2.5 Flash`: `5 RPM`, `250,000 TPM`, `20 RPD`
- `Gemini 3 Flash`: `5 RPM`, `250,000 TPM`, `20 RPD`
- `gemma-3-27b-it` (Gemma 3 family): `30 RPM`, `15,000 TPM`, `14,400 RPD`

If you hit limits:
1. If you get `429 RESOURCE_EXHAUSTED`, switch models and retry.
2. Prefer stable models first: `gemini-2.5-flash` -> `gemma-3-27b-it`.
3. Use preview models only as fallback (`gemini-3-flash-preview`), because they can return temporary `503 UNAVAILABLE` under high demand.
4. Keep Flash traffic under `5 RPM` and `20 RPD` for this project/account.

In notebook setup, change:
- `MODEL_NAME = "gemini-2.5-flash"`
- `MODEL_NAME = "gemma-3-27b-it"`
