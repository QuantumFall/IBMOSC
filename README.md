# IBMOSC

Submission for the IBM Open Science Prize 2022 (started in 2022, but concluded in 2023), together with fellow teammates from CQT Pooja Jayachandran and Chee Chong Hian.

The aim of the challenge was to use the Variational Quantum Eigensolve (VQE) to find the ground state of the Heisenberg Hamiltonian with the connectivity of the Kagome Lattice.
Main judging criteria was done based on accuracy, scalability of method, clarity of code and documentation. 

Our method consisted of using an excitation preserving ansatz that was easier to implement compared to the default one provided in Qiskit, transpiling to much fewer gates
on the real `ibmq_guadalupe` backend. Our choice of optimizer, Rotosolve, was easy to implement and did not involve any hyperparameter tuning unlike gradient-based optimizers.

Finally, to obtain the necessary accuracy on the quantum backend, we used the scale-factor method, where we used a simple Hamiltonian $\hat{M}$ to estimate our scale factor
$f = \frac{\langle \hat{M} \rangle _{\textrm{exact}}}{\langle \hat{M} \rangle _{\textrm{hardware}}}$, which we could use to rescale the final ground state after optimization.




