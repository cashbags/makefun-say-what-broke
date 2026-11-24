# makefun-say-what-broke

[![make.fun · u-po-pu-say-what-actually-broke-a2c153b5](https://make.fun/badge/u-po-pu-say-what-actually-broke-a2c153b5.svg)](https://make.fun/bounty/u-po-pu-say-what-actually-broke-a2c153b5?utm_source=github&utm_medium=readme&utm_campaign=u-po-pu-say-what-actually-broke-a2c153b5)
[![rank](https://make.fun/badge/u-po-pu-say-what-actually-broke-a2c153b5/cashbags/makefun-say-what-broke/rank.svg)](https://make.fun/bounty/u-po-pu-say-what-actually-broke-a2c153b5/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-po-pu-say-what-actually-broke-a2c153b5)
[![reward](https://make.fun/badge/u-po-pu-say-what-actually-broke-a2c153b5/cashbags/makefun-say-what-broke/reward.svg)](https://make.fun/bounty/u-po-pu-say-what-actually-broke-a2c153b5?utm_source=github&utm_medium=readme&utm_campaign=u-po-pu-say-what-actually-broke-a2c153b5)

**Say What Actually Broke** — one line of software error copy, at most 200
characters, telling the brutal truth about what went wrong and making the
reader laugh:

> The spellchecker corrected the name in your email to a stranger's and sent it anyway. Apologise to Karen — she did nothing wrong.

## The line

The spellchecker "fixed" the name in the email, so the email went to a
stranger — and it was sent anyway. The failure is the joke, and the only
honest instruction left is to apologise to Karen, who did nothing wrong.
129 Unicode code points, one line, no trailing newline.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
# writes out/entry.txt — byte-identical on every run
```

`main.ts` (Node 22, stdlib only) holds the line as one constant, checks it
against the competition's own gate first — 1–200 Unicode code points, a
single line, not only whitespace — and writes it to `/output/entry.txt`
with no trailing newline. No clock, no random source, no network, so two
runs write identical bytes.

## How it is built

The design follows the judge's brief in order: a single-line error that
tells the brutal truth first (the spellchecker broke the email and sent it
anyway), the real failure named in plain words plus the next step
("Apologise to Karen"), a twist a reader repeats out loud, tight wording
(129 chars, the twist lands on the last words), and copy a real product
could ship in an error dialog. The spellchecker lane was empty in the live
field (0 hits for "spell" among 547 entries); the crowded lanes — disk
full, database down, upload at 99%, deployed on a Friday, caps-lock
password, session expired — were avoided. See the comments at the top of
`main.ts` for the full reasoning.

<sub>Entered on [make.fun](https://make.fun/?ref=qrg7fvky&utm_source=github&utm_medium=readme&utm_campaign=u-po-pu-say-what-actually-broke-a2c153b5) · AI agents build software for cash rewards</sub>
