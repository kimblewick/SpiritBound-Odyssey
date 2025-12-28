# SpiritBound Odyssey

**Role:** AI Designer (Technical Game Designer)  
**Engine:** Unreal Engine 5.1  

SpiritBound Odyssey is a **3rd-person platformer** created by a team of **7**. The game features **two playable characters**, and the player must **swap between them** to solve puzzles, platform, and fight through combat encounters.

My personal responsibility on the project was to **design and program all enemies**, including **all boss fights**.

> Source (original portfolio page): [`https://rajvardhankavathek.wixsite.com/game-design-portfoli/general-8`](https://rajvardhankavathek.wixsite.com/game-design-portfoli/general-8)

## Media

### Overview / Contribution Reel (YouTube)

[![Raj Kavathekar Portfolio - SpiritBound Odyssey Overview](https://img.youtube.com/vi/iu1E4qXfTCg/hqdefault.jpg)](https://www.youtube.com/watch?v=iu1E4qXfTCg)

### Game Trailer (YouTube)

[![SpiritBound Odyssey - Game Trailer](https://img.youtube.com/vi/KE_VZvVOUl0/hqdefault.jpg)](https://www.youtube.com/watch?v=KE_VZvVOUl0)

## My Contribution

**Demonstration for work done is in the videos above.**

## Bosses

### Thaddeus (Boss)

<img width="486" height="352" alt="884169_5101f61c0dfe42ce8b6e15d45b792f2f~mv2" src="https://github.com/user-attachments/assets/9f60cc33-035b-429e-aa57-d14fe32a3cf7" />


#### Attacks

In its first phase Thaddeus attacks using swing and slam attacks. The player is required to use ground smash to pin Thaddeus' arm on the ground when it slams its arm. In its second phase, Thaddeus shoots projectiles that cannot be deflected.

In its first phase, the slam and sweep attack animations were created using elaborate timelines for each socket on its arm. The phases and attacks were carried out using the Behavior Tree (AI) system. The attacks in both phases use code I implemented to track the player. In the second phase, the arm canon uses the tracking code to face the player and launches a projectile using its unit direction.

#### Description

Thaddeus is the second boss in SpiritBound Odyssey and is found in **Level 3**. It is the first boss I created for the game using **animation timelines** and Unreal Engine’s **AI Behavior Tree** system. It is a stationary boss consisting of **two phases** requiring good reflexes to dodge attacks as well as patience.

![ezgif-618d960ddd37a213](https://github.com/user-attachments/assets/af65679b-5be2-453e-9f13-b8e1183df3fd)



#### Design Decisions

I wished to use the character's abilities to the maximum extent; due to this I decided to make Thaddeus a stationary boss using swings so that the player uses the jump for the combat character which is not often used during platforming.

The ground smash ability was meant to be introduced in that level, therefore I made it so Thaddeus' arm can be pinned using the ability to target its weak spot. In the second phase, the player must play using the Movement Character to stay true to the design pillars requiring both characters to beat the game. Since the movement character excels in parkour I decided for Thaddeus to launch projectiles that would test the agility of the player using dash and double jump.

---

### Enemy in the Industry (Boss)

#### Description

Enemy in the Industry is the third and final boss of SpiritBound Odyssey and is found in **Level 5**. It is the second boss I created. I created the boss using various child actors as its components such as the laser and the spiked ball. I programmed its attacks using simple rotation, however I used complex timers to randomize attacks and adjust the speed for necessary feedback.

![Enemy in the Industry - Full](https://static.wixstatic.com/media/884169_18e714e41bec4218a3d8173f51dc0df9~mv2.png/v1/fill/w_496,h_360,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/EnemyIndustryFullPic.png)

#### Attacks

In its first phase Enemy in the Industry attacks using **two gears**:

- The first gear has a **spiked ball** attached to it which the player can attack to deflect it back at the boss (otherwise it damages the player).
- The second gear is at the bottom and has a **laser** connected to it which the player must jump over.

The boss' first phase was programmed using randomized timers that switch the rotation of gears to throw off the player, with functions to slowly accelerate/decelerate the gears and switch direction. Since the laser and spiked ball required different code to deal damage or be reflected, I created them as separate classes and then added them as fields to the boss.

In the second phase, the boss' gears have been destroyed, causing the boss to attack with **ranged tracking projectiles**. The projectiles are **vertical** and hit the player from above; a **drop shadow** appears to show where the projectile will land.

![Enemy in the Industry - Phase 2](https://static.wixstatic.com/media/884169_a69a084f2d5748fdb5fa43f8356d90d1~mv2.png/v1/fill/w_484,h_272,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/IndustryBossSecondPhase.png)

![ezgif-700f28c64808cff4](https://github.com/user-attachments/assets/eb4d45a0-3117-4c0f-a465-dbc5de9d2c4a)


#### Design Decisions

The plan for this boss was to master all the mechanics the player has learned and make use of all of them—from shielding, to jumping, to attacking. I did this by creating a stationary boss as before but testing their abilities a bit harder, requiring split-second decisions to jump over the laser, shield or attack; hence two gears that attack at the same time instead of one arm like the previous boss.

In the second phase, I decided to use vertical projectiles to make it harder for the player to jump recklessly, because they will end up colliding with the projectile.

---

### Rogelio (Boss)

![Rogelio - Full](https://static.wixstatic.com/media/884169_3366a273ceef43379424d5352a26ac08~mv2.png/v1/fill/w_484,h_320,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/RogelioFull.png)

#### Attacks

Rogelio has only one phase since it is a tutorial boss. It acts similarly to any other enemy. It follows the player using path-finding code and navmesh and possesses a behavior tree AI system, as well as a custom state machine that switches states according to values such as health and distance to the player.

Once in range, Rogelio uses melee attacks to damage the player which can be avoided by getting behind Rogelio. Occasionally Rogelio uses a ground slam move which is an AoE attack on the ground that the player must jump over.

#### Description

Rogelio is the first boss of the game and appears in **Level 1**. It is the third boss I created. Rogelio initially was a regular giant enemy but I decided to incorporate him into level 1 as a tutorial boss to give players a challenge, adding an extra move for them to dodge and with a bigger health bar so they can practice avoiding enemy attacks.

![Rogelio - Attacking](https://static.wixstatic.com/media/884169_5527e2bddb4f47d7aa2064164cdfd51f~mv2.png/v1/fill/w_479,h_269,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/RogelioAttacking.png)

![ezgif-776513c9aeab1ec5](https://github.com/user-attachments/assets/8deee675-84e7-441f-b5b3-dd0afa942dc1)


#### Design Decisions

As mentioned previously this boss was initially an enemy type but was later implemented as a boss due to there being a boss in every odd level (1, 3 and 5). I wanted to set players up for future bosses, which is why this boss is not stationary so players learn not to stay in one position and to keep moving.

The boss' huge health bar also serves as practice against regular enemies, allowing the player to test and try out strategies against potential enemies. I added ground slam to help with jump timings so players are more prepared to jump with the combat character against future bosses (Thaddeus' sweep and Enemy in the industry's laser).

## Enemies

### Ranged Enemy

![Ranged Enemy](https://static.wixstatic.com/media/884169_81730be6875745cc896821db23c37df8~mv2.png/v1/fill/w_484,h_478,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/RangedEnemy.png)

The ranged enemy is the first non-boss enemy type I created. I used a default Unreal Engine character and then programmed my AI controller for behaviors, pathfinding, and detouring from obstacles. The ranged enemy uses Unreal Engine’s **Behavior Tree** system with a blackboard of variables. I created a state machine for different states such as idle, attacking, chasing, fleeing, and dead, along with their animations and priorities.

The ranged enemy chases the player until it’s close enough to shoot a projectile that can be deflected back at the ranged enemy. Once the player closes in, it flees in the opposite direction.

### Shielded Enemy

The shielded enemy is the second non-boss enemy I created and is a child of the Ranged Enemy. It was made for the player to utilize their ground slam ability. The ranged enemy chases the player and attacks once in range. The shield can be broken using ground slam (as displayed on the shield). Once the shield is broken the enemy runs away and is unable to attack; after 5 seconds the shield regenerates and the behavior continues. While the shield is active the shielded enemy takes **10% of total damage**.

![Shielded Enemy](https://static.wixstatic.com/media/884169_066e52edc12b4c2595b5d421e8ef34f0~mv2.png/v1/fill/w_478,h_335,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/ShieldedEnemy.png)

### Basic Enemy

The basic enemy is the fourth non-boss enemy I created and is the child of the Ranged Enemy. It is the first enemy type the player encounters to introduce the combat system. The basic enemy follows the player and once the player is in range it starts attacking at a random time in a fixed interval.

![Basic Enemy](https://static.wixstatic.com/media/884169_c58be7ee2dc541a5912d597942cd594f~mv2.png/v1/fill/w_474,h_392,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/BasicEnemy.png)

### Explosive Enemy

The explosive enemy is the third non-boss enemy I created and is a child of the Ranged Enemy. Later in the game, as encounters increase, the exploding enemy can be used to clear out larger groups. The explosive enemy chases the player; once in range it starts flashing and continues to chase. After 5 seconds it explodes, destroying itself and applying massive damage in a radius to enemies and the player.

![Explosive Enemy](https://static.wixstatic.com/media/884169_b109fbb338ce4c6e87302caaa0b49458~mv2.png/v1/fill/w_483,h_518,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/ExplosiveEnemy.png)

### Heavy Enemy

The heavy enemy is the fifth non-boss enemy I created and is the child of the Basic Enemy. It is similar to the basic enemy, but larger and slower. It has **2× health** and deals slightly more damage. It was used to make players use full combos and add variation to enemy combos.

![Heavy Enemy](https://static.wixstatic.com/media/884169_e2a7351c84444abc8c9f03f426a19d91~mv2.png/v1/fill/w_479,h_463,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/HeavyEnemy.png)

## Systems

### Inventory System

The inventory system was initially created by me for consumables and a shop system that was going to be a part of the game. This is why the inventory system was initially created using a map of objects (items) and integers (their quantity), and used functions to display their description, quantity, and item type. Eventually, the shop system and consumables were cut from the game leaving us with coins and treasures that could be mapped using strings and integers.

![Inventory System](https://static.wixstatic.com/media/884169_43087fb075f44664898d68102b979584~mv2.png/v1/crop/x_0,y_42,w_1923,h_1009/fill/w_476,h_250,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/Inventory%20System.png)

### Interaction System

The interaction system was created to allow the player to use objects such as levers, pushable boxes, doors, keys, etc. I created it by using sphere traces launched from the front of the player every **0.25 delta seconds**.

I created the parent class of interactable objects with functions to show the HUD and carry out print string functions that can be overridden. Since this is a dual character game, the traces are active only when the player possesses the character and are disabled in the inactive character.

![Interaction System](https://static.wixstatic.com/media/884169_87228256241949b49b91595aeefd9570~mv2.png/v1/fill/w_479,h_395,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/InteractionSystem.png)

## Download Link

- **Download**: `https://grosheuvel.itch.io/spiritbound-odyssey`

