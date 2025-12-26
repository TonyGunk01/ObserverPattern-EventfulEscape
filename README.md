# EventfulEscape-ObserverPattern

Eventful escape is a horror game where the player has to get keys and try to escape locked rooms and areas. I have made this game in Unity2D and programmed in C#. 

The challenge here is that, in the case of any major game event like player death, multiple classes need to be modified of this event. Creating methods to individually notify and update states, values, positions, etc is not efficient hence I have implemented an observer design pattern to simplify the process. Just one event needs to be invoked and like a domino effect, the relevant methods to that purpose will also be executed. 

The references to the individual functions is configured with the help of delegates which act as method pointers. However, it's less secure as there's no abstraction implemented. Hence I implemented events in delegates. Now it can be called only from within the class and not outside of it. It also prevents unnecessary overriding of delegates.

Since this is a horror game, the player must feel scared, either through a classic jumpscare, ominous music building up, etc. These scenarios are now effectively controlled by usage of event delegates. Like, you pick up a key and then after a few seconds, suddenly the lights go off, the screen shakes and you hear ominous laughter in the background. This creates the sense of urgency for the player to find and switch on the lights as soon as possible.

Video demo:
