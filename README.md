# Haunt Attraction Simulator

## Background & Context

I worked in a haunted house attraction for 2 years and it inspired me to write this game engine.

The initial idea is to make a text-based haunted house experience where visitors can enter into procedurally generated rooms or corridors and be frightened by actors, animatronics, and atmosphere.

I want to double-dip and save each visitor's experience and compile them into a 50,000 word novel as an entry for NaNoGenMo 2024. The idea here is to collect data about visitor's experiences and stitch them together into a story. Or maybe it could be like a business report. Idk yet. Gotta write this code first, and then we'll see.

## Initial Ideas & Features

1. Gather visitor data
```
> What is your name?
~ Visitor McVisitFace

> What are your pronouns?
~ they/them

> What one thing are you afraid of?
~ Spiders

> What else are you afraid of?
~ Going outside
...
```

The input can be text-based for the name, it would probably be easier to make selection-based for other information. The user-input is captured and used to inform flavor text for different room experiences during the actual visit.

2. Flavor text introducing the haunted house and its lore

> The Haunted Magoo Lagoon was once the home of pirates and after a catastrophic hurricane, it fell into ruin. Lorem ipsum etcetera.

A lot of the flavor texts are probably going to be some sort of Mad Libs situation using a corpora of some kind.

3. The visitor visits

> On a mild Halloween evening, Visitor McVisitFace has decided to visit The Haunted Magoo Lagoon to (test their might? have a good time with their friends? fulfill an obligation from losing a dare?)...

I don't really know what this will end up looking like. But after the haunted house is introduced, the visitor-character shoud have some sort of impetus for visiting. It should be totally random but comprehensible (as will many of the flavor-text features in this game).

4. The visitor can enter a room or corridor

> You step into a sandy, uneven area littered with rotting wood and beach towels. You hear water crashing distantly, almost like waves from the ocean. There are bird cawing. Are they crows or seagulls?

The sample text I wrote here is kind of thematic. It would be nice to constrain the procgen of flavor text based on an area's theme.

5. There might be something frightening in that area: an actor, an animatronic, or the atmosphere. Maybe there is some sort of combination.

> As you are inspecting a mossy statue, a tall, wet figure lurches out from a decaying stack of barrels. `mhreAAH`, it sputters, as it lunges towards you with a flayed hand!

This is the money-maker feature. Should probably spend smart time working this out.

6. The visitor can react to each experience

```
What do you do?
[x] Scream
[ ] Jump back
[x] Cover your eyes
[ ] Laugh
[ ] Heckle the actor
[ ] No reaction
```
These can be multi-select and maybe the data can be collected to figure out what rooms are the scariest. Every option should map to some sort of "factor" that can be reduced into a "scary-score." If this is too complex, then the feedback interface could be as simple as this:

```
Did that scare you?
[ ] Yes, absolutely
[ ] I was moderately startled
[x] Not really
[ ] Not at all
```
Here, the scoring is more obvious.

Scores can be used later in a summary text or in a behind-the-scenes report.

7. The visitor leaves the room

> After not really being scared by the Barrel Flayed-Hand Reacher, you exit the room, ducking under into a doorway covered by thick hanging vines.
This completes one step the visitation-loop. Eventually, there is a final room.

8. The visitor is chased by a chainsaw-wielding person as they exit

Instead of writing the flavor text here, I will say that, as a real-life haunted-house-goer the "chainsaw at the exit" gimmick is one of the cheesiest ways to end a haunt-experience and so many places do it so I'm 100% ending every virtual visit with one of these.

9. The visitor can reflect on their experience

I don't really know what happens here. Stats are nice to give to a player when a level or game is completed, right? The fright-meter thing could be used here. There could be a summary of rooms or actors or something. Or a credits sequence. This will probably be one of the last features, so there's time to figure this out.


## Future Roadmap

- A whole simulation game where the player can manage resources (money, labor, equipment, etc) to build and run a haunted house, with a feature to experience it as a visitor.
