1)

Útskýrðu vel e. GameLoop í leikjagerð.

Game Loop er loop'a sem gengur stöðugt þó að einstaklingur(player)
slá i ekki inn eitthvað(input) röðinn er yfirleitt input update render.
Ef það er ekkert input þá fer það beint í update og þetta gerist á hverju einasta 
FPS frames per second. En maður yfirleitt að hafa cap svo að leikurinn keyri ekki 
of hratt og svo þarf mögulega að vera með catchup sem þíðir að það þarf að keyra
uptade oftar en einusinni áður en það fer í render. Og það getur verið möguleg 
lausn á hardware muni

2)

Útskýrðuð hvernig hægt er að fá hreyfingu (e. movement) á hlut með notkun e. velocity,
position ogsfrv. 

hreyfing í leikum virkar alveg eins og hreyfing í veruleikanum. maður þarf að 
sitja niður reglur eins og a = F/m og svo þarf maður að spila eftir þeim reglum
 til að hreyfa sig

stæ/kóði sem sínir hreyfingu)

    acceleration = force / mass
    change in position = velocity * delta time
    change in velocity = acceleration * delta time
	
    using System.Collections;
	using System.Collections.Generic;
	using UnityEngine;
 
	public class Player : MonoBehaviour {
	 
		 void Update () { //1
			 Vector2 input = new Vector2 (Input.GetAxis("Horizontal"), Input.GetAxis("Vertical")); //2
			 //3 
			 float rate = 10;
			 Vector2 direction = input.normalized;
			 Vector2 velocity = direction * rate;
			 Vector2 moveAmount = velocity * Time.deltaTime;
	 
			 transform.Translate(moveAmount); //4
		 }
	 }
	 
3)

Útskýrðu hvernig árekstur (e. collision detection) gæti verið útfærður í leik með
sýnidæmi













notes)
góð útskiring 1)
A game loop runs continuously during gameplay. 
Each turn of the loop, it processes user input without 
blocking, updates the game state, and renders the game. 
It tracks the passage of time to control the rate of gameplay.
http://gameprogrammingpatterns.com/game-loop.html
2)
https://medium.com/@swiftsnippets/vectors-position-velocity-and-direction-b85342ed9e3a
https://gafferongames.com/categories/game-physics/
3)
https://www.toptal.com/game/video-game-physics-part-ii-collision-detection-for-solid-objects
