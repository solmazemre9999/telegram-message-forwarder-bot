# Roblox PvP Gacha + Game Ideas (Cookie Run Kingdom-Inspired)

## Why I couldn't live-scan the charts
I attempted to reach Roblox Charts via `https://www.roblox.com/charts`, but the request returned a `403 Forbidden` from the proxy in this environment. As a result, the ideas below are based on common, consistently trending Roblox genres and long-running hits in the ecosystem rather than a live snapshot.

## PvP-first game ideas that pair well with a generous (but not trivial) gacha
These are intentionally flexible so you can decide later what theme you like (fantasy, sci‑fi, cute, etc.).

1. **Arena Skirmish (3v3 / 5v5)**
   - Core loop: quick matches, draft weapons + skills, short rounds.
   - Retention: ranked ladder, seasonal rewards, rotating arena hazards.
   - Gacha fit: weapons and skills (separate banners).

2. **Battle Royale Lite (10–20 players)**
   - Core loop: drop in, loot/roll pre‑match, fight for 5–8 minutes.
   - Retention: limited‑time rulesets, duo queues, win‑streak bonuses.
   - Gacha fit: weapon kits + skill loadouts.

3. **Payload / Objective Push**
   - Core loop: team fights over an escort point or capture zones.
   - Retention: map rotation, mid‑season balance updates, clan wars.
   - Gacha fit: weapons with unique ranges + skills that shift combat flow.

4. **Duel Coliseum (1v1 / 2v2)**
   - Core loop: high‑skill duels, fast rematches, spectate queue.
   - Retention: tournaments, streak rewards, wagered matches (cosmetic).
   - Gacha fit: weapon mastery + skills with cooldown timing.

5. **King‑of‑the‑Hill Zones**
   - Core loop: rotating zones, team control bonuses, contested buffs.
   - Retention: weekly zone modifiers, zone‑based achievements.
   - Gacha fit: zone‑synergy skills + weapons tuned for range/mobility.

## Core stats for this PvP game
Keep the system tight and readable for players. Based on your request:
- **HP** (health)
- **ATK** (damage)
- **DEF** (damage reduction)
- **CRIT** (Chance, DMG, Resist)
- **Cooldown** (time to reuse skill)
- **MOV SPD** (movement speed)
- **Range** (effective weapon range)

> You can add advanced stats later, but this set keeps balance manageable.

## Two‑banner gacha system (Weapons + Skills)
### Weapons banner (power + playstyle)
- **Common (C): 60%**
- **Rare (R): 30%**
- **Epic (E): 9%**
- **Legendary (L): 1%**

### Skills banner (separate from weapons)
- **Common (C): 62%**
- **Rare (R): 28%**
- **Epic (E): 9%**
- **Legendary (L): 1%**

> Slightly higher common rate on skills to reduce frustration, since skills are also leveled and need duplicates.

## Pity rules (shared style, separate counters)
- **Soft pity** starts at 30 pulls without Epic+:
  - Increase Epic+ chance by **+0.5%** per pull until one Epic+ appears.
- **Hard pity** at 60 pulls guarantees **Epic**.
- **Legendary pity**: if you go 120 pulls without Legendary, next Epic+ becomes Legendary.

> Weapon and skill banners should each track their own pity counters.

## Duplicate handling (generous but not free)
- **Dupes convert to shards** (or “skill stones”).
- **Shard shop**:
  - Common dupes = 1 shard
  - Rare = 3 shards
  - Epic = 12 shards
  - Legendary = 40 shards
- **Direct craft**:
  - Rare: 60 shards
  - Epic: 180 shards
  - Legendary: 600 shards

## Skill leveling (level 1–100)
- **Upgrade currency**: “Training Tokens” earned from PvP matches, daily quests, and events.
- **Max level**: 100.
- **Per‑level scaling**:
  - Every level increases the skill’s **stat % bonus**.
  - Example linear scaling: **Level 1 = 5% bonus**, **Level 100 = 25% bonus**.
  - This can be non‑linear (slower early, faster mid, slower late) if you want a smoother PvP curve.

## Skill structure (two stats per skill)
Each skill provides **two stats** from this pool: **HP, ATK, DEF, CRIT, Cooldown**.
- Skills only list two stats to keep rarity and balance clean.
- When used, a skill buffs **weapon stats** (ATK, CRIT, Cooldown, MOV SPD, Range) or **player stats** (HP, DEF) depending on the stat types.
- **HP/DEF** are always **player‑only** bonuses.
- **ATK/CRIT/Cooldown** apply to **weapon performance**.

### Placeholder skill examples (you can rename later)
1. **Iron Focus** → ATK + CRIT
2. **Bulwark Pulse** → HP + DEF
3. **Sharpsight** → CRIT + Cooldown
4. **Berserker Rhythm** → ATK + Cooldown
5. **Fortified Sprint** → HP + Cooldown
6. **Steel Skin** → DEF + CRIT

## Skill activation rules (cooldown + duration)
- **Default duration**: **10 seconds** of buff time.
- **Default cooldown**: **30 seconds**.
  - For faster PvP, you can try **20–25 seconds** but keep it noticeable.
- Buffs expire after duration ends, then skill is locked until cooldown completes.

## Balance guardrails
- Keep **weapon rarity** meaningful but avoid massive power spikes.
- Use **matchmaking brackets** or **weapon/skill score** to reduce stomp matches.
- Provide **free pulls** through PvP wins to avoid pay‑to‑win stigma.

## Implementation notes for Roblox
- Use **server‑authoritative RNG** for pulls.
- Store pity counters, shards, and skill levels in a **DataStore**.
- Run skill activation and buff timing on the server to prevent exploits.

## Next steps
If you pick a theme, I can tailor weapon types, skill names, and a banner schedule.
