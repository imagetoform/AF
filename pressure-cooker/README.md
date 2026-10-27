# Pressure Cooker Poetry: Reader Edition

A generative reading room where the reader is the main input. They bring words, and the
cooker finds the poem those words belong to and builds the frame around the reader. The
poem text is never altered.

Open `index.html` in a browser. With only this repository it runs on the public sample
excerpts in `corpus/corpus.sample.txt`.

## What the reader controls

| Reader input | What it changes |
|---|---|
| The words they type | Which poems heat up (TF-IDF plus six semantic axes read out of the books), which words are highlighted in the poem, and the ransom tiles that make up the collage |
| How they type: tempo, deletions, caps and `!`, length | The PSI on the gauge (0 to 15, the real operating range of a pressure cooker) and the layout family |
| Tapping a word in the poem | Adds the word to their ingredients and opens the next unread poem that uses it, building a path through both books |
| Write back | Notes pinned beside the poem, stored only in that browser |
| Forget me | Erases their words, path and notes |

## Layout families

Chosen from the reader, not at random:

- **Cosmic Editorial** (tender or cosmic words, or a hesitant hand): ink ground, orbits, the reader's words in orbit.
- **Collage Organism** (wound or body words): vermilion ground, torn tiles, tape, cutouts.
- **Diagrammatic Choir** (market, algorithm, system): cobalt blueprint; wires run from each reader tile to the place that word appears in the poem.
- **Monolithic Manifesto** (high pressure, raised voice, fire): the reader's most charged word printed at a size the frame can't hold.

## Determinism

Every visual choice draws from a named Mulberry32 stream seeded by
`engine version + poem id + the reader's words + rounded typing metrics`. Same recipe,
same room. "Copy edition recipe" exports that manifest as JSON.

## Privacy

Everything runs client-side. No network calls besides Google Fonts. Nothing the reader
types leaves the browser.

## The full manuscript

`corpus/corpus.txt` holds both chapbooks and is gitignored on purpose; the repository is
public and the manuscripts are unpublished. To run with the full text:

```
python3 build.py          # dist/pressure-cooker.html, full corpus inlined (gitignored)
python3 build.py --sample # dist/pressure-cooker.sample.html
```

When `index.html` is served from a local server next to `corpus/corpus.txt`, it loads
the full corpus automatically.

### Corpus format

```
=BOOK id | Title | after ...
=MOVE I | Movement title
=POEM 1 | Poem title            (append "| excerpt" for partial text)
lines, with a blank line between stanzas
```
