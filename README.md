# ffockstish

> Cheating is lame. Cheaters are scum. If they spent as much time learning actual chess as you spend re-creating new accounts, lying to others, and avoiding the gaze of chess.com fair play team, then they would probably be a decent chess player in the 1-2000 rating range. But they aren't because their puny brains are addicted to farming ELO from innocents.

_- Anon. - circa Oct 2023_

**FFockstish** is a FireFox browser extension for running stocksfish analysis during _OTHER PEOPLES_ chess.com games to aid in cheat detection
You probably dont need this browser plugin. This extension violates chess.com's terms of service if you use it on your own games. So dont do that, because that is cheating. And cheating lowers your IQ and otherwise makes you unnattractive to just about anything with a pulse.

The idea here is that you should be able to analyze another players games in realtime when trying to catch cheaters. Unfortunately, chess.com no longer provides a deep analysis facility during games. This actually makes sense, because when they _did_ provide it to everybody, it was the primary mechanism for low life cheaters. E.g. it would 100% give people with multiple accounts an edge over everyone else. It would also allow groups of people to gang up on others on a back channel (like a discord chat group).

My hope is that I can write a tool that is useful to catch cheaters, without being particularly useful for cheating, that is more useful than the tools that chess.com provides, in the hope that they elect to incorporate something similar back into their site, so we don't need to maintain this via the community.

# How it works

You are never going to 100% prove a player is cheating online outright. Only chess.com can accurately do this, because they can employ much higher degrees of statistical analysis than you can. 

However you can find the blatant cheaters. This tool's sole purpose in life is to encourage (or disprove) your hunches to report a suspected cheater early and often, to ensure that chess.com's algorithms are kept well fed. Remember: nobody loses when you make reports even when you aren't 100% certain.

Cheaters seek the following advantages:

- play good to great moves quickly
- win just enough to keep pushing their ELO higher over time without getting caught
- give multiple moves intelligence in advance to avoid being caught out in unnaturally robotic lines

Cheaters use the following techniques to do this without detection:

- Avoid picking the #1 engine move. Instead they alternate between the top 1-5 engine moves. This is because by default, chess.com only shows 2-3 lines in post analysis. This helps them avoid being reported in the first place
- Avoid playing engine moves on every move. They might alternate such that they only cheat on every 2nd or 3rd move
- Avoid cheating in every game. They might choose to only cheat with white for 10 games, then only cheat with black for 10 games

Therefore, this tool is designed to detect these states. 

- It will load up the players history and go and find 'red flags' for cheating in the players history.
- It will look for patterns in win/loss history.
- It will keep track of each move in a given game and give statisical analysis on how often engine moves where played.
- It will look at the beginning, middle and end games and analyse strength of moves during each section

Thats the plan anyway. If I see any indicators this tool is used for cheating then I'll probably take down the source code and keep it to a private set of cheat hunters.

# Installation

** Once the source for this repo is ready I will remove this sentence. Until then, its not ready, so dont bother with lodging an issue because I'll just close them. **

You will need to download a zip of the source code locally and install it into FF manually. You can find instructions on how to do that elsewhere. I meant it when I said that you probably don't need this browser plugin.
