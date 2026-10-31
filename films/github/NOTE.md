# GitHub, explained: note

`final.mp4`: 25.00 s, 1920x1080, 30 fps, silent. Source: `index.html` (uses the repo's `runtime/` via `../../runtime/`). Plan: `STORYBOARD.md`.

## The idea
One small change, followed from the edit to the merge: in a recipe repo, "3 eggs" becomes "2 eggs". The film cuts between GitHub's own UI (where the change is made) and a large commit graph (where the concept is *drawn*): a branch forks off, a pull request is a dashed line asking to come back, and the merge closes the loop in purple. I picked it because a beginner needs to see a branch and a merge, and because GitHub's own UI strings ("maya wants to merge 1 commit into main from fewer-eggs", "Merge pull request") teach the vocabulary better than marketing copy would.

## Beats and what each buys
| frames | beat | the viewer… |
|---|---|---|
| 0-90 | hook: the camera glides along the history, "GitHub keeps every version of your project." | …sees a project as a line of saved versions |
| 90-254 | edit and commit: 3 → 2 eggs; the Commit changes dialog; message typed; "Create a new branch… and start a pull request"; Propose changes | …watches a real change get saved |
| 254-432 | branch and request: a blue branch forks off with the new commit; a dashed green "Pull request #14" line reaches back toward main | …learns branch and pull request as pictures |
| 432-580 | pull request: Open badge, sam's comment, the approval, Merge pull request → Confirm merge → merged | …sees review happen |
| 580-700 | merge (hero): the dashed line turns solid purple, main reaches the purple merge commit, a purple light blooms, "Merged. The change is now part of main." | …sees the loop close |
| 700-750 | name: Invertocat + "GitHub" crash in over the blurred graph and settle | …knows whose it is |

## What is real and what is illustrative
- **Real:** the Invertocat path (copied unmodified from github.com's inline SVG, shown in black). Mona Sans and Monaspace Neon are GitHub's own OFL typefaces, installed from npm (Fontsource); licences are in `fonts/`. The UI strings follow GitHub's wording as I know it, and the merge-commit message format "Merge pull request #14 from maya/fewer-eggs" follows git's convention.
- **Illustrative:** the repo, people (maya, sam), commits, hashes, comment and PR number are invented. The editor, commit dialog and PR page are **rebuilt fragments** made from Primer light-theme colours, which I took from memory and did not check against the live site, because the capture could not load GitHub's CSS: `github.githubassets.com` is blocked by this sandbox's network policy. The octicon-style glyphs and the identicon are redrawn, and the merge flow skips the merge-commit form shown before "Confirm merge". The real UI may differ in detail.
- **"GitHub" in the lockup** is set in Mona Sans. It is not GitHub's official wordmark artwork.

## Gates (numbers from the scripts)
- `look.py final.mp4 --expect 25`: **G0 PASS** (25.00 s, no audio planned); **G2 PASS** (no run of > 3 flat frames); **G3 PASS** (end hold 1.17 s; final shot 1.67 s = 7 % of the film).
- `lint.mjs index.html`: **GATE G5 PASS**. C5 WARN on the mono commit hashes and branch pills under the graph dots: that's git-log material, kept on purpose. A first pass FAILED C6 on the PR's tab row ("Conversation 1 / Commits 1…"), which read as a header bar on the pull-back, so I deleted it.
- `Motion.selfTest`: ok, 24 random seeks, 0 mismatches.
- **G1 and G4 are by eye only** (no script number): the UI is magnified about 2.9-3.3x, so 14 px UI text renders at about 41-46 px (about 0.04 H), and panels are cropped by the frame. Each frame has one subject: the dot, the dialog, the PR box, or the merge.
- **Motion note:** mean luma change 2.4/255, below the human band (median 6.8, IQR 4.4-9.8). The film is calm and mostly white UI. The calm is a choice for a beginner explainer, but it is also a real gap: the stretch between pull-back and lockup (21.8-23.3 s) is a slow drift.

## Frame descriptions (look/sheet.jpg, draft)
0.8 s: the camera glides along a grey history line, with a past blue branch rejoining at "Merge pull request #9", as the first words rise above. · 2.3 s: the full hook sentence over the two newest commits. · 3.9 s: editor macro, line 4 now reads "2 eggs" with the caret. · 5.5 s: the Commit changes dialog, with "Use" being typed. · 7.0 s: the cursor travelling to the branch option. · 8.6 s: a hard cut onto the blue branch line drawing off "Sort recipes by meal". · 10.1 s: "Your commit waits on its own branch." with "branch." in blue, and the new commit labelled. · 11.7 s: the dashed request line drawing, with the next sentence starting. · 13.3 s: "A pull request asks to merge it back." with the green Pull request #14 pill. · 14.8 s: PR title and Open badge. · 16.4 s: sam's comment. · 18.0 s: the cursor on Merge pull request. · 19.5 s: the purple merge line drawing into main. · 21.1 s: "Merged." in purple, with the purple light under the merge commit (the hero). · 22.6 s: the full closing sentence over the whole change. · 24.2 s: Invertocat + GitHub over the blurred graph. None of these frames would pass as a slide, though the three sentence frames are the closest: a centred line over the graph.

## What I'd still improve
- No sound: with an ElevenLabs key, a voice-over would let the sentences go and give the UI acts more room. Three hand-placed hits (the commit press, the branch landing, the merge) would also help.
- The graph acts are sparse below the human motion band. A second plane (blurred foreground commits passing during the camera moves) would add depth.
- The UI fragments should be checked against the live GitHub UI (dialog wording, button labels) before anyone outside this repo sees the film.
