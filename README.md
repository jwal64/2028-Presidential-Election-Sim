# THE 270 — 2028 Presidential Campaign Simulator

A single-file, no-dependency browser game. Build a candidate, win a contested
primary against a field of real 2028-plausible figures, pick a running mate,
and try to get to 270.

Open `index.html` in any browser. That is the whole install.

## What's in it

**A full primary bracket.** Eight real contests — Iowa, New Hampshire, Nevada,
South Carolina, Super Tuesday, the Rust Belt, the Sun Belt, New York and
Pennsylvania — with 2,140 delegates and 1,071 to clinch. Proportional
allocation above a viability threshold, with a winner's skim on the Republican
side. Rivals gain and lose momentum, drop out on a schedule, and either endorse
you or endorse the person beating you. Fall short of a majority and you get a
contested convention with three ways to try to win the floor — or a concession
speech.

**A real field.** Six rivals each run from a pool of nine per party (Vance,
Rubio, DeSantis, Haley, Youngkin, Ramaswamy, Carlson, Cruz, Sanders on one side;
Newsom, Shapiro, Whitmer, Buttigieg, Ocasio-Cortez, Moore, Beshear, Pritzker,
Gallego, Crockett on the other). Rubio is on the Republican ballot every single
run and Newsom is on the Democratic one; the remaining slots are drawn at
random. The other party runs its own
primary in the background — you watch it on the wire ticker and find out in June
who you actually have to beat.

**A full candidate builder.** Name, home state (all 50, sets your region and your
hometown bump), party, one of eight backgrounds, one of eight signature issues,
and a perk/flaw pair that changes the underlying math — the fundraising machine
prints $4M a turn, the debate assassin halves debate risk, the carpetbagger
loses the home-state advantage and gets $10M for the trouble, and "there is a
file" guarantees the October surprise and makes it worse.

**Or run as somebody who already exists.** Instead of filing your own paperwork
you can take over any contender in your party's pool — Rubio, Vance, Newsom,
Ocasio-Cortez, anyone on the list. They come off the ballot, their name and home
state fill themselves in, and you start the primary at their standing instead of
as an unknown.

**A hundred and eight decisions and a calendar that asks for twenty-six of
them.** Every run draws a fresh set: eleven in the primary, three at the
convention, seven in the fall, two in debate prep and three in the closing
fortnight. Every answer moves base, swing voters, press, money and the regional
map, which is to say every answer moves the polls. Choices tagged to your
signature issue land 35 percent harder. The riskier ones can backfire outright.

Three of every five slots are real political questions with real answers — the
number in weeks, the deportation figure, the top marginal rate, single payer
versus the public option, tariffs versus the price of a washing machine, the
third rail, the plank fight, the pledge with four bullet points and a problem
in the fourth, whether you will say plainly that you'll accept the result.

**The other two are the tier where the country is not well,** and they are
reserved, not left to chance: the push-up challenge, your own campaign chatbot
committing you to a foreign policy at 3 a.m., the grocery-price buzzer segment,
a meme coin with your face on it and a $410M market cap, a rival's hologram
doing nine counties at once from a soundstage in Northern Virginia, a
600-pound butter sculpture of you that looks like somebody else, an eleven-day
livestream, a debate rescheduled to 2 a.m. in a podcast studio, a pay-per-view
debate between two undercard fights, a synthetic endorsement from a president
dead since 2004, and a $40M whale moving the prediction markets four days out.

**Things that happen to you.** Between decisions the news arrives and you do not
get a vote. Sixty-four bulletins fire between turns, at most one per two turns
and never repeating in a run, some gated on the state of your campaign. Half of
them are the news — the jobs number, a hot inflation print, gas under three
dollars, a 900-point drop, hostages on a tarmac, an embassy roof. The other half
is a ceremonial groundhog biting a candidate on live television, your logo
blimp adrift at 1,100 feet over Toledo with two fighters watching it, a black
bear stopping the motorcade for forty minutes, a teleprompter loading the other
party's convention address, your college band's 1994 demo getting a 4.1 from a
real critic, a milkshake, and four hundred thousand dollars of campaign
merchandise arriving in February. Some hit your own numbers. Some move the
national mood, a country-level figure that shifts every state at once and has
its own readout on the gauges.

**The supporting cast.** Media anchors and networks, the podcast circuit,
celebrity endorsers, and billionaire donors — cast fresh each turn from
party-appropriate pools, so the same event reads differently depending on who
walks into it.

**A real map.** Ten battlegrounds worth 120 electoral votes, leaning off the
2024 result relative to the national margin, with 219 safe Republican and 199
safe Democratic votes behind them. Two media buys, an internal poll with a house
error you don't find out about until election night, and a live decision desk.

**Debate nights as scenes.** Four days of prep, then two debates of three
exchanges each, scored live. Every exchange has a way to lose it; prep and press
coverage make that less likely and a gaffe-prone candidate makes it more so. The
spin room pays out on how many you landed.

**The file.** A persistent oppo heat gauge that rises with every corner you cut
and falls when you take the hard, honest option. Above 26 degrees it can surface
at any point in the general — not just in October — and it costs you points at
the end whether it ever ran or not.

**Down ballot.** Ten competitive Senate races on top of a 45-45 hold, running on
a fraction of your coattails plus a candidate of their own, and a House number
driven by the popular vote. Winning the White House with 49 Senate seats gets
you a governing verdict that says so.

**Seeds and a leaderboard.** Every roll in the game runs through a seeded PRNG,
so a seed reproduces a run exactly as long as you make the same choices. The
seed is on the title screen, in the URL as `?seed=`, on the result card, and
behind a "replay this seed" button. Results post to a leaderboard — which lives
in `localStorage`, because a single static page has no server: it survives
reloads on that device and does not travel between devices or people.

## Balance

Tuned against automated playthroughs that pick every choice at random. A random
campaign loses the primary just over half the time and, if it gets through, wins
the general a bit more often than not — roughly a three-in-ten run overall. The
bot never buys advertising, which is the single largest lever a real player has,
so reading the internal polls and concentrating a buy is worth several states on
its own.

## Notes on the satire

Real public figures appear as exaggerated characters. Every event, quote, poll,
scandal and result is invented. Nothing here is reporting, prediction, or a
claim of fact about any real person, and the invented scandals belong to the
player character.
