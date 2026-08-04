# Chordika &amp; Recorika

**Card-sized 3D-printed whistles. Swap a card, change the key.**

日本語版は [README.ja.md](README.ja.md) をご覧ください。

Eight fipple pipes are 3D-printed into a credit-card-sized plate (85.6 × 54 × 4 mm).

- **Chordika** — blow any three adjacent pipes in one breath and a tuned triad sounds.
  Twelve cards cover every key, and the position-to-chord mapping is *identical* on all of
  them, so the same hand motion transposes when you swap the card.
- **Recorika** — the scale counterpart: one octave of a major scale, lowest pipe on the
  left, highest on the right.

The data is published, so anyone with a 3D printer can make the same thing. Each card is exactly credit-card sized, so it travels in a wallet or a card case.

![The twelve Chordika cards](assets/photo_chordika_deck.jpg)

**Project site: https://unryu.org/chordika/**

## The layout

On every Chordika card, the same pipes give the same chord function:

| Pipes | 1·2·3 | 2·3·4 | 3·4·5 | **4·5·6** | 5·6·7 | 6·7·8 |
|---|---|---|---|---|---|---|
| Chord | ii | IV | vi | **I** | iii | V |
| on C / Am | Dm | F | Am | **C** | Em | G |
| on G / Em | Am | C | Em | **G** | Bm | D |

Each card therefore carries a major key *and* its relative minor. Only vii° (the
diminished triad) is missing.

This works because the notes are ordered by scale degree **2·4·6·1·3·5·7·2** rather than
by pitch — which makes every three adjacent pipes a diatonic triad.

## What's in this repository

```
index.html          project site (Japanese / English)
stl/                print data — 12 Chordika cards, 1 Recorika card, 1 cover, 2 box parts
3mf/                pre-sliced files for the Bambu Lab A1 mini (PLA), the same 16 items
video/              short clips of the cards being played
assets/             cheat sheets (JA/EN), chord maps for all 12 keys, photos and figures
```

**Hear them:** start with the [demo video on YouTube](https://www.youtube.com/watch?v=mi-en3c57SM).
The [project site](https://unryu.org/chordika/) also has short clips — chords on
Chordika, the scale on Recorika, and a tune played on it.

If you own a **Bambu Lab A1 mini**, the files in `3mf/` are already sliced with the
settings below and can be sent straight to the printer. They assume Bambu PLA Basic;
each card is about 8.5 g and takes roughly 1 h 15 min. For any other printer or
filament, slice the STL yourself using the settings below.

## Printing

- **0.08 mm layers, 0.5 mm outer wall.** The pipe walls are thin; do not print coarse.
- **No supports.** Print flat, as-is.
- **One card per plate.** Two cards on one plate double the time per layer, the edges cool
  and shrink, and the card warps. A brim alone will not stop it.
- **Brim about 5 mm, brim-to-object gap 0.** With a gap the brim never fuses to the part
  and holds nothing.
- White PLA works well. Translucent PETG is beautiful — the bores show through the plate.

**Remove any sharp spots before you blow into it.** A fresh print leaves fine burrs and
sharp corners, and this is an instrument you put to your lips — as printed it is not safe.
I have come close to cutting my mouth on one more than once. Run a finger along the card's
edges and around the mouthpieces, and smooth anything that catches with a file or the back
of a knife.

Blow with about as much breath as a recorder. Too hard and the pipe jumps an octave.

## Cover card and box

The **cover** (`chordika_cover.stl`) is a 0.5 mm plate with no pipes and "Chordika" cut
through it. It shares the cards' outline and strap-hole position, so it stacks on top of
the twelve and threads onto the same cord.

The **box** is two parts: an open tray (`chordika_box_base.stl`) and a lid that slips over
its outside (`chordika_box_lid.stl`). All thirteen cards lie flat inside, and the lid
carries the same cut-through lettering as the cover. A scallop on each long side lets you
pinch a card out. Closed, it is about 94 × 62 × 57 mm.

The box holds no pipes, so it prints at **ordinary 0.2 mm layers with no supports** — no
need for the fine settings the cards require.

## How it was designed

Pipe length and pitch were fitted from real printed-and-blown pipes as `f = A/(L+e)`.
Solving it backwards turns a wanted note into a length, so a generator written in Python
(trimesh + manifold3d) emits the whole card from a key name. The plate thickness is fixed
at 0.5 mm — exactly the floor thickness of the pipes; any thicker and it eats into the
bore and the card goes silent.

## Licence

[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/) — see [LICENSE](LICENSE).

**You may** print these for your own use, play them, and share them unchanged with credit,
including non-commercially in classes and workshops.
**You may not** use them commercially (selling prints, paid services) or distribute
modified data. If you want different terms, please get in touch.

---

From the "AI whistle-making" project by Kazutaka Kurihara (Tsuda University).
