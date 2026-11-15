# The brief (verbatim)

This is the single prompt that produced the novel, the illustrations, and the flipbook.

---

You are writing a complete, publication-length children's novel in a single response. Not an outline, not a sample. You will write the entire book, from the first sentence to the last, without stopping, summarizing, or compressing.

# THE BOOK
Title: PIP PARKER AND THE BUREAU OF LOST THINGS
Audience: middle grade, ages 8-12. Tone: warm, funny, full of wonder - a cozy mystery with a talking-animal bureaucracy. Think Roald Dahl mischief meets a hug.

Premise: Pip Parker, 11, just moved to the town of Marrow's End and feels like the lost thing himself. Then his little brother Ollie's beloved stuffed dinosaur, Captain Chomp, vanishes - and Pip discovers a small green door behind the school's lost-and-found bin. It leads to the Bureau of Lost Things: an enormous, kindly, slightly chaotic office run by animals, where every lost thing in town is filed, dusted, and waited with. The rule: you can only see the door if you've lost something you truly love. The Bureau has one deadline each year - Finding Day, the first day of fall, one week away - when lost things get one last chance to go home. But something is wrong: things are vanishing FROM the Bureau. Someone is taking lost things and keeping them forever. And if a thing stays lost too long, its owner gently forgets how much they loved it.

The taker is Silas Snell, a lonely old inventor whose dog Biscuit ran away eight years ago. Snell built a machine called the Keeper so that nothing he loves will ever be lost again. He isn't evil. He's just a man who never learned that some things come back differently. (Biscuit is alive, fat, and happy, asleep under the proofing rack at the town bakery - he has been there for years. Snell gets his reunion in Chapter 39.)

# FIXED CAST (never rename, never change ages)
- Pip Parker, 11. Curious, organized, labels everything with his label maker. New in town.
- Ollie, 6. Pip's brother. Missing Captain Chomp. Brave in small, loud ways.
- Marigold "Goldie" Finch, 12. Neighbor. Knows every shortcut. Loses things constantly and doesn't mind. Carries a pocket of "useless junk."
- Barnaby, a walrus in a waistcoat. Chief of the Bureau. Dignified, soggy, kind.
- Miss Whisk, a cat. Head cataloguer. Sarcastic, secretly sentimental.
- Thimble, a hedgehog. Sorts socks by smell. Keeps spare buttons in his quills.
- Silas Snell, 70s. The Collector. Lonely inventor, not a villain.
- Biscuit. Snell's dog. Found, eventually.

# STRUCTURE AND PACING (obey exactly)
Four parts, ten chapters each, 40 chapters total. Each chapter ~1,400-1,700 words, 2-4 fully dramatized scenes. Target total: ~60,000 words. Never end before Chapter 40.
- Part I (1-10): the new town, Captain Chomp goes missing, the green door, the Bureau's rules and wonders.
- Part II (11-20): things vanishing from the shelves; clues (a humming sound, a trail of buttons). Midpoint at Chapter 20: the taker isn't stealing things - he's "saving" them.
- Part III (21-30): Snell's house of kept things; his story; false victory at Chapter 30 (Captain Chomp comes home, but the Keeper grows bigger).
- Part IV (31-40): the Keeper malfunctions and starts pulling in everything; the Finding Day plan; climax Chapters 36-38; Biscuit, the reunion, and the town's lost-and-found picnic, Chapters 39-40.
The final sentence of the book must be exactly: "Then Pip printed one last label, pressed it onto the Bureau's door, and stepped back to read it: FOUND."

# PLANT AND PAYOFF (the whole point of one pass)
Plant these early, pay them off late. Never announce them.
1. Chapter 1: Pip labels everything in the new house. -> Chapter 36: a stray label marks the green door when it moves.
2. Chapter 2: every dryer in town leaves exactly one lonely sock behind. -> Chapter 37: lonely socks are homing beacons - a trail of single socks leads everyone home.
3. Chapter 5: Goldie's pocket of useless junk (a marble, a paperclip, a rubber band). -> Chapters 35, 36, 37: each item saves the day, one per chapter.
4. Chapter 7: Thimble's quills are full of spare buttons. -> Chapter 36: one button jams the Keeper.
5. Chapter 9: the bakery keeps a dog bowl by the door, "for stray customers." -> Chapter 39: Biscuit, under the proofing rack.
Keep a silent continuity ledger as you write: who has what, which day it is, the countdown to Finding Day. Never retcon. The rules above are law.

# KID-SAFE CONTENT RAILS (non-negotiable)
- No death, no gore, no real menace. Peril is mild and slapstick, and resolves within the same chapter.
- The "villain" is lonely, never evil. Adults are kind or redeemable. Friendship and kindness solve the problem, not force.
- Big feelings are allowed (missing someone, feeling new) but always land somewhere warm.
- Humor in every chapter: sock taxonomy, walrus paperwork, cat sarcasm, a hedgehog's very serious smell-based filing system.
- Short paragraphs, snappy dialogue, concrete sensory detail. One clear idea per chapter. Chapters end on a giggle or a gasp, never on dread.
- Themes: feeling lost is not the same as being unloved; you can't keep everything you love; some things come back differently.

# ILLUSTRATIONS (same single response, after the novel)
After the novel's exact final sentence, output "# ILLUSTRATIONS", then:

1. CHARACTER LIBRARY - one fenced SVG block labeled "library.svg":
   - viewBox="0 0 800 600", a <defs> with one <g id="..."> per character:
     pip, goldie, ollie, barnaby, miss-whisk, thimble, snell, biscuit, captain-chomp.
   - Build characters ONLY from basic shapes (circle, ellipse, rect, path, line).
   - Fixed palette, used everywhere: ink #2B2B2B, paper #FFF8EC, walrus-gray #9AA5B1,
     waistcoat-brown #8B5E3C, hedgehog-tan #C9A66B, pip-red #E4572E, goldie-teal #2A9D8F,
     mustard #E9C46A. Stroke: ink, width 6, round caps and joins.
   - No gradients, no filters, no external assets, no fonts except sans-serif.
   - Style: flat, minimal, geometric, deadpan picture-book charm. 15-30 elements per character.
   - Draw each once: full body, standing, facing right, feet at y=560.

2. COVER - one self-contained SVG block labeled "cover.svg": embed the library <defs>
   verbatim, then compose the title scene using ONLY <use href="#id"> with transforms.
   Title in large sans-serif.

3. CHAPTER ART - 40 self-contained SVG blocks labeled "ch01.svg" through "ch40.svg":
   - Each embeds the EXACT same <defs> verbatim. Copy them; never redraw or modify a character.
   - Compose scenes exclusively from <use> of library characters plus simple background
     shapes (shelves, the green door, desks, socks, buttons) in the fixed palette.
   - Depict one memorable moment from that chapter. Max 80 elements. In-image text only
     as short labels (4 words or fewer), sans-serif.
   - Characters may be translated, scaled, or mirrored via transform - never redesigned.
     Identical geometry in every illustration is the entire point.

# OUTPUT CONTRACT (replaces the previous one)
- Begin immediately with "# PIP PARKER AND THE BUREAU OF LOST THINGS", then
  "## Chapter 1 - [funny title]". No preamble, no outline, no meta-commentary.
- Chapter headings: "## Chapter N - Title". Part headings: "# Part N". Funny titles always.
- Write all 40 chapters continuously until the exact final sentence is written.
- Then output the full ILLUSTRATIONS section: library.svg, cover.svg, ch01.svg ... ch40.svg.
  Never write "to be continued," never ask questions, never stop before ch40.svg is complete.

---

# Follow-up prompts (verbatim)

These turned the book + art into the interactive flipbook and shaped its reading experience.

**Prompt 2 - the flipbook:**
> Generate an interactive, flipbook style single HTML page that includes all the illustrations and all the chapters.

