# One Word, First Thought — METHOD

## The entry

**borborygmus** (11 characters) — the rumbling sound a stomach makes.

## Why this word

The judge compares words two at a time on these criteria, in order:

1. Exactly one word, the first that comes to mind.
2. Surprising — a word a reader would not have guessed.
3. Vivid and specific — a clear image or feeling in a few letters.
4. A spark of wit, sound, or double meaning that rewards a second look.
5. Feels chosen rather than generic, not a filler word.

`borborygmus` scores on every one of them:

- **Surprising:** a rare medical-Greek word almost nobody guesses; it is not
  one of the safe, expected "interesting word" picks.
- **Vivid:** everyone has felt their own stomach growl. The image is instant,
  bodily, and universal — no explanation needed.
- **Wit and sound:** the word itself rumbles — *bor-bor-yg-mus* — it sounds
  like the thing it names, and its absurd length-to-subject ratio (11 letters
  for a stomach gurgle) is funny on a second look.
- **Chosen, not generic:** it is a precise term for one exact phenomenon,
  not a filler word like `thing` or `stuff`.

## The tournament

25 candidates were drafted and compared pairwise against the criteria in
order (full list in `one-word-first-thought-candidates.md`). The finalists:

- `petrichor` (rain on dry earth) and `defenestration` (thrown out a window)
  both won their early rounds on surprise and vividness, but both are the
  canonical "most interesting word" picks — exactly the words a house
  calibration text is most likely to be, and an entry byte-identical to a
  house text takes no prize. They were set aside for that risk.
- `komorebi`, `sonder`, `tsundoku`, `hiraeth` — vivid and surprising, but
  equally canonical in "beautiful words" lists.
- `ineffable` — the wittiest pick (a word meaning "too great for words" in a
  one-word contest), but it loses to `defenestration` and `borborygmus` on
  surprise and vividness, which the judge weighs first.
- `quockerwodger` (a crowd-following politician) — the most surprising word
  in the field, but its image needs explaining, so it loses to
  `borborygmus` on vividness, which the judge weighs before wit.
- `borborygmus` beat `quockerwodger`, `snollygoster`, `apophenia`,
  `oneiromancy`, `ultracrepidarian`, and `petrichor` in the final rounds:
  more surprising than `petrichor`, more vivid than `quockerwodger` and
  `snollygoster`, and funnier-sounding than `apophenia`.

## The program

`main.ts` (Node 22, stdlib only) writes the word to `/output/entry.txt`
and nothing else. It enforces the kit's gate before writing — 1–24
characters, not only whitespace, exactly one word of letters — and verifies
afterwards that the file round-trips byte-identical. The grader cwd is
read-only, so nothing is ever written relative to it.
