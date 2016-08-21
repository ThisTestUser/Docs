# KILLAURA DETECTION
AntiCheat has gone far from using NPCS...

### What are the Killaura detection tricks?
**Invisible players behind** - This has been a trick that was used to defeat older client's killauras.  
This has been bypassed in 95% of the clients.

**Visible players behind** - This is a trick that is also a year old, and is patched in most public clients with FOV,
although there are ways to check if a player is real without FOV...

**Players for a short time** - This is a trick to put the entity in front in front of your FOV (but not over your
cursor) for 0.2 seconds. This has never been bypassed in any public client (Hybrid should bypass it though)
but can be bypassed using a function that is originally supposed to be used for smooth animations...

**MobInFront** - This trick has never been bypassed in any public client (except for Hybrid), but is very simple 
because almost every single killaura is designed the same way. SkillClient seems to have bypassed this but
it is a lockview aura. It is also possible to bypass this by a slient aura, although your client has to be smart
and hit the right entity.

**Heuristics- Accuracy (AAC)** - This does NOT measure how accurate the player aims. If that were the case every 
single snapping killaura would have been detected. This is again exploiting how all killauras are the same.
Currently this and MobInFront are catching all the killauras. While Hybrid bypassed this I think, SkillClient
did not.

**Consistency Checks** - These exploit how Killauras can do something a player would not be able to do 
because of human limitations. Some of these can be bypassed while still giving a player an advantage.

###Hypixel Anti-Cheat

Hypixel Entities (I only checked the invis ones flying around, not the visible ones)

-Entity ID is normal (not out of range)

-Not creative or flying

-Walk speed is 0.10 like any other entity

-Isn't onGround (however onGround is true sometimes for real entities) and falldistance is 0

-Randomly generated names (not on tablist)

-No motionX, motionY, or motionZ (uses teleport packets to move around)

Since MCLeaksV2 is out and I think I pretty much have unlimited alts (and I intergrated this into my own client),
this is some notes about Hypixel's Anti-Cheat.

1. NPC-Based (at least mostly) - I got banned after a random entity with armor and visible just teleported to me. (This also
means) that no public clients bypass WatchDog now, because no one has managed to filter the entities. 

But is it possible? Definitely... (at least for now)

### Types of Hacked Clients
**Public Clients** - Clients that have been around for a looong time. Perfect to use on NCP and vanilla servers,
but their lack of bypasses to AAC means that it is not good for AAC servers.

**Old Private Clients** - Clients that are private that are from years ago. These contain powerful bypasses
like Full Block Phase, ScaffoldWalk, and teleport but are pretty much all patched.

**New Private Clients** - The best clients for AAC servers. They have the most modern bypasses and are perfect
for hacking in GommeHD.net and more. However most of them are not public/downloadable.

###Why GommeHD.net and AAC Test Servers are a Poor Demonstration of AAC's Abilities

There is only 1 difference - They do not kick the player.

- If you do not kick the player, it is very easy to glide on AAC (with taking tons of damage), because your Speed, Glide, and NoFall violations can be above 1000 and there will still be no kick. On an AAC server that kicks however, you would be kicked after flying 5-10 blocks.
- The Killaura detection is easily bypassed if there is no kick. You only have the fake players and the MobInFront, which are very easy to bypass. For example, GafferTV's client appears to bypass Killaura because it was tested on GommeHD only, but in reality the client gets kicked for a Heuristics check after 15 seconds. If your killaura appears to bypass it, the server may have disabled Heuristics completely.
- Toggle Use/Sneak checks are useless if you don't kick. I could show a "bypass" for AAC's sneaking check but I would be kicked after 3 seconds in reality.
