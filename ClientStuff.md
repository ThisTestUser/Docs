Here's just a quick scribble of facts and opinions about things in hacked clients.

###1.9 - What happened to so much of the mods?

1.9 patched many mods, because most of the patched mods was based on the fact that the server determines your ticks for
fire and potion effects based on how many C03PacketPlayers you send. This made it easy for clients to spam these packets 
to speed up time, or stop those packets to prevent fire damage or water damage from ticking. At one point, you could achieve GodMode
by stopping C03PacketPlayer packets, but that has been patched. In 1.9, this is no longer the case, rendering every mod that used
this trick useless.

###Why AAC Bypasses Are (Mostly) Not Good

Lets review all the AAC bypasses I have...

-**Killaura** - The most important AAC bypass, as it is the only bypass to work on NCP servers (speed only works on test NCP servers)

-**Speed** - Another very good AAC bypass, however you may get dragged back after a certain amount of time so its better to toggle this on and off.

-**Jesus** - It doesn't give much of an advantage, but otherwise its good.

-**Teleport** - The delay between clicking the location and teleporting is too long, and it is now exteremely short-ranged.

-**Phase** - Ever since AAC 1.9.10 its been heavily nerfed, it can only go through glass panes and iron bars, so it may be used but it might not work that well (or blocked completely).

-**NoFall** - Can get you kicked if you try to fall to far. You also have to fall normally for the next time you fall.

-**Glide** - You can only glide about 5 blocks (on AAC 1.9.10) with my new glide, I also have an old glide but its completely blocked in AAC 1.9.10. Its kind of useless unless the server has kicking disabled.

UPDATE 7/16/16: Most of these are patched. They can only be used on outdated AAC servers now.

###AAC Bypass Level

Latest NCP mostly reflects this, but for some mods it doesn't.

1. AAC doesn't block fastclick, which allows you to move items instantly.
2. AAC blocked packet sneak bypass (and any other similar bypasses) and all auras except Triggerbot.

###SkillClient Killaura

-Only bypasses an old version of AAC (and its because he skidded the bypass)

-Limited to 3 blocks (dev can't fix it because the whole idea was skidded)

-Faces client side instead of packet facing (MC source not public = can't skid packet facing functions)

###Does BlockHitting make you take less damage?

Yes. Both in 1.8 and 1.9. However, it will only do so **only when implanted correctly**. This means that you must be able to block and run at full speed whenever a player is in range. You also need to make sure that the server acknowledges that you are blocking. If you can hit when you are blocking without releasing or modifing how mouse clicking is fired, you are already doing something wrong. If NoSlowdown works when you are blocking without any bypasses, you are also doing something wrong.

###Carrot Client

Now lets see how 0.9.1 does...

AAC Click TP - This isn't how it is supposed to be done at all.

AntiAAC - This also is a fail.

AAC Fly - Another fail, even if it does work it can only fly about 3 blocks.

AAC Spider - Looks like a fail phase.

A pure example of how stupid/skiddy some clients can be and wizardhax still allows it.

**Obfuscation**- It claims to be "skid-protected", but the MC source was **never obfuscated**! 

**Killaura**- NONE of them bypass anything. It never even faced the target, and it won't even get around AntiCheat if its for 1.10, let alone AAC, which requires more tweaks to killaura to bypass then ever. 

**Bypass Section**

**Glides**- NONE of them bypass AAC nor NCP.

For instance:

-AAC Glide is almost 7 months old.

**Speed**- The speed AAC,NCP might bypass, but its skidded from other clients.

-Non of the BHops will bypass (except if they give 0 advantage of course)

-AAC Jesus is skidded so much that he didn't know you could remove the 5.9x statement because it will get overwritten. It also does not give a high advantage.

-NoFall doesn't bypass at all.

-NCP Fly is just plain stupid. Performing the hurt animation doesn't deal damage to you!

-AAC Fly is almost the same as vanilla fly.

-Inventory Move is a skid, and is not implanted.

-AAC Step is also a skid (and doesn't work).

So you see, this client is utter trash. The GUI display is also messed up, and its better for you to stick to your own client.

###CrashHead Exploit

The CrashHead exploit is an exploit to crash clients. It involves creative mode and block placing permissions. This hack was known a long time ago, when it was only featured in private clients. However, due to a client leaking the exploit to the public, this may be patched. Currently this works on vanilla and Bukkit/Spigot servers, and no plugin can stop this. The Spigot team doesn't even know about this. 

EDIT: Even dropping the item can crash players who see it! 



I have already crashed and prevented over a 100 players (just in 2 days span) from joining just because of this new exploit. 

###What can Wurst's Killaura bypass?

The truth, and only the truth, about Wurst's Killaura (this also applies for KillauraLegit)

**CAN**

*NoCheatPlus* - With almost every single killaura facing and attacking correctly, it is almost impossible for NoCheatPlus to cancel
attacks.

*AntiCheat and old anti-cheats* - These anti-cheats enforce the same rules as NoCheatPlus, and are therefore bypassed.

*AntiAura* (checkAura) (**NOT** the one by joehot200) and other plugins which **only** use NPCS - With killaura FOV and invisible players selection, these are easily bypassed.

**CANNOT**

*AAC* - AAC has multiple checks to ensure that clients are easily detected. Even when not hitting any NPCS, you are still flagged. The last version of AAC that Wurst can bypass is 1.7.X, when only NPCs were used.

*AntiAura* (joehot200) - This one also has some good checks to detect Wurst. It doesn't rely on NPCS, and this is why it is detected.  

*Reflex and any other heuristics anti-cheat plugins* - They use maths to catch killauras.

###AAC Teleport

This mod does not go as far as you think. It only goes to about 30 blocks and then you get dragged back if you go any further.

Clue: Besides the original way of doing it (source code for Teleport non bypass is public, search it up), teleport does 1 thing before and 1 thing after the actual teleporting.

###Hybrid's NoFall "Bypass"
I have successfully reverse engineered Hybrid's NoFall bypass and implanted it successfully into my client.

Thing is, its NoFall is no different from other NoFalls, except that it does a certain thing to "trick" AAC
into giving you little to no fall damage.

This is why you can still get kicked because after failing NoFall 30 times you get kicked.
###Can you run commands using signs and books in 1.9?

**Yes.** However, you are **limited** of what you can do. One important thing is that you can no longer run
admin commands as a non-admin. Thus, this is broken. I think you can still do it, but it may be limited by servers.

###Killaura vs KillauraLegit (Wurst)

Differences:

1. KillauraLegit prevents you from going overboard by using things like 6 block
range, 20 attack speed, and prevents criticals which make you look like a hacker.

2. KillauraLegit faces client side, preventing you from accidently hitting a block
and a player at the same time, which means that you get flagged for angle check 
which checks if you are actually looking at something before you can interact with it.

As you can see, considering that you disabled all suspicious settings and turned everything
down (e.g. not setting range to 6 blocks), KillauraLegit will be detected **no slower** 
than if you use Killaura. 

Why?

KillauraLegit's facing and hitting methods are pretty much idential to Killaura's, with the exception of the things
mentioned above. KillauraLegit is just as prone to the exploits that AAC uses to catch Killauras.

###SafeWalk and FastPlace vs ScaffoldWalk

Truth is, if you compare the speed of this on NCP servers, ScaffoldWalk will only be **slightly** faster.

Also, using FastPlace with SafeWalk is useless, the block placing delay has already passed by the time you move one block forward.

So what's the advantage?

1. Automation - You can look at an enemy's base and its distance while placing a block under you, while with SafeWalk you have to have your head away from enemies.

2. Faster - On specific servers you can go really fast (about twice as fast) with this hack, however on NCP servers you can get stopped for FastPlace. It doesn't matter for most private clients anyways, their ScaffoldWalk can't even look at the block properly (all are copied from Saint or some other client) so there's the speed. Also that ScaffoldWalk allows you to walk at full speed while sprinting, while with SafeWalk you can't sprint (unless you also have sprinting backwards hack).

###FakeHackers Code Dump (1.9)

All code belongs to and is written by ThisTestUser.

http://pastebin.com/WqL1S6mw

Every client should have this.

**Why?**

If this popular, there are 2 ways this can go:

1. FakeHackers gets legit players banned as well as hacking players.
2. Staff become more aware of this, and they have to actually see you taking damage or they have to see the hacking firsthand, saving a lot of hackers from ban.
