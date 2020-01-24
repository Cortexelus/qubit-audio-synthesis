# Qubit Audio Synthesis

Generating audio from qubits, using Qiskit.

# How does it work?

It's sorta like wavetable synthesis but with qubit(s). A [qubit](https://javafxpert.github.io/grok-bloch/) serves as a `phase clock` rotating its azimuth 2π every period. This qubit is connected through an `arbitrary quantum circuit` to a `qubit output`. The amplitude of the output's state vector makes the sound.

Manipulating the arbitrary circuit is how you *play* it. What kinds of circuits make crazy sounds? Complicated circuits with lots of entanglements? Maybe you'll find out!! 

Using a real quantum computer you need to collapse the output qubit into a classical register. The amount of `shots` you take determines the amount of *noise* in the sound! (isn't that cool?) Or, if you use a simulator you can read the output qubit's state directly, and have no noise. 


### Wavetable synthesis

See this? These are waves. These waves here last for one period. 

![wavetable synthesis](http://synthesizeracademy.com/wp-content/uploads/wavetable-synthesis-wavetable.gif)

Each wave is a list of amplitudes. You take a wave, repeat it indefinitely, to make a sound. The sound is pitched because it's periodic. The user sets the frequency/pitch by changing the length of the wave (or sample rate).

![wave amplitude](https://study.com/cimages/multimages/16/amplitudedw.png)

# Ideas

 - The `phase clock` doesn't need to be a perfect repeating period. It could rotate in non-repeating ways, evolving the sound forward.
 - The `phase clock` could just be a parameter in the middle of the circuit too
 - Turn this into a web app 



CJ Carr 2020 
[[dadabots.com](http://dadabots.com)] [[cortexel.us](http://cortexel.us)]



