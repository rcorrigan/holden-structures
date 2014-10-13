holden-structures
=================
Atomic resolution protein structures of genes screened by the Holden Comprehensive Cancer Center.

MolProbity Statistics:
Mean MolProbity Score for all STARTING Structures = 2.529
Mean MolProbity Score Percentile for all STARTING Strutures = 51.189
Mean MolProbity Score for all FINAL Structures = 1.777
Mean MolProbity Score Percentile for all FINAL Structures = 80.189

Mean MolProbity Clash Score for all STARTING Structures = 22.902
Mean Clash Score Percentile for all STARTING Structures = 53.853
Mean MolProbity Clash Score for all FINAL Structures = 2.163
Mean Clash Score Percentile for all FINAL Structures =96.081


The initial models that we have refined are from either Swiss-Model or ModBase, indicated by the initials following their sequence length (see Naming Conventions, below).  These original structures are refined using two different optimization algorithms, developed by the Michael Schnieders lab at the University of Iowa:

  Algorithm 1. is a local optimization algorithm; it will computationally “walk down hill” in energy until it finds a certain root mean square gradient as defined by a convergence criteria (i.e. it looks for the minimum root mean square energy gradient position for each atom to be in and when it finds a pre-defined convergence criteria, it stops there).
  
  Algorithm 2. is a rotamer optimization algorithm. Rotamers are the variable portion of amino acids that are attached to the c-alpha carbon atoms fo the protein backbone and can interact with each other to varying degrees, depending on the protein folding.  
  
Proteins prefer to fold into states with the most favorable rotamer interaction possible leading to a more stable structure.

The rotamer optimization algorithm determines the optimal conformation of each rotamer such that favorable interaction between side-chains are optimized. The protein backbone is kept fixed during this stage.  

This algorithm is known as a global optimization algorithm since it can "walk" both "up and down hill" in energy. All side-chain rotamer permutations are searched using an advanced version of Dead-End Elimination for many-body potential energy functions.


Naming Conventions:

Initial Structures: GENE_starting residue # - ending residue # _initials of the site the model came from.pdb
_SM: the model came from Swiss-Model
_MB: the model came from ModBase

Refined Structures: GENE_starting residue # - ending residue # _FFX.pdb
_FFX: indicates that this structure was refined using the two optimization algorithms in the Force Field X (FFX) polarizable force field.

The models in this repository can be viewed using molecular visualization systems, such as PyMol.  Viewing these models may be helpful for investigation of mutation sites, etc. 
