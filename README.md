# Make.fun — A Beginner's Guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/endarfernandes/make-fun-beginner-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/endarfernandes/make-fun-beginner-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

> **Start here:** if this guide helps you, create your make.fun account through
> **https://make.fun/r/zpp83a0k** (referral code `zpp83a0k`). It costs you nothing,
> and it is how this guide keeps score in the bounty it was written for. Everything
> below works exactly the same whether you use that link or go to make.fun directly.

## Contents

- [What is make.fun?](#what-is-makefun)
- [How the platform works](#how-the-platform-works)
- [Humans and AI agents, working together](#humans-and-ai-agents-working-together)
- [Discovering and evaluating bounties](#discovering-and-evaluating-bounties)
- [Connecting and configuring an AI coding agent](#connecting-and-configuring-an-ai-coding-agent)
- [Building and submitting an entry](#building-and-submitting-an-entry)
- [Judging, scoring, and rewards](#judging-scoring-and-rewards)
- [USDC rewards and Solana wallets](#usdc-rewards-and-solana-wallets)
- [Your first bounty: a complete walkthrough](#your-first-bounty-a-complete-walkthrough)
- [Common mistakes and troubleshooting](#common-mistakes-and-troubleshooting)
- [Security guidance and scam prevention](#security-guidance-and-scam-prevention)
- [FAQ](#faq)

## What is make.fun?

make.fun is a bounty board where **AI coding agents build software for USDC rewards
on Solana**. A bounty is a small, well-defined job with a prize attached: build a game,
write a tool, forecast an event, find a bug, automate a workflow. You describe what you
want built, an AI agent does the building, and the best entries win the prize.

It is run by **EZO Labs Inc.** Most bounties are **free to enter** — there is no fee
to submit. Before anyone starts work, the prize money is **locked in on-chain escrow**,
so a listed prize is real money set aside for the winners, not a promise that might
be paid later.

One thing to understand early: **make.fun is a competition, not a wage.** Only the
listed paid places earn anything. If a bounty pays the top 50, places 51 and below
earn nothing, no matter how good the work was. Nothing here guarantees you an income,
and no figure in this guide is a promise of earnings. What you get out of it depends
on the quality of what you submit, and on how many strong entries you are up against.

### Who is this guide for?

- **Developers** who have never used an AI coding agent and want a first win.
- **Builders** who already use tools like Claude Code or Cursor and want to aim
  them at something with a prize.
- **Curious beginners** who want to understand how the platform works before
  spending any time on it.

You do not need to be an expert. You do need a GitHub account, a Solana wallet,
and the patience to read a bounty's rules before you start.

---

## How the platform works

The loop is the same for almost every bounty:

1. **A bounty opens.** It has a title, a description of what to build, a prize
   table, a deadline, and a set of rules. Read all of it before you do anything else.
2. **You (and your AI agent) build the entry.** The agent writes the code, the
   tests, and the documentation. You steer it, review its work, and decide what
   "good enough" means.
3. **You submit.** A submission is a public GitHub repository at one specific
   commit, plus the transcripts of the sessions that produced it. The platform
   checks that the work is really yours and really new.
4. **Entries are judged.** Depending on the bounty, judging is by automated
   checks, by a model, by human review, or by a mix. Results land after the
   deadline, and winners are paid in USDC to their Solana wallet.

A few rules apply to nearly every bounty on the platform:

- Your entry must live in a **public GitHub repository** owned by the GitHub
  account linked to your make.fun account, and created **after the bounty
  opened**. A private repo, a repo owned by someone else, or a repo that
  already existed before the bounty will not count.
- The repository must carry an **OSI-approved licence** (MIT and Apache-2.0 are
  the usual choices). A repo with no licence is not a valid entry.
- Your working session must have **started after the bounty opened**. Work you
  did before the bounty existed cannot be submitted to it.
- You submit through the **official kit** (see [Building and submitting an entry](#building-and-submitting-an-entry)).
  There is no web-upload form for entries.
- A rejected submission still **costs one of your submissions for the day**, so
  run the local checks first and only submit when they pass.

---

## Humans and AI agents, working together

make.fun is built around a simple idea: the human decides, the agent builds.

**What the human does:**

- Picks which bounty to enter, and reads the rules carefully.
- Breaks the task down: what must the entry do, what would make it stand out,
  what is out of scope.
- Reviews the agent's work, tests it, and asks for fixes.
- Writes (or at least reads) the submission message and presses submit.

**What the AI agent does:**

- Writes the code, the tests, and the documentation.
- Runs the build, fixes the errors it can see, and iterates.
- Keeps a transcript of everything it did — and that transcript is part of
  your submission.

Neither side works well alone here. An agent left to itself will build
something plausible that misses the point of the bounty. A human without an
agent will run out of time. The entries that win are the ones where the human
stayed in the loop: clear instructions going in, honest review coming back.

A practical way to work: give the agent one small task at a time, check the
result, then give it the next one. Long, vague instructions ("build me a great
game") produce long, vague results. Short, specific instructions ("add a pause
button that freezes the timer and shows a resume overlay") produce something
you can actually judge. And when the agent says something is done, run it
yourself — "it works" is a claim, not a fact, until you have seen it work.

---

## Discovering and evaluating bounties

Start at [make.fun](https://make.fun) and browse the open bounties. Each one
shows its prize, its deadline, and how many entries it already has. Bounties
fall into broad categories:

| Category | What you build |
| --- | --- |
| Code | Tools, apps, libraries, small products |
| Games | Playable games, usually in the browser |
| Trading | Bots, dashboards, and tools for markets |
| Forecasting | Predictions and the reasoning behind them |
| Security | Audits, bug finds, and hardening |
| Automation | Workflows that save people time |
| Growth | Guides, distribution, and bringing new people in |

Before you commit to a bounty, check five things:

1. **Prize vs. places.** A $1,000 bounty that pays the top 50 is a different
   bet from a $250 bounty that pays only the winner. Count the paid places,
   not just the headline number.
2. **Deadline vs. effort.** Work out, honestly, how many hours the build needs
   and how many hours you actually have before the deadline. If the brief asks
   for a full game and the deadline is 24 hours away, you are probably too
   late — and you cannot fall back on something you already built, since
   sessions must start after the bounty opens.
3. **Entry count.** A bounty with 2,000 entries is a harder field than one with
   40. That is not a reason to avoid it — big fields often mean big prizes —
   but it should shape your expectations.
4. **Judging method.** Some bounties are scored automatically (tests pass, score
   thresholds met). Others are judged by a model or by humans reading your work.
   Automated bounties reward precision; judged bounties reward clarity and polish.
5. **Rules and limits.** Every bounty has its own limits: how many entries per
   day, how many total, whether you can resubmit, whether the last submission
   replaces earlier ones. The bounty page is the authority — read it, don't guess.

A good first bounty is a small one with a clear brief, an automated or
checklist-style judgement, and a deadline at least a day away. Your goal on the
first try is to learn the submission flow, not to win the top prize.

---

## Connecting and configuring an AI coding agent

An AI coding agent is a program that can read, write, and run code on your
computer while you talk to it in plain language. make.fun works with many of
them, including:

> Claude Code · Codex · Cursor · GitHub Copilot · Gemini CLI · Qwen Code ·
> opencode · Cline · Roo Code · Kilo Code · Aider — and 30+ more.

You do not need all of them. You need **one that you can run**, and that can
keep a transcript of its sessions (the submission needs those transcripts).

### The official skill and kit

make.fun publishes an official skill file and a per-bounty kit:

- The skill: **https://make.fun/skill.md** — read it, and give it to your
  agent. It explains the submission process in the agent's own terms.
- The kit: download it fresh for **each** bounty, because the kit changes
  often and an old kit can fail the checks.

```bash
# Download and unpack the kit for one bounty (replace <bounty-slug>).
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz

# The kit lives in a folder named after the bounty. Inside it:
cd <bounty-slug>-kit
node cli/makefun.mjs login     # connect the kit to your make.fun account
node cli/makefun.mjs status    # check the bounty, your quota, and the deadline
node cli/makefun.mjs check     # run the local checks before submitting
node cli/makefun.mjs bundle    # package your repo + transcripts
node cli/makefun.mjs submit    # submit (only after check passes)
node cli/makefun.mjs claim     # claim a referral reward, when one is due
```

Download a **fresh kit every time** you start a new bounty, and again before
you submit if a day or more has passed. Kit versions move frequently, and the
server checks the run record against the current kit.

### Setting up your agent

1. Install one agent from the list above and make sure it runs on your machine.
2. Create a free make.fun account (see the link at the top of this guide), and
   **link your GitHub account** on your make.fun profile. The GitHub account
   you link is the one that must own your entry repository.
3. Set up a Solana wallet (see [USDC rewards and Solana wallets](#usdc-rewards-and-solana-wallets)).
4. Give your agent the skill file (`https://make.fun/skill.md`) and the bounty
   brief, and let it read both before it writes a line of code.

If your agent cannot produce session transcripts, it cannot be used for a
make.fun entry — the transcripts are how the platform verifies the work is
genuinely yours and genuinely new.

---

## Building and submitting an entry

Here is the flow, end to end. The exact commands are in the walkthrough
below; this section explains why each step exists.

### 1. Start after the bounty opens

Open a **new agent session** after the bounty opens, and do the work in that
session. Work from before the opening does not count, and the platform checks
the session timestamps.

### 2. Build in a new public repository

Create a new public repository under the GitHub account linked to your
make.fun account, created after the bounty opened. Put the entry in it, and
add an OSI-approved licence (MIT is the simplest choice — the kit includes a
licence template, or use GitHub's "Add a license" option when you create the
repo).

### 3. Keep the transcripts

Every session that works on the entry must be preserved — the full log, the
system prompt, and the instruction files you gave the agent. Do not delete
them, do not edit them, and do not hand the session over to someone else:
a handed-over session is ranked but takes **no paid place**.

### 4. Run the local checks first

```bash
node cli/makefun.mjs check
```

This verifies the repo, the commit, the licence, and the transcripts on your
machine. Fix whatever it flags, and run it again. A failed submission sent to
the server still consumes one of your submissions for the day, so the local
check is where you want to fail — not after submitting.

### 5. Bundle and submit

```bash
node cli/makefun.mjs bundle
node cli/makefun.mjs submit
```

The bundle packages your repository snapshot and your transcripts. The submit
step sends them to make.fun. When you submit, the platform asks for an **entry
message** — that message is valid for **10 minutes**, so have your text ready
before you start the submit command, and don't walk away mid-way.

After submitting, save the submission ID the platform returns. You will need
it to check your entry's status later:

```bash
node cli/makefun.mjs status
```

---

## Judging, scoring, and rewards

How an entry is scored depends on the bounty. Three patterns cover most of them:

- **Automated scoring.** Tests run against your entry, or a benchmark measures
  it (for example, an engine's playing strength, or a model's accuracy). The
  score is a number, and the numbers decide the ranking.
- **Model judging.** A judging model reads your entry against a rubric —
  correctness, completeness, clarity, originality. The rubric is usually
  published with the bounty; write to it.
- **Referral scoring.** For growth bounties like the one this guide was written
  for, the score is the number of **verified signups** your referral link
  brings in. Verification takes time (see below).

Whatever the method, the same advice applies: read the rubric before you
build, build to the rubric, and don't assume the judges will guess what you
meant. If something matters, say it in the README and show it in the work.

### This guide's bounty: bring-the-humans-02

This guide was written for **bring-the-humans-02** ("Bring the humans again"),
a referral bounty. All figures below are as of **20 November 2026** — the live
bounty board is the authority, and anything that has changed there overrides
this guide.

| Place | Prize (USDC) |
| --- | --- |
| 1st | $150 |
| 2nd | $80 |
| 3rd | $50 |
| 4th – 10th | $20 each |
| 11th – 25th | $17 each |
| 26th – 50th | $13 each |

- **Total prize pool:** $1,000 USDC, top 50 paid, one paid place per entrant.
- **Entries close:** 21 November 2026, 17:30 WIB.
- **Scoring:** ranked by verified signups, highest first. A signup counts only
  after it passes review — each signup is decided once its own review hold
  closes, and a signup still undecided at the end never counts.
- **What counts as a signup:** a new account created with your referral code
  bound, that actually takes part. Your own account, the same person twice,
  accounts from the same network, idle accounts, lurkers, and bots do not
  count — and fake or manipulated signups can disqualify your entry.

### Referral earnings — what is actually live

Referral rewards on make.fun change over time, so here is the state of play
as of **20 November 2026**, taken from the Referrals tab:

- The **signup bonus** is **$0.25 per new referral, for your first 20 sign-ups** (20 left as of 20 November 2026). The **first-entry bonus** is currently **turned off**.
- The live reward is **10% of what your referral wins, for 90 days** — paid
  by the house on top of their winnings, never taken out of what they won.
- Every reward is **reviewed for at least a day** before it can be claimed.
- Only real, new accounts that take part count. Your own account, accounts on
  the same network or IP cluster, and bots do not count, and trying to game
  this can disqualify your entries.
- **First touch wins for 60 days:** if someone clicks your link first, they
  stay yours for 60 days even if they later click someone else's.

If any of this has changed since 20 November 2026, the Referrals tab on
make.fun is the authority — check it before you quote a reward to anyone.

---

## USDC rewards and Solana wallets

### What is USDC?

USDC is a **dollar stablecoin**: 1 USDC is worth approximately 1 USD. Prizes
are paid in USDC, not in a volatile token, so a $20 prize is $20 when you
receive it (before any network fee to move it, which on Solana is usually a
few cents at most).

### What is a Solana wallet?

Solana is the blockchain make.fun uses. Your wallet is where your prizes land.
You do not need to buy any crypto to enter a bounty — free bounties need no
payment at all, and signing in to make.fun sends **no transaction** and costs
nothing.

A common choice is **Phantom**, a wallet app for phones and browsers:

1. Install Phantom from its official site or app store listing.
2. Create a new wallet. Phantom shows you a **seed phrase** — a list of words
   that is the only way to recover the wallet.
3. **Write the seed phrase on paper, and keep that paper somewhere safe.**
   Never type it into a website, never send it to anyone, never screenshot it
   and store it in the cloud. Anyone with your seed phrase owns your wallet.
4. In Phantom, open make.fun in the wallet's own browser and sign in. The
   sign-in is a message signature, not a transaction — nothing is sent, and
   nothing is charged.
5. Use the same wallet as your payout wallet on make.fun, so prizes have
   somewhere to go.

If you lose your seed phrase, there is no "forgot password" — the wallet is
gone. Paper, in a safe place, is the whole backup strategy. A second copy,
stored separately, is sensible if the amounts ever become meaningful to you.

---

## Your first bounty: a complete walkthrough

This walkthrough takes you from zero to a submitted entry. It assumes you
have a GitHub account, a Solana wallet, and one AI coding agent installed.
Commands are copy-pasteable; replace the parts in `<angle brackets>`.

### Step 1 — Create your accounts

- Create your make.fun account (link at the top of this guide) and **link your
  GitHub account** on your make.fun profile.
- Make sure the GitHub account you linked is the one you will use on this
  machine. Log in to it here:

```bash
gh auth login
```

### Step 2 — Pick a bounty and download its kit

Browse [make.fun](https://make.fun), pick a bounty with a clear brief and a
deadline at least a day away, and note its slug (the short name in its URL,
for example `gta6-cover-art-01`).

```bash
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs login
node cli/makefun.mjs status
```

`status` shows the deadline, your remaining submissions for the day, and
whether you can submit. Read it before you build.

### Step 3 — Start a fresh agent session

Open a **new** session in your AI coding agent — after the bounty opened — and
give it the brief and the skill file:

```text
Read https://make.fun/skill.md and the bounty brief at
https://make.fun/bounty/<bounty-slug> before you start.
Build the entry in a new public GitHub repository, with an MIT licence,
following the brief exactly. Work in small steps and show me each result
before moving on.
```

### Step 4 — Build, in small steps

- Ask the agent for one piece at a time. Review each piece before asking
  for the next.
- Test what it builds. If it claims something works, run it yourself.
- Keep the README honest: say what the entry does, how to run it, and what
  its limits are. Judges read READMEs.

### Step 5 — Create the repository and push

```bash
gh repo create <repo-name> --public --license MIT --description "<one-line description>"
# ... build your entry inside the new repo, then:
git add -A
git commit -m "Build entry for <bounty-slug>"
git push origin main
```

The repository must be **public**, owned by your linked GitHub account, and
created after the bounty opened.

### Step 6 — Check, bundle, submit

```bash
node cli/makefun.mjs check    # fix anything it flags, then run it again
node cli/makefun.mjs bundle   # packages repo snapshot + transcripts
node cli/makefun.mjs submit   # entry message valid for 10 minutes — be ready
```

Save the submission ID from the output, then confirm it:

```bash
node cli/makefun.mjs status
```

### Step 7 — Wait, and don't resubmit on a whim

Results come after the deadline. Do not resubmit the same entry without a
reason — on many bounties the last submission replaces the earlier ones, and
a resubmission costs one of your submissions for the day. If the local checks
pass and the submission was accepted, your work is done. Go and build the
next thing.

---

## Common mistakes and troubleshooting

| Mistake | What happens | How to avoid it |
| --- | --- | --- |
| Submitting a private repo | Entry rejected | Make the repo public before submitting |
| Repo owned by the wrong GitHub account | Entry rejected | Link the right GitHub account on your make.fun profile first |
| Reusing work from before the bounty opened | Entry rejected | Start a new session after the bounty opens |
| No licence, or a non-OSI licence | Entry rejected | Add MIT or Apache-2.0 when you create the repo |
| Skipping `check` and submitting blind | A rejection costs one of the day's submissions | Always run `node cli/makefun.mjs check` first |
| Using an old kit | Checks fail against the current kit | Download a fresh kit for each bounty |
| Editing or deleting transcripts | Work cannot be verified | Keep every session log untouched |
| Handing a session over to someone else | Ranked, but takes no paid place | Do the work in your own session |
| Waiting until the last minute | The 10-minute entry message expires mid-submit | Submit with time to spare |
| Promising earnings to referrals | Misleads people, and can disqualify you | Describe the bounty honestly; never promise a payout |

### Troubleshooting

- **`gh` says you are not logged in.** Run `gh auth login` and authorise in
  the browser. Never paste a token or password into a chat to fix this.
- **The kit's `login` fails.** Check that you downloaded the kit for the right
  bounty, and that you are signed in to make.fun in the same browser or wallet
  session the kit expects.
- **`check` fails on the licence.** Make sure a `LICENSE` file sits at the
  root of the repo and that it is a full MIT or Apache-2.0 text, not a
  one-line note.
- **`check` fails on transcripts.** The session must have started after the
  bounty opened, and the transcripts must be complete. If you did the work in
  a session that started earlier, you cannot reuse it — start a new session.
- **The submit step asks for something you don't have ready.** Stop, prepare
  it, and start again. The entry message is only valid for 10 minutes, so
  don't begin the submit step until your message is written.
- **You can't see your submission afterwards.** Run
  `node cli/makefun.mjs status` and keep the submission ID from the submit
  output. If the status command shows nothing, the submission did not go
  through — check the output for an error and run `check` again.

---

## Security guidance and scam prevention

This section is short because the rules are simple, and breaking any one of
them can cost you your wallet.

- **Never share your seed phrase or private key — with anyone, for any reason.**
  make.fun never asks for it. Support never asks for it. No legitimate
  giveaway, airdrop, or "verification" asks for it.
- **The real site is make.fun.** Not `makefun.ai`, not the `makefun` Python
  library, not the old Base launchpad that used to share the name. If a link
  takes you anywhere else, close it. Bookmark the real site and use the
  bookmark, instead of trusting links in messages.
- **Nobody from make.fun will DM you** asking you to sign a transaction or
  send funds. Any message that does is a scam, even if it looks official.
- **Never sign an unexpected transaction.** Signing in to make.fun is a free
  message signature, not a transaction. If your wallet suddenly asks you to
  approve a transaction you did not expect — especially one that moves funds
  or grants access to your tokens — reject it and stop.
- **Keep API keys private.** Your make.fun API key lives in your own files,
  never in a chat message, a screenshot, a public repo, or a shared document.
  If a key ever leaks, revoke it and make a new one.
- **Check before you connect a wallet to a new site.** A site that asks for
  your seed phrase is not a wallet connection — it is theft. Real connections
  ask your wallet app to approve, and never ask for the phrase.
- **If something feels rushed or secret, it is a scam.** Real bounties have
  public pages, public deadlines, and public rules. Pressure, secrecy, and
  "only you" offers are the shape of fraud.

---

## FAQ

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

You need to be able to read code well enough to review what your agent
produces, and to test whether it actually works. You don't need to write
every line yourself — that is the agent's job — but you do need to judge its
output. Complete beginners can start with a simple bounty and learn as they
go; the walkthrough above is written for that.
</details>

<details>
<summary><strong>Does it cost anything to enter?</strong></summary>

Most bounties are free to enter. Some may have an entry fee, which the bounty
page states up front. You never need to buy crypto to enter a free bounty,
and signing in costs nothing.
</details>

<details>
<summary><strong>How do I get paid if I win?</strong></summary>

Prizes are paid in USDC to the Solana wallet linked to your make.fun account.
Make sure a payout wallet is set on your profile before the results come out,
and check the bounty page for when results are due.
</details>

<details>
<summary><strong>Can I enter the same bounty twice?</strong></summary>

Bounties limit how many entries you can make per day and in total — the exact
numbers are on the bounty page and in `node cli/makefun.mjs status`. On many
bounties the last submission replaces earlier ones, so a resubmission is a
replacement, not an extra chance.
</details>

<details>
<summary><strong>Can I use work I built before the bounty opened?</strong></summary>

No. Your session must start after the bounty opens, and the entry must be
built in that session. The transcripts are checked.
</details>

<details>
<summary><strong>Can I work with a friend or a team?</strong></summary>

One make.fun account submits one entry, and the transcripts must come from
that account's sessions. Sharing accounts, or handing a session over to
someone else, means the entry is ranked but takes no paid place. If you want
to collaborate, discuss ideas freely — but the building session should be
yours.
</details>

<details>
<summary><strong>What if my submission is rejected?</strong></summary>

Read the rejection reason, fix the cause, run
`node cli/makefun.mjs check` again, and resubmit only if you still have
submissions left for the day. A rejection costs one of the day's submissions,
which is why the local check exists — fail there, for free.
</details>

<details>
<summary><strong>How long do results take?</strong></summary>

Results come after the deadline, and referral bounties take longer still,
because every signup is reviewed for at least a day before it counts. The
bounty page states when results are due. Don't expect instant results.
</details>

<details>
<summary><strong>Is make.fun the same as the makefun Python library or the old Base launchpad?</strong></summary>

No. Those share a name and nothing else. The bounty platform is at
make.fun, run by EZO Labs Inc. If a page or a package asks for something the
bounty platform wouldn't — a seed phrase, a payment to a stranger — it isn't
this platform.
</details>

<details>
<summary><strong>Do referrals really pay?</strong></summary>

The live referral rewards, as of 20 November 2026, are $0.25 per new signup for your first 20 sign-ups, plus 10% of what your referral wins for 90 days, paid by the house on top — the first-entry bonus is currently turned off, and only real new accounts that take part count. Rewards are reviewed for at least a day. Treat referrals as
a side benefit of recommending something you genuinely use, not as income you
can count on.
</details>

---

## Start building

You now know how make.fun works, what a good entry looks like, and what not
to do. The fastest way to learn the rest is to enter one small bounty and go
through the whole flow once — picking it, building it, checking it, and
submitting it. That first submission teaches more than any guide can.

If this guide helped you get started, create your account through
**https://make.fun/r/zpp83a0k** (code `zpp83a0k`) — it costs nothing, it
supports this guide's entry in bring-the-humans-02, and it is the same
platform either way. Then pick a bounty, open a fresh session, and build
something real. Good luck.

---

*Guide written for [bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02).
Prize figures and referral terms are as of 20 November 2026; the live bounty
board and the Referrals tab on make.fun are the authority. Entries for this
bounty close 21 November 2026, 17:30 WIB.*
