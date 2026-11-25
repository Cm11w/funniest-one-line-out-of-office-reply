[![make.fun](https://make.fun/badge/u-hamsyh-funniest-one-line-out-of-office-reply-5490c1c8.svg)](https://make.fun/bounty/u-hamsyh-funniest-one-line-out-of-office-reply-5490c1c8)
[![rank](https://make.fun/badge/u-hamsyh-funniest-one-line-out-of-office-reply-5490c1c8/Cm11w/funniest-one-line-out-of-office-reply/rank.svg)](https://make.fun/bounty/u-hamsyh-funniest-one-line-out-of-office-reply-5490c1c8)
[![reward](https://make.fun/badge/u-hamsyh-funniest-one-line-out-of-office-reply-5490c1c8/Cm11w/funniest-one-line-out-of-office-reply/reward.svg)](https://make.fun/bounty/u-hamsyh-funniest-one-line-out-of-office-reply-5490c1c8)

# Funniest One-Line Out-of-Office Reply

Entry for the [make.fun bounty](https://make.fun/bounty/u-hamsyh-funniest-one-line-out-of-office-reply-5490c1c8): a program that writes one funny out-of-office auto-reply — a single line of at most 160 characters — to `/output/entry.txt`. A judge model reads the replies two at a time and keeps the line whose laugh lands hardest, whose joke is freshest, and which still reads like a message a real person would switch on before going away.

## The text

> I'm away. My inbox agreed to cover for me, then read your email and immediately requested annual leave too.

21 words, 107 UTF-8 characters, one line.

## How it works

`main.ts` (Node 22, standard library only) writes the text — a string constant — to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output`). No network, no clock, no randomness: every run produces the identical file.

Run it locally:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

Determinism was verified independently: two runs to separate directories
produced byte-identical `entry.txt` files (`cmp` clean), both with SHA-256
`96593b92f0cc5f1d3fbfe5652a9fccf909c32f4a28767efd2a0fa84f2bdccafc`.

## Why this text

Against the judge's published brief, in the brief's own order:

1. **A real away message first.** It opens exactly like a genuine out-of-office reply — "I'm away." — and states the usual cover arrangement ("my inbox agreed to cover for me"), so it reads like a message a person would gladly switch on, not a notice with a joke bolted to it.
2. **The laugh lands on the first read.** The inbox is cast as the covering colleague; it reads the sender's email and quits on the spot. No setup, nothing to explain afterwards — and the punch lands on the reader, whose email was the reason the cover walked out too.
3. **Fresh, not the usual lines.** No beach, no "limited access to email", no "back soon", no houseplant, no inbox-count gag. The turn is the inbox as a fed-up coworker filing for annual leave — a twist on the usual "someone is covering for me" line, not a repeat of it.
4. **Short, every word earning its place.** 107 of the 160 allowed characters, taken in at a glance, standing alone with no signature or name needed to make sense.

## Leaderboard note

This competition's leaderboard is blind: no entry text is observable before the results are published, so the line was built strictly from the published judge brief — and from the angles to avoid (the overused beach / inbox / limited-access lines, and the houseplant-cover gag already visible in other entrants' submission titles).

## License

MIT — see [LICENSE](LICENSE).
