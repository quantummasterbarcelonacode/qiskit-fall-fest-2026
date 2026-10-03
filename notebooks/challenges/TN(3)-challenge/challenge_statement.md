# Simulating a quantum computer on your laptop

MQST Qiskit Fall Fest 2026 challenge (Qiskit + Tensor Networks).

Mentors: Joaquín G Márquez Olguín & Miguel Fernández Suárez.

Quantum computers are supposed to give an exponential speed-up for certain problems, and computing quantum dynamics is the obvious example. Is that true? The question turns out to be harder to answer than it sounds, and in this challenge you will find it out with measurements on your own laptop!

Consider a state of 300 spins. If we want to store it in our computer, it has 2^300 complex amplitudes, about 10^82 gigabytes!!! but the observable universe holds an estimated 10^80
atoms... Writing or manipulating the complete state down is therefore an impossible task.

However, quantum many-body dynamics does not always use all that space. Quantum algorithms are designed to use it, but a spin chain evolving for a short time may not, and if it does not, your laptop can follow the short time evolution of hundreds of qubits. Finding where that stops being true is the challenge.

In 2011, Lanyon and collaborators ran the first universal digital quantum simulations on a quantum computer of six trapped ions, with sequences of up to a hundred gates [1]. You will build three classical simulators from scratch in Python and point them at that same physics: a state vector simulator, a sparse matrix solver that is still exact but much cheaper, and a tensor network (matrix product state) simulator that organises its memory on entanglement rather than on amplitudes. Everything is cross-checked against Qiskit since Aer ships both a state vector and a matrix product state engine.

Then comes the experiment. You push every engine on your own machine until it dies and work out
what killed it, along two axes: the number of qubits, and evolution time where the entanglement
barrier hits, comparing classical limits against what physical quantum processors can provide.

Evaluation will be based on both, the notebook filled with your own code and answers, and a live defense answering the main question above. You can use whatever you want in the notebook, but the answers must be yours. 

AI assistants can be used to assist you with the code, but the answer to the main question should be yours entirily.

No prior tensor network knowledge is assumed.

## References

[1]. B. P. Lanyon et al., Universal Digital Quantum Simulation with Trapped Ions, Science 334,
57 (2011). Included as `lanyon2011.pdf`.

[2]. U. Schollwock, The density-matrix renormalization group in the age of matrix product
states, Ann. Phys. 326, 96 (2011), arXiv:1008.3477.

[3]. R. Orus, A practical introduction to tensor networks, Ann. Phys. 349, 117 (2014),
arXiv:1306.2164.

[4]. A. T. Sornborger and E. D. Stewart, Higher-order methods for simulations on quantum
computers, Phys. Rev. A 60, 1956 (1999).

[5]. Qiskit, https://www.ibm.com/quantum/qiskit, in particular the Aer `matrix_product_state`
simulation method.

[6]. J. Schachenmayer, Classical computing for quantum technologists, Universite de Strasbourg.
The lecture course this challenge descends from.

[7]. For the Julia route taken by the original version of this challenge, ITensors.jl at
https://itensor.github.io/ITensors.jl/ and Yao.jl at https://yaoquantum.org/.
