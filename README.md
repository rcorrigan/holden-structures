holden-structures
=================

Atomic resolution protein structures of genes screened by the Holden Comprehensive Cancer Center.

The initial models that we have refined are from either Swiss-Model or ModBase, indicated by the initials following their sequence length (see Naming Conventions, below).  These original structures are refined using two different optimization algorithms, developed by the Michael Schnieders lab at the University of Iowa:

  Algorithm 1. is a local algorithm; it will computationally “walk down hill” in energy until it finds the lowest possible energy (i.e. it looks for the lowest energy position for each atom to be in and when it finds a certain minimum energy, defined by convergence criteria, it stops there).
  
  Algorithm 2. is a rotamer optimization algorithm. Rotamers are branches that protrude from the main protein structure and can interact with each other to varying degrees, depending on the protein folding.  
  
Proteins prefer to fold into states with the lowest rotamer interaction possible leading to a more stable, lower-energy structure.

The rotamer optimization algorithm determines the optimal orientation of each rotamer so they have the least possible interaction with other rotamers around them while maintaining the protein backbone in a fixed position.  

This algorithm is known as a global algorithm since it can “walk” both “up and down hill” in energy until it finds the absolute minimum energy structure. This differs from a local optimizer in that it is willing to leave a low energy state in order to see if there is a state of even lower energy the algorithm can find. 


Naming Conventions:

Initial Structures: GENE_starting residue # - ending residue # _initials of the site the model came from.pdb
_SM: the model came from Swiss-Model
_MB: the model came from ModBase

Refined Structures: GENE_starting residue # - ending residue # _FFX.pdb
_FFX: indicates that this structure was refined using the two optimization algorithms in the Force Field X (FFX) polarizable force field.

The models in this repository can be viewed using molecular visualization systems, such as PyMol.  Viewing these models may be helpful for investigation of mutation sites, etc. 
