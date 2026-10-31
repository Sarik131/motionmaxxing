# GitHub, explained: storyboard

25 s, 1920x1080, 30 fps (750 frames), smooth clock, silent (no ElevenLabs key on this machine).

## PAGE
- **Problem:** a beginner hears "GitHub" and gets jargon (repo, commit, branch, pull request, merge) with no picture of what actually happens.
- **Audience:** someone new to it (a student, a designer, a new hire), watching on mute in a feed or a course page.
- **Goal:** education. Afterwards they can say: GitHub keeps every version of a project; you save a change as a commit on a branch; a pull request asks others to review it; merging puts it into main.
- **Emotion:** from "this is jargon for programmers" to "oh, that's just how a team shares one careful change."

**The one true thing:** a single small change, followed from the edit to the merge in GitHub's own UI. Assumption: a beginner learns the vocabulary faster from one concrete change than from a feature tour.

## Brand inventory
| Look at | What GitHub has |
|---|---|
| Logo shape | The Invertocat in a circle. It doesn't resemble a control. It stays the signature and is not given a forced job. |
| Core control | The green **Commit changes** / **Merge pull request** button |
| Signature material | The commit graph (dots on lines that fork and rejoin), diffs (red/green lines) |
| Key verb | commit, branch, merge |
| Success moment | The purple **Merged** state and the branch line rejoining main |
| Voice | Plain and direct; the product explains itself in its own strings ("maya wants to merge 1 commit into main from fewer-eggs") |
| Colour logic | Primer state colours: green = open/added, red = removed, purple = merged, blue = branch name. Nothing else is coloured. |
| Type | Mona Sans (GitHub's own, OFL); Monaspace Neon for code (GitHub's own, OFL) |
| Would never | Hacker clichés: green-on-black code rain, hoodies, glitch, neon |

Capture note: `brand.mjs` got GitHub's page **without its CSS** (Times New Roman, link blue `#0000ee`), and `github.githubassets.com` is blocked by this sandbox's network policy, so the capture was discarded. The palette is Primer's light theme (from memory, not verified live), the fonts are GitHub's open-source families from npm (Fontsource), and the mark is the official path from the page's inline SVG.

## Ideas
1. *(first, discarded)* An Octocat waving beside a cloud with arrows over "Where the world builds software." That's the category costume, and it explains nothing.
2. **A UI documentary of one change.** A recipe repo: "3 eggs" becomes "2 eggs", committed to a new branch, opened as a pull request, approved, merged. The commit graph carries the film between UI moments, so the concepts are *drawn* (a branch literally forks off, a pull request is a dashed request line, a merge closes the loop).
3. A typographic essay written entirely as a git log, scrolling.

Cover-the-logo test: the green Commit button, "wants to merge 1 commit into main from…", "Merge pull request", the purple Merged state and the commit graph are GitHub's own UI. A competitor's film would need different strings and colours.
**Pick: 2.** Beginners need to *see* a branch and a merge. The graph performs the words, and the UI strings are GitHub's real vocabulary.

## World
- **Graph acts (A, C, E, F):** a light Primer canvas with a soft key from the top left falling off to the bottom right, plus temporal grain. A soft light pool follows the "live" change, and a purple light blooms once, at the merge (light as an event). Depth comes from contact shadows on dots and labels, and the camera travels along one long graph (parallax-free, one lens).
- **UI acts (B, D):** GitHub's light UI magnified about 3x by the camera (text ≥ 0.04 H; panels cropped by the frame), with one directional falloff overlay. The UI is a rebuilt fragment at real proportions.
- **Sound:** none (no key). The picture runs on a fixed cadence.
- **Hero moment (the screenshot):** the merge. The dashed green request line turns solid purple, the main line reaches the purple merge dot, and a purple light blooms under it with "Merged." landing above.

## Beats (frames at 30 fps)
| # | role | frames | buys: the viewer… | picture with the text covered | words | in / out / handoff |
|---|---|---|---|---|---|---|
| A | hook | 0-90 | …sees a project as a line of saved versions | camera already gliding along a history of commits (one past branch-and-merge loop) to the newest dot | "GitHub keeps every version of your project." | starts moving; decelerates on HEAD; dives into the dot, cut 90 |
| B | proof | 90-254 | …watches a real edit and the commit dialog choose "a new branch… start a pull request" | editor macro: "3 eggs" → "2 eggs"; Commit changes; the dialog's message typed; radio → new branch `fewer-eggs`; press **Propose changes** | UI strings only | cut in mid-push; cut on the press, before release |
| C | turn | 254-432 | …sees a branch fork off and a pull request as a request to come back | blue branch line peels off HEAD, the new commit crashes onto it; then a dashed green line reaches toward main with a "Pull request #14" pill | "Your commit waits on its own branch." / "A pull request asks to merge it back." | camera travels right; dives into the pill, cut 432 |
| D | proof | 432-580 | …sees review happen: a comment, an approval, Merge → Confirm | PR page macro: title, green Open, "maya wants to merge 1 commit into main from fewer-eggs", sam's comment, approval, merge box | UI strings only | press Confirm merge; box turns purple; cut 580 |
| E | point | 580-700 | …sees the merge close the loop | dashed line turns solid purple, main extends to the purple merge dot, purple light blooms, the camera pulls back over the whole history | "Merged. The change is now part of main." | pull back continues into F |
| F | cta | 700-750 | …knows the name | Invertocat + "GitHub" crash in from 3.5x over the blurred graph, settle, about 1 s resolved hold | "GitHub" | ends on a designed stillness |

Importance: A 2, B 2, C 2, D 2, **E 3**, F 1 (1 of 6 is "the point").
Checks before building: G1 (UI at about 3x: 14 px UI text → about 42-45 px; panels wider than the frame); G3 (F is 1.7 s = 7 % of the film; resolved hold under 1.4 s); G4 (one lit subject per frame: the dot, the dialog, the PR box).
