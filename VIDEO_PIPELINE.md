# Faceless NBA Story Video System (Sawakita-style, upgraded)

> **What this file is:** a complete production spec + pipeline for making **13–15 minute** faceless
> NBA/basketball story videos that match the competitor **澤北SG (@Sawakita)** and beat it on editing quality.
>
> **How to use it:** paste this whole file into Claude (or another strong AI model) and say:
> *"Use VIDEO_PIPELINE.md. Topic/title: ___. Language: ___. Give me Part 2 outputs A → E."*
> The AI will return titles, a timed script, an edit-ready shot list, captions (SRT) and the description.
>
> **Evidence:** everything in Part 1 is based on the competitor data in **Part 4**:
> - NexLev data for ~120 videos;
> - an AI frame log of a full 10-minute video (estimates);
> - an **ffmpeg frame-by-frame measurement** of a downloaded video (exact).
>
> Rules marked **OURS** are where we deliberately do better than the competitor.
> Thumbnails are covered later (only a short placeholder here).

---

## PART 0 — Quick reference card

| Item | Competitor (measured) | **OUR RULE** |
|---|---|---|
| Video length | 10:02–12:19 (most 10:10–10:55) | **13:00–14:59** |
| Narration words | ~4.5 Mandarin chars/sec | **~150 words/min English → 1,950–2,250 words** (Urdu/Hindi: same 13–15 min of speech) |
| Game clip length | 3.1–3.3s in newest video (older: up to 13s) | **STRICT: max 4.0s per clip, every clip. No exceptions.** Target 2.5–3.5s |
| Still photo length | 4.7–6.6s, slow zoom-in | 3.5–5.5s, slow zoom/pan, blurred-background fill |
| Screen time split | 68% video / 27% photos / 5% graphics (newest) | **~60% clips / ~25% photos / ~15% animated graphics** |
| New visual every | ~4.3s (body) | **every 3–4s** |
| Subtitles | 100% of narration, new caption every ~1.7s, 4–14 chars, 1 line | Same + **keyword highlight** in brand colour |
| Text on images | None (only subtitles + logo badge) | **OURS:** name tags, stat cards, quote cards, chapter cards |
| Voice | Male, deep (median pitch ~108 Hz), expressive (~14 semitone range), 350 ms pause between phrases | Male, deep, energetic storyteller; same phrase-pause rhythm |
| Music | Barely audible bed, 20–28 dB under voice; mood changes per chapter (older video) | Bed 20–24 dB under voice + ducking, **mood per chapter**, swells in pauses |
| SFX | ~1–2, intro only | **OURS:** subtle whoosh/pop/riser, ~1 every 20–30s |
| Game audio | Muted | **Muted, always** |
| Transitions | Hard cuts + cross-dissolve + dip-to-black + pixelate + watercolour wipe | Hard cuts on action; dissolve/whip/zoom on idea changes; branded wipe between chapters |
| Brand | Yellow border + `澤北SG` badge top-left on every frame; fixed catchphrase intro | Own colour border + logo badge; own catchphrase |

---

## PART 1 — Production spec (the rules)

### 1.1 Format & length

- 16:9, 1080p minimum (4K if possible), 30 fps, faceless.
- **Length 13:00–14:59.** Narration ≈ 13:00–14:20, plus a ~10s intro and a 20s end screen.
- Upload rhythm: start with 3/week. Go daily once the system runs smoothly (the competitor posts ~1/day).

### 1.2 Language

**Competitor:**
- Narration is in **Mandarin**. Subtitles use **Traditional Chinese** characters (Taiwan/HK audience).
- **Player names stay in English letters** inside the Chinese text (`LeBron`, `Bronny`, `Wembanyama`, `KD`).
- It's packed with **fan slang and nicknames** (嘴綠 = Draymond Green, 濃眉 = Anthony Davis, 字母哥 = Giannis). It sounds like an insider fan, not a news anchor.
- The narrator refers to himself by his **channel name in the third person** ("Zebei thinks…"). That gives the channel a personal voice without a face.

**OUR RULES (any language):**
1. Pick one language per channel: `LANGUAGE = English | Urdu | Hindi | …`. Voice, subtitles and title all use it.
2. Keep **player/team names in English letters**, even inside Urdu/Hindi text.
3. Use 5–10 recurring fan nicknames per video (e.g. "King James", "The Greek Freak", "Wemby").
4. The narrator has a name and uses it in the third person 2–4 times per video ("{NARRATOR} thinks this is…").
5. Write the way people speak, not like an essay. Short phrases, one idea each.
6. Always upload an **English SRT** as well, even if the video is in another language (wider reach, better search).
7. **Audience angle:** the competitor's best recent video (3x) is about a player from its own audience's country.
   Find the story your audience feels close to (South Asian fans, Asian players, underdogs, players popular in your region).

### 1.3 Titles

**Competitor formula** (60/60 titles follow it, 65–90 Chinese characters):

```
[SHOCK FACT/RESULT]！ + [descriptor] + [PLAYER NAME] + [是否/到底/究竟/為何 … ？] +
[proof point 1]、[proof point 2]， + [Famous name]：[short quote]  OR  [speculation？！] ｜[Brand]
```

| Feature | Frequency |
|---|---|
| Ends with the brand `｜澤北SG` | 60/60 |
| Player named (English letters) | ~58/60 |
| First clause ends with `！` / `？！` | ~60/60 |
| Central question word (whether / really / why) | ~60/60 |
| Two proof points joined by `、` | ~55/60 |
| Hard number (cm, %, years, $, games) | ~45/60 |
| Ends with a quote `Name：…` | ~20/60 (older popular videos) |
| Ends with speculation `…？！` | ~20/60 (newest videos) |

**OUR title rules (YouTube shows ~60–70 chars on mobile):**
- Title: 55–75 characters, with the **player name and hook in the first 40 characters**.
- Must contain: one **shock fact or number** + one **open question**. Never answer the question in the title.
- Proof points and quotes from the competitor formula go into the **thumbnail text** and **first description line**, not the title.
- Generate 10, score each 1–5 on clarity, curiosity and emotion, and keep the top one.

**10 proven title formulas (adapted from their outliers):**

1. **Banned / too strong:** `The NBA Had to BAN This [Play/Trade/Player]. Here's Why` (their #2 all-time, 1.2M)
2. **War instead of show:** `The Most Violent All-Star Game in NBA History` (their #1, 1.3M)
3. **Undersized underdog:** `[5'8"] and in the NBA?! How [Player] Proved Everyone Wrong` (3 hits, 340K–540K)
4. **Bust mystery:** `[Record/Pick] to Out of the League: What Really Happened to [Player]?` (500K–734K)
5. **Champion to vanished:** `Champion at 23, Gone at 26: The [Player] Mystery` (519K)
6. **Local-angle legend:** `Is [Local/Asian Player] Really the Greatest [Position] Ever?` (their best recent, 3x)
7. **Number shock news:** `[40] Assists in One Game?! How [Player] Changed [Team] Overnight` (2.5x)
8. **Will X succeed?:** `Fired, Doubted, Back: Can [Player] Actually Save His Career?` (their daily news format)
9. **Peak breakdown:** `How Unstoppable Was Prime [Player], Really?`
10. **Quote hook:** `"[Short quote]": Why [Famous Player] Feared [Player]`

### 1.4 Script

**What the competitor does (measured hook, 0:09–1:20):**
1. Show a striking image and ask the viewer a question ("Looking at this photo, what's your first reaction?").
2. Answer it right away and drop the news fact with ages/numbers ("41-year-old LeBron and 21-year-old Bronny…").
3. Use an **"on one hand… on the other hand…"** structure, then the twist **"in fact, the exact opposite"**.
4. Add authority: an **ex-player's quote**, then the **subject's own quote**.
5. End the hook on the **thesis question** at ~78s ("So what is his situation next season? Is this really good for him?").
6. After the hook, each section opens with a rhetorical question. Chapters cover background → rise → deep skill/tactic
   breakdown with comparisons ("Taiwan's Chris Paul") → verdict → a question for the comments → "subscribe, see you next time".

**OUR 13–15 min structure (≈2,100 words at 150 wpm):**

| # | Section | Time | Words | Must contain |
|---|---|---|---|---|
| 0 | **Cold open + catchphrase** | 0:00–0:10 | 15 | 6–10 fast clips (0.4–1s each), catchphrase, "I'm {NARRATOR}", subscribe line |
| 1 | **Hook** | 0:10–1:20 | 170 | Striking image + question → news fact with numbers → one hand/other hand → "actually, the opposite" → expert quote → **thesis question** |
| 2 | **Ch.1 Background** | 1:20–3:30 | 320 | Opens with a rhetorical question; origin, first sign he was special (or doomed); 3+ numbers |
| 3 | **Ch.2 Rise / key moment** | 3:30–6:00 | 380 | The breakthrough; best game/season stats; **open loop** ("but that's not what made him famous…") |
| 4 | **Ch.3 Deep breakdown** (longest) | 6:00–9:30 | 520 | Skill/tactic/decision analysis; 2 comparisons to famous players; slow-mo + freeze cues; **re-hook at ~40%** |
| 5 | **Ch.4 Conflict / turning point** | 9:30–11:30 | 300 | Injury, trade, controversy, quote war; answers the hook's first question |
| 6 | **Ch.5 Twist + counter-view** | 11:30–13:00 | 230 | "But here's what most people miss…"; strongest argument against our thesis; **re-hook at ~70%** |
| 7 | **Verdict + outro** | 13:00–13:50 | 140 | Clear opinion, a question for the comments, narrator sign-off line, next-video tease |
| 8 | End screen | 13:50–14:10 | 0 | 20s, 1 video + subscribe |

**Writing rules:**
- **One caption = one breath phrase.** The competitor speaks in phrases of 4–14 Chinese characters, each followed by a ~350 ms pause (43 phrases = 43 pauses in 72s).
  - English: 3–8 words per phrase, 1–2 phrases per sentence.
  - Write the script **one phrase per line**, so the voice, captions and shot list line up 1:1.
- A **specific number every ~20–30 seconds** (age, stat, money, date). Every number becomes a stat card (OURS).
- An **open loop every 60–90s**; a **rhetorical question at the start of every chapter**.
- At least **3 real quotes** per video (ex-players, coaches, the subject), each with a source link.
- The narrator says his own name in the third person 2–4 times. Use the same catchphrase and sign-off every video.
- **No invented facts or quotes.** Anything unverified is marked `[VERIFY]` and fixed before voicing.

### 1.5 Voice

**Competitor (measured from audio, 72s sample):**

| Property | Value |
|---|---|
| Gender / register | **Male, deep.** Median pitch ~108 Hz (10th–90th percentile 75–167 Hz) |
| Expressiveness | **High:** ~14 semitones of pitch range. Storytelling, not monotone |
| Pace | ~4.5 Mandarin characters/sec (≈150–160 English wpm equivalent) |
| Phrase rhythm | Short phrase → **~350 ms pause** (median); up to ~1.4s at idea changes |
| Speech density | Voice active ~71% of the time; the rest is short pauses |
| Level | Voice ~−17 dB RMS; very consistent (compressed/normalised) |
| Human or AI? | **Cannot be confirmed from the audio.** Sounds like a consistent single narrator, either a human or a good cloned voice |

**OUR voice spec:**
- Male, deep-to-mid, confident and slightly excited. "Sports storyteller", not "news anchor".
- 145–160 wpm English. Slow down on numbers and on the thesis question; speed up in montage moments.
- Pause **300–400 ms between phrases**, **800–1200 ms before a twist or a chapter change**.
- AI voice options: ElevenLabs, Fish Audio or similar. Pick one voice and **never change it** (consistency = brand).
  - Starting settings (ElevenLabs-style): stability 40–50%, similarity 75–80%, style 15–30%, speaker boost on.
  - Generate **one paragraph at a time**, listen, and regenerate any line with a wrong emphasis or a mispronounced name.
- Urdu/Hindi: use a native-speaker voice. Player names must still be pronounced the English way.
- Processing: high-pass 80 Hz, light compression, normalise to **−14 LUFS integrated** for the final mix.

### 1.6 Music & SFX

**Competitor:**
- Music is a bed **barely audible under the voice** (pauses drop to −37 to −48 dB against a voice at ~−17 dB, so the music sits ~20–28 dB below the voice).
- In the older video logged by AI there are **3 moods**: upbeat hip-hop (intro/context), emotional piano (childhood/struggle), lo-fi hip-hop (analysis to end).
- **SFX: almost none.** At most 1–2 in the intro (impact on the subscribe text).
- **Game/crowd audio: muted.**

**OUR rules (better):**

| Section | Music mood | Level |
|---|---|---|
| Cold open (0–10s) | Hard-hitting hip-hop/trap hit | Loud (−18 LUFS) under the catchphrase, then duck |
| Hook | Tense, pulsing | Voice −14 LUFS, music −34 to −36 LUFS |
| Background/origin | Emotional piano / soft keys | same ratio |
| Rise / highlights | Upbeat hip-hop | same; **swell +4 dB in pauses and montages** |
| Deep breakdown | Lo-fi / minimal beat (doesn't distract) | slightly lower |
| Conflict / twist | Dark, tense, riser before the twist | same |
| Verdict / outro | Uplifting or reflective | fades out under the end screen |

- **Sidechain ducking:** music drops automatically while the voice speaks.
- **SFX (OURS):** soft whoosh on chapter wipes; pop/click on stat cards and name tags; riser (1–2s) before twists; camera-shutter on photo reveals.
  - At most **1 SFX every 20–30s**, 6–10 dB under the voice. Never on top of key words.
- **Game audio: always muted** (copyright + clarity).
- Music sources: YouTube Audio Library (free), Epidemic Sound or Artlist (paid, claim-safe). Never use popular songs.

### 1.7 Visuals — clips, photos, graphics

#### STRICT CLIP RULE

> **Every video clip on screen is 4.0 seconds or shorter. No exceptions.**
> The competitor's older videos held clips up to 13s; its newest holds game clips at ~3.2s. We cap at 4s regardless.

How to cover a long sentence without breaking the rule:
1. Chain 2–3 **different** clips (different games/angles), each 2–4s.
2. Put a photo (3.5–5.5s, zoom) or an animated graphic in between.
3. In breakdown sections, slow a 2s moment to 60–70% speed. It can play up to 4.0s on screen, never more.
4. **Never reuse the same clip** in one video.

#### Screen-time split and shot budget

| Type | Competitor (newest, measured) | **OUR target** | Length per shot |
|---|---|---|---|
| Game clips | ~32% (8 × 3.2s in 82s) | **~45%** | 2.5–4.0s |
| Candid/interview/press clips | ~26% (4.3–6.0s) | **~15%** (cut to ≤4s) | 2.5–4.0s |
| Still photos | ~27% (4.7–6.6s) | **~25%** | 3.5–5.5s |
| Animated graphics (stat/name/quote/chapter cards, PiP, maps, comparisons) | ~5% | **~15%** | 2–4s |

**Shot budget for one 14-minute video (~840s):**
- **~150–160 clips** (game + candid), all ≤4s
- **~45–55 photos**
- **~30–40 animated graphics**
- **Total ≈ 230–250 shots**, i.e. a new visual every ~3.5s

| Section | Visual recipe |
|---|---|
| Cold open | 6–10 fastest highlight clips (0.4–1s each), dunks/blocks, hard cuts on the beat |
| Hook | Striking photo with blurred background → 2 candid clips → 4–6 game clips → quote card + interview clip → PiP composite on the thesis question |
| Background | More photos (childhood, college, early career), each with a slow zoom; dissolves between them |
| Rise | Mostly game clips (≤4s), stat card on every number |
| Deep breakdown | Game clips in slow-mo (≤4s), **freeze frame + ring/arrow on the player**, split-screen comparison with the famous player |
| Conflict / twist | Press/interview clips (≤4s), headline/tweet screenshots recreated as clean cards, dip-to-black before the twist |
| Verdict | Best emotional photo, slow push-in; final montage of 4–6 clips; end screen |

#### Photos

- Photo not 16:9? Place it centred on a **blurred, enlarged copy of itself** (competitor does this).
- Every photo moves: slow zoom-in 100%→108% or a slow pan. Use zoom-out only for comparisons/reveals.
- Prefer press/agency photos, player social media and team media. Avoid watermarked images.

### 1.8 Text on screen — where, what, how

| Text element | Competitor | **OUR rule** | Style |
|---|---|---|---|
| **Subtitles / captions** | Burned in, **100% of narration**, new caption every ~1.7s, one line, 4–14 chars | **Same, 100% of narration.** One phrase per caption (3–8 English words), changes with each phrase | Bottom-centre, ~6% of frame height, bold sans (e.g. Montserrat ExtraBold / Noto Sans Bold), white with 4–6px black outline + soft shadow. **Highlight 1 keyword per caption** in brand colour (OURS) |
| Brand badge / watermark | `澤北SG` on a yellow tab, top-left, every frame | Logo badge top-left, every frame | Small, ~4% height, brand colour |
| Border frame | Yellow border on every frame | Brand-colour border on every frame | Thin, constant |
| Big centre text | Only once: intro subscribe call-to-action + hand-drawn arrow | Intro subscribe line only (+ arrow) | Big, bold, pop-in with bounce |
| **Text on photos/images** | **None.** Photos never carry labels | **OURS:** a **name tag** the first time a person appears (lower third, 2.5s) | Slide in from left, brand colour bar + white name + small role text ("Ex-NBA guard") |
| **Numbers / stats** | Only inside subtitles | **OURS:** a **stat card** for every important number (e.g. `34 REB`, `$40M`, `41 vs 21`) | Big number + small label, pop-in + count-up animation, 2–3s |
| **Quotes** | Spoken + subtitles only | **OURS:** a **quote card** (photo of the speaker + quote text) | 3–4s, typewriter or fade-in |
| Chapter titles | None | **OURS:** a 1.5s **chapter card** at each chapter start (matches YouTube chapters) | Full-screen wipe in brand colour + chapter title |
| Tactic markup | None (old video: arrows in intro only) | **OURS:** ring/spotlight on the player, arrows for movement, during freeze frames | Hand-drawn style, animated stroke |
| Outro text | None (just subtitles) | Comment question shown as a big text card for 3s | Same as stat card style |

**Golden rule:** at most **2 text elements on screen at once** (subtitle + one graphic). Never cover the player's face or the ball.

### 1.9 Transitions & animation

| Where | Competitor | **OUR rule** |
|---|---|---|
| Clip → clip (same idea) | Hard cut | Hard cut, on the beat where possible |
| Photo ↔ photo / idea change | Cross-dissolve (~0.5s) | Dissolve 0.3–0.5s or a quick zoom-through |
| Before a big reveal | Dip to black (0.2s) | Dip to black + riser SFX |
| Section change | Watercolour basketball wipe (intro), pixelate (later) | **One branded wipe** (logo/ball shape) used every chapter |
| Composite moments | Circle **picture-in-picture** over a bigger photo | Use PiP for "X vs Y", "then vs now", "father vs son" moments |
| Motion on stills | Slow zoom-in | Slow zoom/pan + **parallax** (cut-out player over blurred background) on 3–5 key photos |
| Freeze frame | Not seen in measured video | **OURS:** freeze + ring + slow zoom on key plays (breakdown chapter) |

**Animation toolkit (OURS, build once as templates):** name tag, stat card, quote card, chapter card,
split-screen comparison, PiP circle, ring/arrow markup, branded wipe, subscribe pop-up, end screen.
Tools: CapCut / Premiere Pro (Essential Graphics) / After Effects / Remotion. Make them templates and only change the text.

### 1.10 Brand elements

- **Intro (≤10s, every video):** fast highlight montage + catchphrase + "I'm {NARRATOR}" + "subscribe…" big text with an arrow + branded wipe into the hook.
  - The competitor's intro is 9.4s and identical in every video.
- **Constant frame:** brand border + logo badge on every frame.
- **Outro:** comment question → sign-off line ("{NARRATOR} is off to play ball, see you next time") over 3–4 clips → 20s end screen.
- One brand colour plus white and black. Keep it the same across video, thumbnails and the channel banner.

### 1.11 Copyright safety (strict)

- Game clips **≤4s**, **game audio muted**, always under **commentary**, mixed with photos and graphics.
- Our story and analysis must be the main value, not the footage.
- Don't upload long uncut sequences or full plays with broadcast audio. Don't use popular music.
- Check claims in YouTube Studio before publishing. Fix anything claimed by replacing that clip.
- This lowers the risk; it does not remove it.

---

## PART 2 — Pipeline with AI prompts

```
[1] Find viral topic → [2] Score → [3] Titles (A) → [4] Research pack → [5] Script + shot list + captions (B)
→ [6] Voice → [7] Edit (Part 1 rules) → [8] Thumbnail (later) → [9] Description/chapters (C) → [10] Publish & review
```

**Config (fill once):**

```
NICHE        = NBA / basketball player stories
LANGUAGE     = English            # or Urdu / Hindi …
LOCAL_ANGLE  = <who your audience feels close to>
CHANNEL_NAME = <brand>    NARRATOR = <narrator name>
CATCHPHRASE  = <fixed intro line>    SIGNOFF = <fixed outro line>
BRAND_COLOR  = <hex>
LENGTH       = 13:00–14:59 (≈2,100 words)
CLIP_MAX     = 4.0 seconds (strict)
```

### 2.1 Find viral topics (NexLev + free sources)

| Goal | NexLev tool | Settings |
|---|---|---|
| Competitor's proven topics | `youtube_channel_outliers` | channel `UC7A3Mbc2g61ccaOg6kvSw7A`, `max_videos=500`, `min_outlier_threshold=1.5` |
| Competitor's all-time top | `youtube_channel_videos` | `sort_by=popular` |
| Viral NBA videos from small channels | `search_videos` | `query="NBA"`, `minOutlierScore=3`, `minLength=10:00`, `maxSubCount=500000`, last 6 months, `sortBy=outlierScore` |
| Breakouts from tiny channels | `search_viral_videos_small_channels` | `query="NBA"`, `maxChannelSubCount=50000`, `minVideoLengthSeconds=600` |
| What YouTube is pushing now | `search_youtube_suggested_videos` | `isFromHomeFeed=true`, `query="NBA"`, `minOutlierScore=2` |
| Faceless outliers by meaning | `faceless_outliers_videos` | `query="NBA player downfall story"`, `videoType=long`, `minOutlierScore=3` |
| More competitors | `get_similar_channels` | competitor channel, `level=3` |

- **Translate other-language outliers** (Chinese, Spanish, Portuguese NBA channels). A topic that went viral in one language is usually untapped in yours.
- Save every candidate to a NexLev Swipefile folder (`NBA – Title Bank`).
- Free sources:
  - News pegs: ESPN, The Athletic, Shams Charania on X, r/nba.
  - Evergreen stories: Basketball-Reference, Wikipedia "List of…" pages.
  - Demand check: Google Trends.

**Topic score — keep only ≥18/25** (1–5 each):
- proven demand (source outlier score);
- curiosity/mystery;
- emotion (underdog, downfall, rivalry, injustice);
- local/audience angle;
- story depth (enough for 13–15 min).

**Content buckets that won for the competitor:**
- A: Banned / too strong
- B: Undersized underdog / local-Asian player
- C: Bust or downfall mystery
- D: Hot news explainer (publish within 24–72h)
- E: Legend peak breakdown

Evergreen topics (A/B/C/E) produced every 1M+ video; plain game recaps flopped (11K–54K).

### Prompt A — Titles

```
Use VIDEO_PIPELINE.md Part 1.3. Topic: {topic}. Source video(s) that went viral: {titles + outlier scores}.
Language: {LANGUAGE}. Write 10 titles using the 10 formulas (55–75 chars, name + hook in first 40 chars,
one shock fact/number + one open question, never answer the question). For each, add 2–4 word thumbnail text
that adds a second layer (not a repeat). Score each on clarity/curiosity/emotion (1–5) and recommend the best.
```

### Research pack (before writing; ~45 min)

1. Timeline: 8–15 key dates.
2. 12+ hard numbers.
3. 3–6 real quotes with source links.
4. 3–5 turning points.
5. 2 comparison players.
6. The strongest counter-argument.
7. Source list.

**No source = not in the script.**

### Prompt B — Script + shot list + captions (the main one)

```
Use VIDEO_PIPELINE.md Part 1 (all rules) and the config below.
TITLE: {title}   THUMBNAIL TEXT: {thumb}   LANGUAGE: {LANGUAGE}
NARRATOR: {name}  CATCHPHRASE: {line}  SIGNOFF: {line}
RESEARCH PACK (use only these facts; mark anything else [VERIFY]): {paste}

Output 4 things:

1) SCRIPT — 13–15 min (≈2,100 words), structure from Part 1.4 sections 0–8 with timestamps.
   Write ONE BREATH PHRASE PER LINE (3–8 words). Rhetorical question at each chapter start,
   number every 20–30s, open loop every 60–90s, re-hooks at ~40% and ~70%, narrator 3rd-person 2–4 times.

2) SHOT LIST — a table, one row per phrase:
   | # | start | end | phrase (caption) | visual type (CLIP ≤4s / PHOTO / GRAPHIC) |
   | exact visual + search keywords (game, date, play) | on-screen graphic text (name tag / stat card /
   quote card / chapter card / none) | transition | music mood | SFX |
   Rules: every CLIP ≤ 4.0s (split longer moments into several different clips), screen time ≈ 60% clips /
   25% photos / 15% graphics, new visual every 3–4s, no clip reused, game audio muted.

3) CAPTIONS — SRT file, one phrase per caption, timed at ~150 wpm with 0.35s gaps, and the 1 keyword
   per caption to highlight in brand colour written in **bold**.

4) CHECK — total words, estimated runtime, count of clips/photos/graphics and their % of screen time,
   longest clip (must be ≤4.0s), list of [VERIFY] items.
```

### Voice step

- Feed the script **paragraph by paragraph** to the TTS voice (Part 1.5 settings).
- Fix names and numbers by spelling them out ("forty-one", "Antetokounmpo" → phonetic if needed).
- Export WAV, then normalise to −14 LUFS.
- Re-time the SRT to the real audio (CapCut auto-captions or Whisper, then paste our phrase breaks).

### Edit step

- Follow the shot list and Part 1.7–1.10. Build the 10 animation templates once and reuse them.
- Final check before export:
  - longest clip ≤4.0s;
  - subtitles on 100% of narration;
  - game audio muted;
  - music ducked under the voice.

### Thumbnail — *later (to be designed next)*

Competitor notes so far:
- One high-action player shot on the right.
- 2-line bold text on the left (nickname + question).
- High saturation; jersey colours.
- Text adds to the title instead of repeating it.

### Prompt C — Description, chapters, tags

```
Use VIDEO_PIPELINE.md. From this script + timestamps write: (1) a 2-sentence hook restating the title question
with player name + keyword, (2) chapters list from the section timestamps, (3) a 3-sentence summary with natural
keywords, (4) "Sources:" list, (5) 3–5 hashtags only, (6) 10–15 tags (player, nickname, teams, "NBA story", era).
```

The competitor has no chapters, no captions and ~80 hashtags. More than 60 hashtags makes YouTube ignore all of them.
Our chapters + captions + 3–5 hashtags are an easy win.

### Publish & review

- Publish at a fixed time.
- At 48h and 7 days, check NexLev (`get_my_video_analytics`, `get_my_audience_retention`, `get_my_traffic_sources`).
- Log each video: title, bucket, length, CTR, average view duration %, 7-day views.
- Every 10 videos, double down on the best bucket.
- Targets:
  - CTR ≥ 6%;
  - average view duration ≥ 40% on 13–15 min videos;
  - 30-second retention ≥ 70%.

---

## PART 3 — Final QA checklist (before upload)

- [ ] Length 13:00–14:59
- [ ] **Every clip ≤ 4.0s** (check the timeline), no clip reused
- [ ] Screen time ≈ 60/25/15 (clips/photos/graphics); new visual every 3–4s
- [ ] Subtitles on 100% of narration, one phrase each, keyword highlighted, nothing covering faces/ball
- [ ] Name tag on every person's first appearance; stat card on every key number; quote cards for quotes
- [ ] Hook ends with a clear thesis question by ~1:20; every chapter opens with a question
- [ ] All facts/quotes sourced; zero `[VERIFY]` left
- [ ] Voice −14 LUFS; music ducked 20–24 dB under the voice; game audio muted; SFX ≤ 1 per 20s
- [ ] Brand border + badge on every frame; intro ≤10s; outro + 20s end screen
- [ ] Description with chapters, sources, 3–5 hashtags; English SRT uploaded

---

## PART 4 — Competitor evidence (appendix)

### 4.1 Channel snapshot (NexLev, 2026-10-01)

| Metric | Value |
|---|---|
| Channel | 澤北SG (@Sawakita), `UC7A3Mbc2g61ccaOg6kvSw7A` |
| Subscribers / views | 193K / 172.5M |
| Videos | 1,187 since Sep 2022 (~1/day) |
| Average views | ~145K per video |
| Length | 10:02–12:19 recently (older: 9–14 min) |
| Format | Faceless; no Shorts; no captions uploaded; Traditional Chinese |

### 4.2 Top videos and outliers

**All-time:**
- 1.3M: the most heated All-Star game
- 1.2M: tactics banned for being too strong
- 734K: Tacko Fall
- 661K: blocked super-trade
- 645K: Embiid soft in the playoffs
- 575K: Dwight Howard joins the Taiwan league
- 548K: Cooper Flagg
- 540K: Yuki Kawamura, 172cm
- 519K: champion at 23, gone at 26
- 513K: Anthony Bennett bust
- 502K: Yuta Tabuse, 175cm

**Recent outliers:**
- 3.0x: Chen Ying-chun, a Taiwanese guard
- 2.1x: Wembanyama playoffs
- 2.1x: Ben Simmons return
- 2.1x: LeBron to the Warriors?
- Middle era: 2.3–2.6x for news with a shock stat (Kawhi, Luka, Butler, SGA, Whiteside)

**Evolution:**
- Early game recaps flopped (11K–54K); early evergreen stories exploded.
- Titles grew from ~50 to ~70–90 characters and settled on the 5-part formula.
- Length settled at just over 10 minutes.

### 4.3 Measured video (ffmpeg, exact): `AOJFfj-ijfc` (Bronny James), first 82.5s

| Time | Len | Type | On screen | Transition | Text |
|---|---|---|---|---|---|
| 0.0–3.2 | ~0.5s ×6 | Game clips | Dunk/drive montage | Hard cuts | Catchphrase `人在家中躺 球技心中漲` |
| 3.2–6.4 | 1.5–1.7s ×2 | Game clips | Drive, dunk | Hard cut | `大家好` / `我是做夢都在打球的澤北SG` |
| 6.4–8.5 | 2.1s | Game clip | Bronny vs Nets | Hard cut | **Big centre** `訂閱頻道 一起變強！` + arrow |
| 8.5–9.4 | 0.9s | Graphic | Watercolour basketball wipe | — | — |
| 9.4–16.0 | 6.6s | Photo | Studio composite, blurred-background fill, zoom | Wipe | "Looking at this photo…" |
| 16.0–28.0 | 6.0s ×2 | Candid clips | LeBron + Bronny courtside | Cross-dissolve | Ages 41 / 21 |
| 28.0–40.7 | **3.1–3.2s ×4** | Game clips | 4 different games | Hard cuts | Narration subtitles |
| 40.7–45.0 | 4.3s | Candid clip | Thanasis (comparison) | Hard cut | |
| 45.0–61.0 | 4.7–5.9s ×3 | Photos | Bronny press conf / ball / smile, slow zoom | Dissolves | |
| 61.0–66.2 | 5.2s | Interview clip | Jason Williams (quote source) | Hard cut | "Ex-NBA player…" |
| 66.2–66.4 | 0.2s | — | Dip to black | | |
| 66.4–79.5 | **3.2–3.3s ×4** | Game clips | 4 different games | Hard cuts | |
| 79.5–82.5 | 3.0s | Graphic composite | LeBron (76ers) + Bronny + **circle PiP** | Pixelate | Thesis question |

**Totals:**
- Screen time: 68% video, 27% photos, 5% graphics.
- **8/8 game clips were 3.1–3.3s.**
- 43 captions in 72.5s (one every 1.7s).
- Voice: male, median 108 Hz, ~350 ms pauses.
- Music 20–28 dB under the voice; game audio muted.

### 4.4 AI-logged full video (estimates): `1vemBPHJE9I` (Chen Ying-chun, 10:18, 3x outlier)

**Overall:**
- ~104 shots: ~54% clips / ~44% photos / ~2% graphics.
- By time: ~51% clips / ~49% photos.
- Average clip ~5.6s (max 13s); average photo ~6.6s.

**Structure:**
- 0:00–0:08 intro;
- context/news to 1:35;
- backstory to 3:50;
- rise to 5:30;
- skill breakdown to 9:50 (with comparisons: "Taiwan's Chris Paul", Brunson);
- verdict + comment question + sign-off.

**Music:** upbeat → emotional piano (backstory) → lo-fi (analysis).

**Other:**
- Slow-mo clips in the breakdown.
- Subtitles 100% of the time.
- Yellow border + badge on every frame.
- 18s still photo as the end screen.

### 4.5 Similar channels

- 阿尚聊球 `UCZSTzBJTSboY5AyE2Qz_rdQ`: a new clone of the format.
- 球迷聊球 `UCi8eTvI6AhasDg493CmlzDA`.
- 卡酷籃球 `UCMhUlIthPNcOO5smWmiZxGg`: 926K views in 97 days with 13-min breakdowns.

**English outliers (small channels):**
- "How Australia's Greatest Player Became an NBA Footnote" (80x)
- "When the NBA was truly scary…" (59x)
- "I Built a Model to Find the Most Average NBA Player" (99x)

### 4.6 Ready-made first topics

- *The NBA Banned These Plays for Being Too Good* (A, source 1.2M)
- *5'8" and in the NBA?! How Yuki Kawamura Proved Everyone Wrong* (B, 540K)
- *Champion at 23, Gone at 26: The Andrew Bynum Mystery* (C, 519K)
- *The Most Violent All-Star Game in NBA History* (A/E, 1.3M)
- *Tacko Fall Broke 3 Combine Records. Why Did He Last Only 37 Games?* (C, 734K)
