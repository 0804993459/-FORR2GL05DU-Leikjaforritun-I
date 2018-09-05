1)Útskýrðu vel e. GameLoop í leikjagerð.

Game Loop er loop'a sem gengur stöðugt þó að einstaklingur(player)
slá i ekki inn eitthvað(input) röðinn er yfirleitt input update render.
Ef það er ekkert input þá fer það beint í update og þetta gerist á hverju einasta 
FPS frames per second. En maður yfirleitt að hafa cap svo að leikurinn keyri ekki 
of hratt og svo þarf mögulega að vera með catchup sem þíðir að það þarf að keyra
uptade oftar en einusinni áður en það fer í render. Og það getur verið möguleg 
lausn á hardware muni

2)Útskýrðuð hvernig hægt er að fá hreyfingu (e. movement) á hlut með notkun e. velocity,
position ogsfrv. 










notes)
góð útskiring 1)
A game loop runs continuously during gameplay. 
Each turn of the loop, it processes user input without 
blocking, updates the game state, and renders the game. 
It tracks the passage of time to control the rate of gameplay.
http://gameprogrammingpatterns.com/game-loop.html
2)
https://medium.com/@swiftsnippets/vectors-position-velocity-and-direction-b85342ed9e3a

