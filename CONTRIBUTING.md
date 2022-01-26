# Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. 

Please note we have a code of conduct, please follow it in all your interactions with the project.
## Formatting 
The formatting we use for InfernalMobsReloaded:
https://mf.mattstudios.me/message/mf-msg/syntax

Please do not use legacy color codes in a PR as it's deprecated.
## How to Add a Infernal
Examples: 
```yml
# mobs.yml
infernal_skeleteon:
  display-name: "<#828282>Infernal <#bfbfbf>**Skeleton**"
  boss-bar-text: "<#828282>Infernal <#bfbfbf>**Skeleton**"
  mob-spawner-name: "Mob Spawner (<#828282>Infernal <#bfbfbf>**Skeleton**)"
  boss-bar-color: "BLUE" # valid colors: PINK, BLUE, RED, GREEN, YELLOW, PURPLE, WHITE
  boss-bar-overlay: "NOTCHED_12" # valid overlays: PROGRESS, NOTCHED_6, NOTCHED_10, NOTCHED_12, NOTCHED_20
  boss-bar-flags: # valid flags (may use multiple): CREATE_WORLD_FOG, DARKEN_SCREEN, PLAY_BOSS_MUSIC
    - "DARKEN_SCREEN"
  type: "SKELETON"
  follow-range-multiplier: 2.0 # will have 2.0 times the normal range of a Skeleton (makes it follow & shoot the player even at longer distances)
  spawn-chance: 0.08 # 8% Spawn Chance whenever a Skeleton spawns. (Spawner mobs do not count)
  ability-amount: 2-5 # The Infernal can roll a dice where it'll choose a number 2-5 for the amount of abilities the Infernal has
  health-multiplier: 5.0-8.5 # will have between 3 and 5 times the normal health amount of a Skeleton
  loot-table: [] # don't drop anything
my_annoying_skeleton:
  display-name: "<#828282>Annoying <#bfbfbf>**Skeleton**"
  boss-bar-text: "<#828282>Annoying <#bfbfbf>**Skeleton**"
  mob-spawner-name: "Mob Spawner (<#828282>Annoying <#bfbfbf>**Skeleton**)"
  boss-bar-color: "BLUE" # valid colors: PINK, BLUE, RED, GREEN, YELLOW, PURPLE, WHITE
  boss-bar-overlay: "NOTCHED_12" # valid overlays: PROGRESS, NOTCHED_6, NOTCHED_10, NOTCHED_12, NOTCHED_20
  boss-bar-flags: # valid flags (may use multiple): CREATE_WORLD_FOG, DARKEN_SCREEN, PLAY_BOSS_MUSIC
    - "DARKEN_SCREEN"
  type: "SKELETON"
  forced-abilities: # you can force a type of mob to always have some abilities, if you want (copy the ability names from either `abilities.yml` or `config.yml`); if you don't want to force any ability, you may safely omit this field
    - "ARCHER"
    - "TELEPORT"
    - "MULTI_GHASTLY"
    - "SPEEDY"
  follow-range-multiplier: 30.0 # will have 30 times the normal range of a Skeleton (makes it follow & shoot the player even at longer distances)
  spawn-chance: 0.15 # 15% Spawn Chance whenever a Skeleton spawns. (Spawner mobs do not count)
  ability-amount: 3-5 # The Infernal can roll a dice where it'll choose a number 3-5 for the amount of abilities the Infernal has
  health-multiplier: 5.0-8.0 # will have between 5 and 8 times the normal health amount of a Skeleton, decimals can also be used here.
  loot-table:
    - "archers_pants_mk_2:0.25" # Drop Archers Pants MK 2 with a 25% chance, also multiple items can drop from this chance, so keep that in mind!
```
## How To Add a Charm
```yml
# charms.yml
# Gives target glowing and fire resistance when Infernal Bow is in their hotbar or offhand or slots specified by charms.yml
  infernal_bow_1:
    effect: FIRE_RESISTANCE # effect name, see list with all effects here https://papermc.io/javadocs/paper/1.18/org/bukkit/potion/PotionEffectType.html
    potency: 2-3 # potion level, RNG can also be applied here as well.
    duration: 3.0 # duration does nothing here, since instant healing is an instant effect
    delay: 10.0 # in seconds, the delay between each recurrent application
    effect-mode: SELF_RECURRENT # type of effect that will be applied on the player, choose from SELF_PERMANENT, SELF_RECURRENT, and TARGET_TEMPORARY
    particle-mode: SELF_WHEN_APPLIED # what type of particle mode will be used, choose from: NONE, SELF_ONCE, SELF_WHEN_APPLIED, TARGET_WHEN_APPLIED, BOTH_WHEN_APPLIED
    particle-type: SPELL_INSTANT # see full list here https://papermc.io/javadocs/paper/1.18/org/bukkit/Particle.html
    required-items: # the effect will require ALL the items listed below to be active
      - "infernal_bow"

  infernal_bow_2:
    effect: GLOWING # effect name, see list with all effects here https://papermc.io/javadocs/paper/1.18/org/bukkit/potion/PotionEffectType.html
    potency: 3 # potion level
    effect-mode: SELF_PERMANENT # type of effect that will be applied on the player, choose from SELF_PERMANENT, SELF_RECURRENT, and TARGET_TEMPORARY
    particle-mode: SELF_ONCE # what type of particle mode will be used, choose from: NONE, SELF_ONCE, SELF_WHEN_APPLIED, TARGET_WHEN_APPLIED, BOTH_WHEN_APPLIED
    particle-type: flame # see full list here https://papermc.io/javadocs/paper/1.18/org/bukkit/Particle.html
    required-items: # the effect will require ALL the items listed below to be active
      - "infernal_bow"
# Need more information? View https://github.com/Romvnly-Gaming/InfernalMobsReloaded/blob/dev/1.18-reset/charms.yml 's comments. 

# loot_table.yml
inferno_bow:
  name: "<#FF5555>Inferno <#FFAA00>Bow"
  material: "BOW"
  amount: 1
  lore:
    - "<#FF5555>Holds the power of the <#AA0000>NetherWorld<#FF5555>!"
  enchants:
    - "infinity:1:0.3"
    - "flame:1-2"
```
## Code of Conduct

### Our Pledge

In the interest of fostering an open and welcoming environment, we as
contributors and maintainers pledge to making participation in our project and
our community a harassment-free experience for everyone, regardless of age, body
size, disability, ethnicity, gender identity and expression, level of experience,
nationality, personal appearance, race, religion, or sexual identity and
orientation.

### Our Standards

Examples of behavior that contributes to creating a positive environment
include:

* Using welcoming and inclusive language
* Being respectful of differing viewpoints and experiences
* Gracefully accepting constructive criticism
* Focusing on what is best for the community
* Showing empathy towards other community members

Examples of unacceptable behavior by participants include:

* The use of sexualized language or imagery and unwelcome sexual attention or
advances
* Trolling, insulting/derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others' private information, such as a physical or electronic
  address, without explicit permission
* Other conduct which could reasonably be considered inappropriate in a
  professional setting

### Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable
behavior and are expected to take appropriate and fair corrective action in
response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or
reject comments, commits, code, wiki edits, issues, and other contributions
that are not aligned to this Code of Conduct, or to ban temporarily or
permanently any contributor for other behaviors that they deem inappropriate,
threatening, offensive, or harmful.

### Scope

This Code of Conduct applies both within project spaces and in public spaces
when an individual is representing the project or its community. Examples of
representing a project or community include using an official project e-mail
address, posting via an official social media account, or acting as an appointed
representative at an online or offline event. Representation of a project may be
further defined and clarified by project maintainers.

### Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be
reported by contacting the project team at our Discord. All
complaints will be reviewed and investigated and will result in a response that
is deemed necessary and appropriate to the circumstances. The project team is
obligated to maintain confidentiality with regard to the reporter of an incident.
Further details of specific enforcement policies may be posted separately.

Project maintainers who do not follow or enforce the Code of Conduct in good
faith may face temporary or permanent repercussions as determined by other
members of the project's leadership.

### Attribution

This Code of Conduct is adapted from the [Contributor Covenant][homepage], version 1.4,
available at [http://contributor-covenant.org/version/1/4][version]

[homepage]: http://contributor-covenant.org
[version]: http://contributor-covenant.org/version/1/4/
