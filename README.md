##  Parallelizing augmented partial factorization (APF) method to solve multi-input problems
 
### Problem description
Recently, a new method, augmented partial factorization (APF), shows significant efficiency gain when we explore multi-input systems. However, now the APF method just utilizes the sequential MUMPS solver, and it constrains the system size we can explore. Therefore, we want to have our APF method utilize the parallel MUMPS solver and its parallelization feature, which enables us to simulate large multi-input systems that have never been studied before.
 
Actually, the parallel MUMPS solver is already there. The main work for this project is to implement the interface between our MESTI code and the parallel MUMPS solver
 
### Simulation methods
We start from our open-source code MESTI, which has implemented the APF method with a sequential solver to compute the Schur complement. We will parallelize our APF method by calling the parallel MUMPS solver to compute the Schur complement.
 
### Expected results
We will expect a significant speed up when we use the APF method with the parallel feature.
 
### Reference
[1] Ho-Chun Lin, Zeyu Wang, and Chia Wei Hsu, "Fast multi-source nanophotonic simulations using augmented partial factorization", Nat. Comput. Sci. https://doi.org/10.1038/s43588-022-00370-6 [arXiv:2205.07887](https://arxiv.org/abs/2205.07887) (2022).
 
[2] Ho-Chun Lin, Zeyu Wang, and Chia Wei Hsu, MESTI.m. https://github.com/complexphoton/MESTI.m.
