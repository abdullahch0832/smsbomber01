# "Post-Game Reveal" Baseball Video System (based on 大谷しか勝たん)

> **What this file is:** a standalone pipeline for making **20–30 minute** faceless videos in the style of the
> Japanese channel **大谷しか勝たん** ("Only Ohtani Wins"): Shohei Ohtani / Dodgers post-game stories built around
> "what player X said right after the game".
>
> **How to use it:** paste this whole file into Claude (or another strong AI model) and say:
> *"Use OHTANI_PIPELINE.md. Game/topic: ___. Language: ___. Give me outputs A → E."*
>
> **Data:** NexLev on 2026-10-02.
> - 56 outlier videos.
> - 60 recent and popular titles.
> - 3 full transcripts (~16, ~21 and ~26 min).
> - An AI shot-by-shot watch of 2 videos (one 2025, one 2026).
> - 15 similar channels.

---

## PART 0 — Read this first: what the competitor does that we must NOT copy

The competitor's videos are built on **"interviews" that very likely never happened**:

1. Every title claims a player's words were **"revealed in a US media interview"** (`米メディアの取材で明かし`, in 50 of 53 outlier titles).
2. The "answers" in the transcripts are **long, chatty first-person monologues** that don't read like real post-game quotes.
   - Example: Blake Snell supposedly talks for minutes about a "family tree" with Yamamoto, Ohtani and Skubal.
3. In the 2026 video, the AI watch found the answers **voiced by AI voices made to sound like the players**,
   played over real press-conference footage of those players. An **AI-generated news anchor** asks the questions.
4. Several channels in the same niche admit in their descriptions that videos contain **"prediction and fiction"** (予想とフィクション).

**Why we don't copy this part:**
- Putting invented words in real people's mouths with realistic AI voices breaks YouTube's rules on misleading content.
  It also requires YouTube's **altered/synthetic content disclosure**.
- It risks impersonation and defamation complaints from the players or teams.
- YouTube can demonetise channels for **mass-produced, inauthentic content**.
- The competitor uploads up to **9 near-identical videos in one day**. That is the exact pattern that gets channels hit.

**What we copy instead, with the same emotional pull:**

| Competitor element | **Our version** |
|---|---|
| Invented "US media interview" | **Real post-game quotes** (press conferences, team media, beat reporters), translated, with the source named on screen |
| AI voice pretending to be the player | **Narrator reads the quote:** "Snell told reporters: '…'". Or the real clip with real audio, ≤ a short excerpt, with subtitles |
| AI news anchor asking fake questions | Narrator sets up each quote with the **real question asked** (from the press-conference video) or a framing line |
| Invented "legend" reactions (Smoltz etc.) | Real broadcaster or analyst quotes from the actual broadcast or articles, sourced |
| Invented overseas fan reactions | **Real fan reactions** from r/Dodgers game threads, X/Twitter and YouTube comments (paraphrased, no usernames) |

Everything else (topic choice, title psychology, story structure, pacing, editing, upload rhythm) is copied and improved below.

---

## PART 1 — Competitor teardown

### 1.1 Channel snapshot

| Item | Value |
|---|---|
| Channel | 大谷しか勝たん, `UC1C2FvyrUf8meDbpuTWTlkA`, Japan |
| Started | 11 Apr 2025 (≈18 months old) |
| Subscribers / views | 21.6K / 20.5M |
| Videos | 338. Average ≈0.6 per day, but in bursts (9 uploads on 18 Sep 2026) |
| Average views (NexLev) | ~60.6K per video |
| Length | 2025 videos: **14–19 min**. 2026 videos: **20–26 min** (average 22:07) |
| Language | **Japanese** voice and subtitles |
| Niche | Shohei Ohtani + Dodgers teammates (Yamamoto, Sasaki, Snell, Glasnow, Kershaw, Betts, Freeman…) |
| Category | People & Blogs (not Sports) |

The views have a **huge subscriber-to-view ratio** (20.5M views on 21.6K subs). The channel lives on **browse and suggested** traffic from Ohtani fans, not on its subscribers.

### 1.2 Outliers (56 videos ≥1.5× the 60.6K average)

| Score | Views | Length | Topic (translated) |
|---|---|---|---|
| **11.4x** | 690K | 16:27 | After HR #52, Kershaw's wife Ellen and kids visit Ohtani… Ohtani's "heart-touching words" |
| **10.6x** | 644K | 18:24 | HRs #2 and #3, a foot injury, the 18-inning game… Ohtani's "one line" to interpreter Ireton |
| **10.3x** | 622K | 14:30 | After a revenge hit-by-pitch, Darvish's furious words to Suarez |
| **10.2x** | 619K | 25:40 | Angry Ohtani throws 164 km/h repeatedly… what Betts, Freeman and others "really thought" |
| **10.1x** | 610K | 18:12 | Yamamoto's emergency relief, World Series MVP… what Snell, Kershaw and Glasnow said |
| 9.1x | 552K | 15:24 | Ohtani pulled in the 7th… teammates' true feelings |
| 8.4x | 508K | 16:19 | Gave up a 3-run HR; Ohtani's words to the interpreter behind the bench; Dodgers win the title |
| 6.5x | 396K | 15:49 | Yamamoto's first complete game |
| 6.3x | 379K | 18:54 | HRs 1–3 plus scoreless pitching (the "two-way" game) |
| 6.1x | 369K | 14:05 | Revenge HBP, Darvish confronts Machado, Roberts ejected |
| 5.4x | 327K | 16:56 | *(English title)* Lux and his fiancée visit Ohtani after the game |
| 3.6x | 216K | 20:42 | (Sep 2026) Ohtani–Yamamoto argument after Yamamoto leaves the game; Snell: "these two are a handful" |
| 3.1x | 190K | 21:34 | (Sep 2026) Same argument, told from the pitching coach's angle |

**What the outliers have in common:**
1. **Emotion + family/relationship angle.** Wives, kids, interpreter, trainer, "brothers" Snell/Yamamoto. 9 of the top 10 are about **relationships**, not stats.
2. **Conflict or anger.** Revenge hit-by-pitch, "angry Ohtani", arguments between teammates, umpire controversy.
3. **Big moments.** Milestone home runs (#37, #44, #45, #52), the 50-50 season, postseason and World Series games, MVP awards.
4. **Kershaw's farewell and the 2025 postseason (Oct–Nov 2025)** produced the biggest wave: 7 of the top 10. **Big events = big views.** Plan around the calendar.
5. **One story, several teammates' views.** Titles list 2–4 players ("Snell, Kershaw, Glasnow and Ohtani said…").
6. **English titles also work.** 3 English-titled re-uploads scored 2.9–5.4x, so the format travels across languages.

**Recent trend (last 30 uploads):**
- Most videos got 10K–90K views.
- Only the Ohtani–Yamamoto "argument" story broke out (190K–216K).
- Volume without a strong emotional hook doesn't work. **Fewer, better stories** beat 9 uploads a day.

### 1.3 Title formula (measured on 53 Japanese outlier titles)

```
【大谷翔平】 + [THE MOMENT: game event + number] + 直後に + [WHO: 1–4 named people] + が放った
+ “まさかの一言 / 本音 / 第一声 / 胸を打つ発言” + を米メディアの取材で明かし + [EMOTION WORD] (+ レジェンド○○)
```

| Element | Frequency |
|---|---|
| Starts with `【大谷翔平】` (name in brackets) | 53/53 |
| Hook in Japanese quote marks `“…”` (the unexpected words/action) | 53/53 |
| `明かし` ("revealed") | 53/53 |
| Ends with an emotion word | 52/53 |
| `米メディアの取材` ("in a US media interview") | 50/53 |
| `直後` ("right after") | 45/53 |
| `まさか` ("unexpected / no way") | 38/53 |
| A number (home run #, km/h, strikeouts, inning) | 35/53 |
| `一言 / 第一声 / 発言` (one line / first words / remark) | 34/53 |
| `レジェンド○○` ("legends react") | 32/53 |
| Several people listed with `、` | 20/53 |

- **Emotion words used:** 感涙 (moved to tears) 30, 驚愕 (shocked) 22, 号泣 (sobbing) 9, 驚嘆 (amazed) 9, 困惑 (confused) 5, 大興奮 (thrilled) 5.
- **Length:** 53–99 Japanese characters (median 71).
- **Newest variant (2026):** puts a short quote right in the title (`「この二人は面倒だよ」`) and asks for the "real reason" (“本当の理由”). This variant produced the latest outlier.

### 1.3b Title evolution (oldest 30 vs outliers vs newest 30)

| Period | Title style | Views |
|---|---|---|
| **First ~30 videos (spring 2025)** | `…“ある発言”がヤバすぎる…米メディアが明かした内容とは` ("…X's certain remark is crazy… what US media revealed"), `“本当の理由”` ("the real reason"), `涙が止まらない` ("can't stop crying"); 12–15 min | **15 to 2,100 views.** Almost everything flopped |
| **Breakthrough (mid 2025 →)** | `[big moment]直後に[name]が放った“胸を打つ発言”を米メディアの取材で明かし感涙 レジェンドら驚嘆` + a dramatic real event (revenge HBP, milestone HR, Kershaw's farewell, postseason) | 22K → **369K–690K** |
| **Now (Sep 2026)** | `[name]が放った“まさかの第一声 / 本音”を米メディアの取材で明かし驚愕`, plus the new "short quote in 「」 + “本当の理由”" variant; 20–25 min | Mostly 10K–90K; the argument story hit 190K–216K |

**Lesson:**
- The same formula only explodes when the **real event underneath is big and emotional**: a fight or HBP, a farewell, a milestone, the postseason.
- Vague teasers ("a certain remark is crazy") without a big event got almost no views.

### 1.4 Script structure (measured from 6 transcripts)

> The channel has used **two different script formats**. All of its 600K+ hits used **Format A**.

**Format A: "documentary narrative" (2025; every 600K+ video)**

Measured on `BThfQRMg-SM` (16:27, 11.4x), `39pqPFZhg0k` (14:30, 10.3x) and `ugpJrnU7K5I` (16:56, 5.4x).

- **Speed:** ~5.3 chars/sec.
- **Questions:** 0–2 in the whole video. It's told like a story, not an interview.

| Block | Time (example: BThfQRMg-SM) | What happens |
|---|---|---|
| 1. Cold-open quote | 0:00–0:02 | One emotional first-person line: "The whole family cried." / "That was an abnormal way to get angry." / "My girlfriend cried." |
| 2. Greeting + title read | 0:02–0:16 | "Hello everyone. Today's topic is [the full title]. Let's get started right away." |
| 3. **Cinematic recap** | 0:16–2:30 | Scene-setting like a film: "Dodger Stadium was wrapped in a special atmosphere that day…". Inning by inning with numbers, building to *the moment* |
| 4. Clubhouse scene | 2:30 | "After the game, in the quiet clubhouse, [name] appeared… as reporters held out their microphones, he slowly opened his mouth." |
| 5. **Speaker 1** (the emotional centre, e.g. Kershaw) | 2:30–8:00 | Quote → narrator stage direction ("his voice trembled slightly", "he wiped tears with his finger") → quote. Repeated, building to a final line |
| 6. **Speaker 2** (Ohtani) | 8:00–10:10 | Same pattern; Ohtani's quotes are humble and thankful |
| 7. **Speaker 3** (`さらに…`, e.g. interpreter or trainer) | 10:10–12:10 | The "insider who saw it up close" |
| 8. **Speaker 4** (manager Roberts) | 12:10–13:30 | Authority view |
| 9. **Legend** (a broadcaster/ex-player such as John Smoltz or Alex Rodriguez) | 13:30–15:30 | "Even he, with tears in his eyes, squeezed out the words…" |
| 10. **"Overseas reactions"** | 15:30–16:00 | `海外では…との声が寄せられています` ("Overseas, people are saying…") + 5–8 short fan comments |
| 11. Fixed outro | 16:05–16:27 | "Keep watching Ohtani and the Dodgers. That's today's news. Thanks for watching to the end. Please subscribe and like. See you in the next video." |

- **Link words between speakers:** `さらに` (furthermore), `そして` (and then), `一方` (meanwhile), `試合後、…` (after the game…).
- Some videos add a **social-media ending**: "About an hour after the game, Ohtani quietly posted one photo on Instagram…".

**Format B: "Q&A interview" (2026)**

Measured on `svbPHJxnwFs` (25:40, 10.2x), `sKIlxzBPXdc` (20:42, 3.6x) and `jAVrbpAP7-o` (22:51, below average).

- **Speed:** ~5.8–6.6 chars/sec (faster).
- **Questions:** 28–36 per video. Answers are a median of ~190–250 characters (~35–45s).

| Block | Time (example: sKIlxzBPXdc) | What happens |
|---|---|---|
| 1. Cold-open quote | 0:00–0:05 | Casual first-person line, often a teaser: "Shohei, that one line bothered me. I feel he's still hiding something." |
| 2. **Short recap** | 0:05–0:45 | 40–60s only: the key numbers of the game |
| 3. **Double question hook** | ~0:45 | "So what did Ohtani say back? And why did that one line make the coach see a different side of Ohtani for the postseason?" |
| 4. **Speaker 1** | 0:45–6:20 | Introduced in one line: `試合後、[name]は[angle]を振り返り…語りました` ("after the game, X looked back on…"). Then 6–10 question → answer pairs |
| 5. **Speaker 2** (`一方、…`) | 6:20–14:50 | Same Q&A pattern, a different angle (e.g. "he watched what happened *after* their talk") |
| 6. **Speaker 3** (`最後に、…`) | 14:50–20:20 | Same pattern; often the most senior player (Betts, Freeman) |
| 7. Outro | last 15s | A question to viewers ("How do you see these two? Tell us in the comments") + like/subscribe |

- 3 speakers in 20 min, or **5 speakers in 25 min** (svbPHJxnwFs: Betts → Robleski → Freeman → Cole → Muncy, 3–8 min each).
- No greeting, no legend block, no "overseas reactions" block.

**Which format to use:**
- **Format A** for big emotional events: farewells, fights, milestones, the postseason.
- **Format B** only when there's a lot of real press-conference material (several players gave long answers).

### 1.4a Old notes from the first 3 transcripts

**Speed:** 5.3–6.6 Japanese characters per second (fast, news-reader pace). A 20-minute script is ~6,500–8,000 Japanese characters.

| Block | Time | What happens | Example (translated) |
|---|---|---|---|
| 1. **Cold-open quote** | 0:00–0:05 | The single most emotional line, in first person, before anything else | "My whole family cried." / "If you make Shohei angry, nobody can stop him." |
| 2. Greeting + title read *(2025 only)* | 0:05–0:20 | "Hello everyone. Today's topic is… [reads the title]. Let's get started." | Dropped in 2026 videos, which go straight to the recap |
| 3. **Game recap** | ~0:20–2:00 | Play-by-play with numbers: innings, km/h, strikeouts, HR number, score swings | "First inning: back-to-back 160 km/h… Betts's 300th career HR…" |
| 4. **The "why?" bridge** | ~2:00 | One question line + who will answer it | "Why didn't either of them back down? After the game, Snell revealed the reason." |
| 5. **Speaker 1, Q&A** | ~2–8 min | 6–10 question → long-answer pairs. Each answer 30–60s, conversational, with humour and emotion | Q: "You're close with Yamamoto, right?" A: "Yoshinobu is my brother…" |
| 6. **Speaker 2, 3, 4** | ~8–18 min | Linked with `一方、○○選手は…` ("Meanwhile, player X…"), each 3–5 min | Teoscar Hernández, Betts, Freeman, pitching coach Pryor, trainer Yada |
| 7. **Legend / overseas reactions** *(mostly 2025)* | last 2–3 min | A famous ex-player's "comment" + "Overseas, people are saying…" | John Smoltz "with a trembling voice…" |
| 8. **Outro** | last 20s | 2025: "That's today's news. Thanks for watching, please subscribe and like." 2026: a question to viewers, then the like/subscribe ask | "How do you see these two? Tell us in the comments." |

**Writing style:**
- Narration is formal news Japanese (です/ます).
- "Quotes" are casual first person, with humour ("my family tree keeps growing") and an emotional peak near the end of each answer.
- Each speaker block ends on a quotable summary line.

### 1.4b MEASURED: 2026 video frame by frame (ffmpeg) — `sKIlxzBPXdc`, first 4:14

> **This is the current style to copy.** It was measured from the downloaded video:
> - ffmpeg cut detection at 10 fps (subtitle zone ignored);
> - every second checked by eye on timestamped contact sheets;
> - motion inside each shot measured, to tell video from still photo;
> - voice pitch per shot;
> - loudness every 0.25s.

**Shot list (19 shots in 254s):**

| # | Time | Length | What's on screen | Type (measured) | Voice |
|---|---|---|---|---|---|
| 1 | 0.0–5.4 | 5.4s | Snell at the press-conference podium (NL Wild Card backdrop) | Real press video | **Player voice (deep, ~103 Hz)**: the cold-open quote |
| 2 | 5.4–11.1 | 5.7s | **AI news anchor** (grey-haired man, suit, purple tie, studio with baseball-player silhouettes) | AI video | Narrator (~150 Hz) |
| 3 | 11.1–16.5 | 5.4s | Ohtani and Yamamoto face to face in the dugout | **Still photo + slow zoom** | Narrator |
| 4 | 16.5–19.8 | 3.3s | Snell at the podium | Real press video | Player voice |
| 5 | 19.8–24.1 | 4.3s | Ohtani (#17) walking to bat | Real game video | Narrator |
| 6 | 24.1–29.6 | 5.5s | Yamamoto pitching vs Padres | Game shot, slowed / slow zoom | Narrator |
| 7 | 29.6–33.9 | 4.3s | Yamamoto at his locker (team-sponsor backdrop) | Real locker-room video | Narrator |
| 8 | 33.9–38.0 | 4.1s | Dodger Stadium at night, wide | Stadium shot, slow move | Narrator |
| 9 | 38.0–45.7 | 7.7s | AI anchor | AI video | Narrator: the "why?" bridge + first question |
| 10 | 45.7–58.9 | 13.2s | Snell at the podium | Real press video | Player voice |
| 11 | 58.9–72.0 | 13.1s | The same Ohtani–Yamamoto photo again | **Still photo + slow zoom (reused)** | Player voice |
| 12 | 72.0–74.1 | 2.1s | Snell at the podium | Real press video | Player voice |
| 13 | 74.1–77.2 | 3.1s | AI anchor | AI video | Narrator (asks the next question) |
| 14 | 77.2–134.7 | **57.5s** | Snell, Yamamoto and teammates at spring training | **Still photo + very slow zoom** | Player voice |
| 15 | 134.7–167.4 | 32.7s | Yamamoto smiling, Ohtani leaning in (dugout) | **Still photo + slow zoom** | Player voice (+ narrator question) |
| 16 | 167.4–179.8 | 12.4s | Snell at the podium | Real press video | Player voice |
| 17 | 179.8–223.2 | **43.4s** | Yamamoto pitching vs Padres (same shot as #6) | **Frozen frame + slow zoom** | Player voice |
| 18 | 223.2–240.7 | 17.5s | Yamamoto close-up on the mound | **Still + slow zoom** | Player voice |
| 19 | 240.7–254.5 | 13.8s+ | Ohtani batting | **Still + slow zoom** | Player voice |

**Totals for 254s:**

| By screen time | Share |
|---|---|
| **Still photos / frozen frames + slow zoom** | **~73%** (~186s, 7 shots) |
| Real press-conference / locker video | ~16% (~41s, 6 shots) |
| AI anchor | ~6.5% (~16.5s, 3 shots) |
| Real moving game/stadium video | ~3.3% (~8.4s, 2 shots) |

**Rhythm:**
- 19 shots in 4:14, so an average of **13.4s per shot**.
- The first 45s cut every ~4–6s.
- After 1:17 the shots are 30–57s long: one picture while the "answer" plays.
- Photos are **reused** (#3 = #11; #6 = #17).

**What the measurement shows, element by element:**

- **Language:** Japanese voice and Japanese subtitles on everything. Player names are written in katakana (スネル, ヨシノブ, 翔平).
- **Frame/border:** **none.** Footage is full-screen 16:9. No logo, no watermark, no channel badge.
  - An earlier AI watch reported a "blue frame with logos". Those were the sponsor logos on the press-conference backdrop, not a frame.
- **Subtitles:**
  - 100% of the time, bottom-centre, 1–2 lines.
  - Bold Japanese gothic font, **white with a thick black outline**. Each subtitle stays up for the whole sentence (2–6s).
  - The **cold-open quote (0:00–0:05) is in yellow** with a black outline. That's the only coloured subtitle in the sample.
  - The interviewer's questions use the same white subtitles, ending in `？`.
- **Other text:** **none.** No name plates, no titles, no stat cards, no chapter cards, no arrows or stickers.
  - Speakers are only identified by the narrator saying their name.
- **Voices: two AI voices.**
  - **Narrator / interviewer:** median pitch ~150–185 Hz, a clear news voice. It also asks the questions.
  - **"Player" voice:** deeper, ~95–117 Hz, casual first person. It "speaks" for Snell.
  - The player voice is matched to real press-conference footage of that player.
- **Transitions:** **hard cuts only.** No whoosh, fade or wipe was detected.
- **SFX:** **none** detected.
- **Music:**
  - The overall level sits ~17 dB under the voice. Pauses drop to −42 to −50 dB (106 short gaps, 47.5s in total).
  - So any music bed is **very quiet** and nearly disappears between sentences. Transcripts show `[音楽]` (music) marks ~13 times per video, i.e. short music stings between answers.
- **Game audio:** muted (only narration and voice are heard).
- **Motion:** every still photo has a **slow zoom-in** (Ken Burns). Long shots change only ~0.3–0.6 per frame, i.e. a barely visible drift.

**What this means for production:**
- The competitor's 2026 edit is **very cheap**: ~6 real press clips + 6–8 photos + 3 AI anchor shots per 4 minutes, all hard cuts.
- The "value" is entirely in the **script and the voices**, not the editing.
- Our edit can win easily with more visual variety: a new visual every 5–8s, real footage, name plates.

### 1.5 Editing style (AI watch of 2 videos)

| Element | 2025 style (`BThfQRMg-SM`, 11.4x) | 2026 style (`sKIlxzBPXdc`, 3.6x) |
|---|---|---|
| Opening | White-on-black **text card** with the cold-open quote (1s) | Real press-conference clip of the speaker, quote in subtitles |
| Host element | Small **AI anime-girl avatar**, bottom-left, during the greeting | **AI-generated news anchor in a virtual studio**, used for questions and bridges (2–7s each) |
| Title read | 14s **3D rotating baseballs** graphic with the full title as text | None |
| Footage | Real game clips (Kershaw pitching, Ohtani HR, family in the stands), **15–45s each**, some slow-mo | Real game/dugout/press clips **3–52s**; a long "answer" plays over one dugout clip |
| Photos | Few (1 in 4 min), slow zoom | Few (2 in 3 min, one reused) |
| Average shot | **~20s** | **~10s** |
| Frame | Cinematic black bars top and bottom | **Blue frame**, Dodgers logo top-left, MLB logo bottom-right |
| Subtitles | Bottom-centre, white with black outline, on 100% of speech | Same + **key phrases highlighted in yellow** |
| Voice | Male AI narrator; quotes read by the same voice | Male AI narrator + **different AI voice for each player** |
| Music | Emotional orchestral piano, low under the voice | Dramatic orchestral, low |
| SFX | Whooshes on transitions, **camera-shutter clicks** on photos/quotes (~12 in 4 min) | None in the first 3 min |
| Transitions | Cuts + whoosh | Hard cuts only |
| Game audio | Muted / faint crowd only | Muted |

Other channels in this niche say in their descriptions that they use **VOICEVOX** (a free Japanese TTS) for narration.

### 1.6 Description, tags, thumbnail

- **Description:** the full title repeated, then "Thanks for watching to the end! Subscribing, rating and commenting makes us happy!", then **3 hashtags**: `#大谷翔平 #ドジャース #mlb`. No sources, no chapters.
- **Tags:** the same 6 every time: 大谷翔平, mlb, ドジャース, 海外の反応, 野球, メジャー. No captions uploaded.
- **Thumbnails:** not analysed yet. Thumbnail images couldn't be opened from this environment (i.ytimg.com is blocked).
  Send 3–5 screenshots of their thumbnails and this section will be filled in.

### 1.7 Similar channels (NexLev)

| Channel | Subs | Views | Avg length | Note |
|---|---|---|---|---|
| やきゅうの時間 `UCaVRAnhIRiWfp-D_9LlpgrQ` | 21.9K | 22.5M | 9:23 | 5ch-thread style, VOICEVOX voice; says it includes fiction |
| 大谷翔平の1億ドルCHANNEL `UCchUeBDKwZE_i-AOwZ8YZ9Q` | 2.7K | 3.7M | 12:49 | Started Mar 2026; VOICEVOX; says it includes fiction |
| 大谷翔平の丸太小屋 `UCCP0G8srONMiVAE7ottEK1g` | 6.7K | 3.0M | 10:29 | Same template as above |
| ショータイムズ【大谷翔平 速報 海外の反応】 `UCRWnMrXwJjLXSZC1KKGbcAg` | 9.5K | 5.2M | **1:24:54** | Very long compilations |
| ドジャース大谷ch【海外の反応】 `UCDsyXHNuxvvMw85sekMuPFQ` | 5.0K | 1.1M | 1:34:24 | Compilations |
| MLB translation channel `UCB9Bptvb7Itd78R66pMKYvA` | 21.1K | 13.0M | 15:46 | **Translates real local broadcasts.** This is the honest version of the niche, and it works |
| 抹茶ラテ `UC0rNIfLINiXy4RDkiqRNMdA` | 47K | 71.3M | 7:36 | Fan channel, 5,589 videos |

The niche is crowded with templated Ohtani channels. **Being the trustworthy one** (real quotes, sources on screen) is a real advantage, not just a safety measure.

---

## PART 2 — Our production spec

### 2.1 Config (fill once)

```
LANGUAGE       = Japanese | English | Urdu | Hindi …   (competitor = Japanese; English titles also work)
MAIN_SUBJECT   = Shohei Ohtani + Dodgers (or another star with a huge fan base)
CHANNEL_NAME   = <brand>       NARRATOR_STYLE = calm news anchor, warm
LENGTH         = 20–30 min (sweet spot 20–24 min)
UPLOADS        = 1 per day max; 2 on big-event days. Never batch near-identical videos
BRAND_COLOR    = <hex>
```

### 2.2 Script structure (20–24 min ≈ 3,000–3,600 English words at 150 wpm, or ~7,000–8,000 Japanese characters)

| # | Block | Time | Content |
|---|---|---|---|
| 1 | **Cold-open quote** | 0:00–0:08 | The strongest **real** quote of the story, on screen + voiced by the narrator ("Snell, after the game: '…'") |
| 2 | **Hook line** | 0:08–0:30 | What happened, in one breath, plus the question this video answers ("So why did neither of them back down?") |
| 3 | **Game recap** | 0:30–3:00 | Key moments with numbers (inning, score, km/h or mph, strikeouts, HR #). Build up to *the moment* |
| 4 | **The moment** | 3:00–4:30 | The exact scene (argument, hug, injury, milestone) told slowly, with what cameras showed |
| 5 | **Voice 1: main quote source** | 4:30–9:00 | Real press-conference quotes, each set up by the real question or a narrator line, then **our explanation** of what it means |
| 6 | **Voice 2** (`Meanwhile, …`) | 9:00–12:30 | A second teammate/coach view |
| 7 | **Voice 3** | 12:30–15:30 | A third view (manager, catcher, trainer, opponent) |
| 8 | **Context / background** | 15:30–18:30 | Relationship history (how they met, past games, earlier quotes), stats that show why it matters |
| 9 | **Real fan & media reactions** | 18:30–21:00 | What US/Japanese media and fans said (sourced, paraphrased) |
| 10 | **Verdict + outro** | 21:00–22:30 | Our take, a question to viewers, like/subscribe |

**Rules:**
- **Only real quotes.** Each one needs a source (video link + timestamp, or article link). Translate faithfully. Shorten with "…", never add words.
- Not enough real quotes for 3 voices? Use **context, history and analysis**. Don't invent dialogue.
- Mark **opinion as opinion**: "We think…", "It looks like…".
- **Emotional beats:** one per voice block (gratitude, humour, frustration, respect). Put the most touching line at the end of each block.
- An **open loop every ~2 min** ("But Freeman noticed something nobody else did…").
- The title's promise must be paid off in the video. If the title says "Snell revealed the real reason", the real reason must be in Snell's real words.

### 2.3 Title formula (our version)

**Japanese (if LANGUAGE = Japanese):**
`【大谷翔平】[moment + number]直後に[名前]が語った“[real hook]”に[emotion]`

- Use `語った` (said) or `明かした` (revealed). Don't claim "US media interview" unless it really was one; name the real source if useful (`会見で` = at the press conference).
- Emotion word: 感涙 / 驚愕 / 号泣 / 驚嘆. Use it only if the content actually earns it.

**English:**
`Right After [Moment], [Player] Said THIS About Ohtani… (Teammates Reveal Why)`
`"[Short real quote]": What [Player] Told Reporters After [Moment] Will Move You`

**Rules:**
- Lead with the star's name.
- Include one number or milestone.
- One curiosity gap ("unexpected words", "the real reason").
- Keep it 55–80 characters (English) or 50–75 characters (Japanese).

### 2.4 Voice

- **Narrator only.** One consistent AI voice (Japanese: VOICEVOX or a licensed commercial TTS; English: ElevenLabs or similar). Calm, warm, news style. Japanese pace ~5.5–6 chars/sec; English ~150 wpm.
- **Never clone or imitate a real player's voice.**
- Quotes are read by the narrator with a slight change of tone, and introduced as "[Player] told reporters:".
- Or play the **real clip with the player's real voice** (a short excerpt) with translated subtitles.
- Any realistic AI visuals (e.g. an AI anchor): turn on YouTube's **"altered or synthetic content"** disclosure.

### 2.5 Editing spec

| Element | Competitor | **Ours** |
|---|---|---|
| Frame | Blue frame + team/league logos | Own brand-colour frame + channel logo. **Don't use team/MLB logos as branding** |
| Cold open | Text card or press clip | Black card with the real quote in large type + source line ("— Blake Snell, post-game press conference") + camera-shutter SFX |
| Quote display | AI anchor + AI-dubbed player | **Quote card:** speaker photo or press-conference still + translated quote text + source tag. Hold ~1s per 10 characters |
| Footage | Clips 3–52s | Real clips kept **short (≤5–8s each, mute the broadcast audio)**, mixed with photos, quote cards and stat cards. A long voice block = a new visual every ~5–8s |
| Subtitles | 100% of speech, white with black outline, yellow highlights | Same: 100% of narration, white + black outline, **1–2 key phrases per line highlighted** in brand colour |
| Name plates | None | Lower-third name + role on each speaker's first appearance |
| Stat cards | None | Score / km/h / strikeouts / HR # as pop-in cards in the recap |
| Music | Orchestral / emotional piano, low | Same moods, ducked under the voice: tense for conflict, piano for emotional quotes, uplifting for the outro |
| SFX | Whoosh + camera shutters (2025); none (2026) | Shutter on quote cards, soft whoosh between voice blocks, nothing over key words |
| Transitions | Hard cuts | Hard cuts inside blocks; a branded wipe + title card between voice blocks ("VOICE 2: Teoscar Hernández") |
| Visual pace | 10–20s per shot | **5–8s per visual** (they are slow here; this is our easiest win) |

### 2.6 Description, tags, chapters

- **Line 1:** the title.
- **Line 2:** one sentence summarising what was really said.
- **Chapters** (from the script blocks).
- **"Sources:"** list of press-conference videos and articles.
- **3–5 hashtags** (`#大谷翔平 #ドジャース #MLB` or English equivalents).
- **Tags:** star name, team, teammates in the story, the event ("World Series", "HR 52"), the language keyword ("海外の反応" for Japanese).
- Upload subtitles (SRT) and set the category to **Sports**.

### 2.7 Thumbnail (placeholder, to be finished after competitor thumbnails are analysed)

- Emotional face of the star or the quote's speaker.
- 2–6 big words with the emotion or hook.
- Brand frame.
- No fake quotes in quotation marks.

---

## PART 3 — Finding viral topics and titles

### 3.1 Where the stories come from (real sources)

| Need | Source |
|---|---|
| What happened in the game | MLB.com game recap & box score, Baseball Savant (velocity, exit velocity), team Gameday |
| **Real post-game quotes** | Dodgers official YouTube & SportsNet LA post-game press conferences; MLB.com articles; beat reporters on X (e.g. Dodgers beat writers for The Athletic, LA Times, MLB.com, Orange County Register) |
| Japanese angle | Nikkan Sports, Sponichi, Sports Hochi, Full-Count, Yahoo! Japan News (Japanese reporters ask Ohtani/Yamamoto/Sasaki directly) |
| Emotional side stories | Team social media (dugout videos, hugs, family moments), broadcasters' on-air comments |
| Fan reactions | r/Dodgers and r/baseball game threads, X replies, YouTube comments on official highlights |

### 3.2 NexLev workflow (which topics are getting views right now)

| Goal | Tool | Settings |
|---|---|---|
| This competitor's winners | `youtube_channel_outliers` | `channel_id=UC1C2FvyrUf8meDbpuTWTlkA`, `max_videos=500`, `min_outlier_threshold=2` |
| Its newest uploads (what's hot this week) | `youtube_channel_videos` | `sort_by=newest` → compare views after 2–3 days |
| Niche-wide hits | `search_videos` | `query="大谷翔平"` (or "Ohtani"), `minOutlierScore=3`, `minLength=12:00`, last 30–60 days, `sortBy=outlierScore` |
| Breakouts on tiny channels | `search_viral_videos_small_channels` | `query="大谷"` / `"Ohtani"`, `maxChannelSubCount=30000` |
| What YouTube is pushing | `search_youtube_suggested_videos` | `isFromHomeFeed=true`, `query="大谷"` |
| More competitors to watch | `get_similar_channels` | competitor ID, `level=2` |
| Real local-broadcast translations (honest benchmark) | `youtube_channel_videos` | `UCB9Bptvb7Itd78R66pMKYvA`, `sort_by=popular` |

### 3.3 Story score (keep ≥ 18/25)

Score each from 1 to 5:
- **Emotion:** family, gratitude, tears, friendship, conflict.
- **Big moment:** milestone, postseason, record, award.
- **Real quotes available:** at least 3 people quoted on record.
- **Relationship angle:** two named people and how they interact.
- **Proven demand:** a similar story was an outlier (≥3x) on any channel.

**Calendar boosters:**
- postseason and World Series (Oct–Nov);
- MVP and award week (Nov);
- milestones (HR #40/#50, strikeout records);
- returns from injury;
- a teammate's farewell (Kershaw-type);
- WBC years.

---

## PART 4 — AI prompts

### Prompt A — Titles

```
Use OHTANI_PIPELINE.md Parts 1.3 and 2.3. Language: {LANGUAGE}.
Story: {what happened + the real quote(s) + who said them + source}.
Write 10 titles (5 in the Japanese-style formula, 5 in the English formulas), each with: the star's name first,
the moment + a number, a curiosity hook about real words, an emotion word the content truly earns.
Never claim a source we don't have. Score each on curiosity/emotion/accuracy (1–5) and pick the best.
```

### Prompt B — Research pack

```
Collect for {game/date}: final score and 5–8 key moments with numbers; every real post-game quote from
{players} with exact source (video URL + timestamp or article URL); 3–5 pieces of background (past games,
relationship history, earlier quotes); 5 real fan/media reactions (paraphrased, with links).
Output as a table. Flag anything unverified as [VERIFY]. Do not invent quotes.
```

### Prompt C — Script (20–24 min)

```
Use OHTANI_PIPELINE.md Part 2.2 and the research pack below. Language: {LANGUAGE}. Narrator only.
Write the full script in blocks 1–10 with timestamps. Use ONLY quotes from the research pack, each introduced
as "[Name] told reporters:" / "at the press conference, [Name] said:" and followed by our explanation.
Fill length with context, history and analysis, never invented dialogue. Mark opinions as opinions.
After every 1–2 sentences add a visual cue: [CLIP: …≤8s], [PHOTO: …], [QUOTE CARD: name / quote / source],
[STAT CARD: …], [NAME PLATE: …], [MUSIC: tense|piano|uplifting], [SFX: shutter|whoosh].
End with: word/character count, runtime estimate, list of sources used, and any [VERIFY] items.
```

### Prompt D — Description & tags

```
From the script, write: line 1 = title; 1-sentence summary of what was really said; chapters from the block
timestamps; "Sources:" list; 3–5 hashtags; 10–15 tags (star, team, teammates in the story, event, language keyword).
```

### Prompt E — QA check

```
Check this script against OHTANI_PIPELINE.md Part 0 and Part 5: every quote has a real source; no AI voice
imitates a real person; title promise is paid off; opinions are marked; runtime 20–30 min; a new visual every
5–8s in the cue list. List every problem with a fix.
```

---

## PART 5 — Final checklist (before upload)

- [ ] Every quote is real, translated faithfully, and its source is in the description (and on screen in the quote card)
- [ ] No AI voice imitating a real person. Synthetic-content disclosure is on if any realistic AI visual is used
- [ ] The title's promise is answered in the video, in the person's real words
- [ ] 20–30 min runtime; cold open ≤8s; recap done by ~3:00; 3 voice blocks; reactions; outro
- [ ] Subtitles on 100% of narration, key phrases highlighted; name plate on each speaker's first appearance
- [ ] A new visual every 5–8s; broadcast clips short with their audio muted; music ducked under the voice
- [ ] Category Sports; chapters, sources, 3–5 hashtags, SRT uploaded
- [ ] At most 1–2 uploads per day, each a genuinely different story
