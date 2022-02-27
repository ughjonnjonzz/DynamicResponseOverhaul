# Dynamic Response Overhaul
_a Stardew Valley dialogue mod, by CelestialFirestorm_

## Dependencies
### Content Patcher:
Kinda goes without saying; here it is anyway. Hard requirement. Everything _besides_ Content Patcher is technically optional, but you MUST have at least one of them or DRO won't do anything. Literally nothing.

Makes use of dozens of `When:` conditions, comparing against NPCs' `Hearts` levels, to determine which dialogue to use in a given moment. Because of the sheer depth of variance, I decided to work in "tiers" of `Hearts` levels. In general, the tiers are:
  - 0-2 `Hearts`
  - 2-6 `Hearts`
  - 6-10 `Hearts` for non marriage candidates
  - 6-8 `Hearts` for marriage candidates
  - 8-10 `Hearts`
  - 10-14 `Hearts`

There are some characters with minor differences to reflect growth in their story, but this was the template I started with given that most of them don't have drastic changes between two and six `Hearts`.

Every line of dialogue, for every character, for every single item, in every single tier, was written by me.

### Custom Gift Dialogue Utility:
Enables NPCs' unique dialogue when receiving gifts. Technically optional, but this is the main purpose of DRO.

Makes use of:
  - `GiftReaction_`
  - `GiftReactionCategory_`
  - `GiftReactionPreserved_`
  - `_Birthday`
  - `_SecretSanta`

[Full documentation](https://github.com/purrplingcat/StardewMods/tree/master/CustomGiftDialogue#create-gift-reaction-dialogues)

### Unique Courtship Response Core:
Enables NPCs' unique dialogue for:
  - accepting/rejecting a bouquet
  - accepting/rejecting the Mermaid Pendant
  - giving the Stardrop after marriage
  - receiving birthday gifts (that weren't already covered by the previous module)

This is every function currently available, and DRO makes use of all of them.

[Full documentation](https://github.com/MissCoriel/UniqueCourtshipResponseCore/wiki/Explanation-of-Dialog)

### More Conversation Topics:
Enables NPCs' unique reactions to:
  - `Player`'s wedding
  - `Player`'s divorce
  - `Player`'s newborn child
  - the best outcome at the Luau
  - the soup being poisoned at the Luau
  - Mayor Lewis's unmentionables in the soup at the Luau

This is every function currently available, and DRO makes use of all of them, with a fun bonus: NPC reactions when the `Player` is _expecting_ a child, not just after it's born. On top of that, through the use of `When:` conditions and a special Dynamic Token (`{{1stChild.Gender}}`), villagers will know the gender of the first child and react to the gender of the second child accordingly, both before and after birth.

[Full documentation](https://github.com/elizabethcd/MoreConversationTopics/tree/main/docs)

### Custom Tokens:
Enables post-marriage dialogue, specifically on your anniversary. All NPCs have special dialogue to congratulate you, and your spouse reacts uniquely to gifts given on the day.

Makes use of:
  - `AnniversaryDay`
  - `AnniversarySeason`
  - `YearsMarried`

[Full documentation](https://github.com/TheMightyAmondee/CustomTokens/blob/master/README.md)

## Known Issues:
`divorce`: If you divorce `Character B` after having previously divorced `Character A`, `Character A` will react with the same dialogue they used after their own divorce.
  - I'm looking into it (maybe your new divorce just brings up painful memories, I dunno)
  - for now, `divorce` dialogue is more general to make it less awkward

## Future Plans:
Once all the dialogue is finished, there are no more plans for DRO -- at least on my end. If any of its dependencies update with new functionality, I will also update DRO to take advantage of those new possibilities. Short of that, and bugfixes as necessary, when it's done, it's done.

**Stats As Tokens:**
  - pull the name of a random animal from `Player`'s farm when gifting Artisan Goods
    - _function currently broken; Stats As Tokens needs to update_
    	- I literally already have this all written; I just need SaT to work

## Changelog:
<!-- **0.3.0:**
	- Caroline complete

**0.2.0:**
	- Alex complete

**0.1.0:**
  - Abigail complete
-->
**0.0.9:**
  - basic functions... functional. it lives!
  - translation capable!
