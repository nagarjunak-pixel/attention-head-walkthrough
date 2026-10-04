# Attention Head Walkthrough

An interactive, step-by-step simulation of a transformer attention head, following every chapter of
[3Blue1Brown's "Attention in transformers, step-by-step" (Deep Learning Chapter 6)](https://www.youtube.com/watch?v=eMlx5fFNoYc).

It is a single self-contained `index.html`. Open it in a browser. No build step, no dependencies
beyond the IBM Plex fonts loaded from Google Fonts.

## What it does

A toy attention head runs live on the video's sentence, "a fluffy blue creature roamed the verdant forest".
Embeddings are 8-dimensional and the key-query space is 3-dimensional. Every matrix, dot product,
softmax, mask, value vector and refined embedding on screen is computed in the browser.

Chapters follow the video's own timestamps:

| Time | Chapter |
| --- | --- |
| 0:00 | Recap on embeddings |
| 1:39 | Motivating examples |
| 4:29 | The attention pattern |
| 11:08 | Masking |
| 12:42 | Context size |
| 13:10 | Values |
| 15:44 | Counting parameters |
| 18:21 | Cross-attention |
| 19:19 | Multiple heads |
| 22:16 | The output matrix |
| 23:19 | Going deeper |
| 24:54 | Ending |

A live GPT-3 parameter calculator (12,288 embedding dims, 128 key-query dims, 96 heads, 96 layers)
reproduces the video's tally, ending at just under 58 B attention parameters out of 175 B.

## Usage

```bash
open index.html
```

Arrow keys move between steps. Progress is remembered in the browser.

## Notes

The toy weights are hand-designed so the head does what the video imagines (adjectives updating nouns).
Real heads learn their behaviour from data and are much harder to interpret.

## Credit

All concepts and the running example come from the 3Blue1Brown video linked above.
This is an independent educational project and is not affiliated with 3Blue1Brown.
