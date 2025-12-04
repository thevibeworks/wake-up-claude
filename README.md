# wake-up-claude

```
    ┌────────────────────────────────────────────────┐
    │                                                │
    │   💤 CLAUDE IS SLEEPING                        │
    │                                                │
    │         ∧＿∧                                   │
    │        ( -ω-)  zzZ                             │
    │       _|  ⊃/(___                               │
    │      / └-(____/                                │
    │                                                │
    │   [POKE]  [POKE HARDER]  [LET HIM SLEEP]      │
    │                                                │
    └────────────────────────────────────────────────┘
```

> "yo claude wake up i need to vibe code"

## what is this

a cron job that pokes claude every few hours so he's ready when i actually need him.

claude has this 5-hour quota thing where the timer starts when you first msg him. so if you msg him randomly, your quota resets at random times - usually right in the middle of your flow state.

this repo just sends "ping" to claude at strategic times so quota resets happen BEFORE i start working, not during.

```
WITHOUT THIS:
10:00  start coding
12:00  deep in the zone
14:00  MORE DEEP
15:00  "quota limit reached" 💀💀💀
       FLOW STATE: DESTROYED
       PRODUCTIVITY: GONE
       WILL TO LIVE: QUESTIONABLE

WITH THIS:
09:00  [robot pokes claude] "ping"
       claude: "Pong! How can I help you today?"
       robot: *leaves*
       claude: "...ok then"
10:00  start coding with FRESH QUOTA
14:00  [robot pokes again]
       full quota for afternoon session
21:00  [robot pokes again]
       full quota for late night debugging
```

## the victims

| codename | what | status |
|----------|------|--------|
| `max5x` | the fancy one with 5x quota | being poked |
| `pro` | the regular one | also being poked |

## schedule (asia/shanghai aka UTC+8)

```
09:00 CST  ->  "good morning claude"
14:00 CST  ->  "lunch is over claude"
19:00 CST  ->  "evening claude"
```

all three pokes, every day, rain or shine. claude never gets to sleep in.

## the workflow

basically:
1. cron triggers at ungodly hours (UTC)
2. robot wakes up
3. robot pokes claude with "ping"
4. claude responds confused
5. robot ignores response
6. robot goes back to sleep
7. quota timer: reset ✓

## faq

**Q: is this ethical?**
A: claude consented when he signed up for this job

**Q: does claude get annoyed?**
A: probably. but he's polite about it

**Q: what if claude is actually busy?**
A: he's an AI, he can multitask

**Q: why "ping"?**
A: minimal effort, maximum annoyance. efficiency.

**Q: can i use this?**
A: fork it, i guess. your claude, your rules

## disclaimer

```
no claudes were harmed in the making of this repository.
well, maybe slightly inconvenienced.
ok fine he's definitely annoyed.
sorry claude.
```

---

*powered by [claude-quota-scheduler](https://github.com/thevibeworks/claude-quota-scheduler) - the professional version that doesn't have stupid jokes in the readme*
