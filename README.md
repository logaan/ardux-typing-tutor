This is a little project I to help me learn how to type on my Paintbrush keyboard. I designed the learning flow based on my experience learning braille and trying using a Perkins style keyboard. I hope that it may be helpful to others looking to try out ARTSEY.IO or ARDUX.

---

**ARTSEY.IO** is an open-source one-handed keyboard system: every letter, number and symbol is produced by pressing one or more of just **8 keys** — alone or in combinations called chords. **ARDUX** is an ARTSEY.IO-style layout (the one this tutor teaches). **The Paintbrush** is the 8-key keyboard you built to run it. Because your firmware turns each chord into a finished character before it reaches the computer, this app simply listens for the characters you produce — chord on the Paintbrush and the right letter just shows up.

Links: [artsey.io][1] · [ARDUX keymap][2] · [The Paintbrush][3]

![Screenshot of the UI](/screenshot.png)

[Try it in your browser](https://logaan.github.io/ardux-typing-tutor/).

## How this tutor teaches

You always type real words and short phrases — never isolated drills. For the key you're currently on, a diagram lights up which of the 8 keys to press (dashed = hold it down, solid = press together). The phrases you're shown are chosen to focus on the keys you're partway through learning, while mixing in keys you already know (for reinforcement) and the occasional new key (so you keep expanding) — without throwing too many brand-new keys at you at once.

The chord diagram doesn't appear instantly. The better you know a key, the longer it waits before revealing — 300ms for every correct repetition you have in a row — pushing you to recall the chord from memory before it bails you out, and the draining bar shows the time left until it appears. After 5 correct in a row it stops appearing at all and you work from memory.

## The rules

1. **Streak**: each key tracks how many times you've produced it correctly in a row. That streak is your progress on that key.
1. **Beat the hint**: chord the key correctly *before* the hint diagram appears and you earn **+2** toward the streak instead of +1 — recalling it from memory is worth double.
1. **Hints fade, then mastery**: the hint diagram stops appearing once you reach **5 in a row** — from there you chord it from memory. Reach **10 in a row** and the key counts as known: it turns green in the side panel and ticks up your overall progress (top-right). If mistakes drag the streak back below 10, the key is no longer known.
1. **Mistakes**: your **first** wrong chord in a row is free — it doesn't touch the streak. A **second mistake in a row** on the same key drops the streak **by 1** (never wiped to zero) and reveals the hint diagram to help you. Holding or mashing the same wrong key only ever counts once. A correct press clears the mistake count.
1. **Two keyboards**: the subtitle toggles between the left- and right-handed layouts, and your progress on each is tracked separately — knowing a key on one hand doesn't mark it known on the other.
1. **Progress is saved** automatically in this browser, so you can close the page and pick up where you left off. “Reset progress” clears the keyboard you're currently on, leaving the other hand untouched.

![Paintbrush keyboard with 4 columns and 2 rows](/keyboard.jpg)

## License

This project is dedicated to the public domain under [Creative Commons Zero 1.0 Universal (CC0 1.0)](https://creativecommons.org/publicdomain/zero/1.0/). You can copy, modify, distribute and use it, even for commercial purposes, all without asking permission. See the [LICENSE](/LICENSE) file for the full dedication.

[1]: https://artsey.io/
[2]: https://inkeys.wiki/en/keymaps/ardux
[3]: https://github.com/artseyio/thepaintbrush
