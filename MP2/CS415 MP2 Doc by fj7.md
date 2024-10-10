I will briefly talk about the process of my level design. I firstly followed up from what I have done from MP2 CP1, which is right after finished the chaser. Based on all I have from that, I made the mortar enemy. The mortar fire part is intuitive and easy to implement. We can simply make a projectile Blueprint and cause some radial damage at hit location, which stimulate the basic explosion.

Also for the kill by stepping onto enemies' head functionality, it is intuitive as well. Simply set up a collision box onto enemy's head and set up corresponding function on begin overlap will perfectly achieve this feature.

Since I do not want to have it fire up randomly without any accuracy, I decide to make a projection prediction functionality which determine the projection angle and direction based on player's velocity, that is, the willingness. This is not hard to implement, after watch some references and tutorials online [^1], I successfully implement that but it just not that..smart. The prediction is becoming stupid when player suddenly increase or decrease its velocity. It is working perfectly for constant speed and static object.

Asking for the third user-defined enemy, it took me a long while to think about it. I end up deciding to combine the mortar projectile and the chaser together - the bomb carrier, which will spot player, chase him, and perform a suicide bomb which has huge damage on player and cause player to lose the ability to move. I consider this enemy as the boss. Once encounter him, the best way is to avoid combat (he has collision box onto his head as well, but the bomb is in front of him, which make the collision zone is hard to approach), and escape from it immediately. 

I made a linear map formed by several islands - a few of small islands which placed with mortar enemy which have really favorable spot and sight to constantly shoot player, and a few of big islands which contains several chaser and one bomber. Every island is reachable, either jump or fly. There are bonus and med-kit along the route which can help player a lot.


[^1]:  [Mortar Prediction BP](https://www.youtube.com/watch?v=4FH8FowTDmg&t=219s&ab_channel=UE-Loss_)