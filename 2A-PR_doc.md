Module ir_a2a_pagerank
======================

Classes
-------

`PageRank()`
:   Class used to find the page ranks
      1. with random teleportations
      2. without random teleportations
    using the following techniques to find the principle left eigenvector-
      1. using the numerical linear algebra package
      2. using the Power iteration method
    
      Class variables:
        n: number of nodes in the web graph
        e: number of edges/connection in the web graph
        alpha: hyperparameter indicating probability of random teleportation
        adj: adjacency matrix
        edges: list containing tuples indicating the start and end point of the connections
    
        PT: probability transition matrix for case without random teleportations
        PT_tele: probability transition matrix for case with random teleportations
        left_eig1: pr left eigenvector for PT_tele found using lin alg library
        left_eig2: pr left eigenvector for PT_tele found using power iteration
        left_eig3: pr left eigenvector for PT found using lin alg library
        left_eig4: pr left eigenvector for PT found using power iteration
    
    Function for initializing and taking input necessary for the algorithm

    ### Methods

    `calc_PT(self)`
    :   Function to find PT

    `calc_PT_tele(self)`
    :   Function to find PT_tele

    `power_iter(self, prob_mat, iter=1000)`
    :   Finding the principle left eigen vector for prob_mat using Power Iteration
        Parameter:
          prob_mat: n*n probability transition matrix for which we need to find the pr left eigen vector
        Return value:
          left_eig: list representing the pr left eigen vector

    `print_res(self, page_ranks)`
    :

    `run(self)`
    :   Function to be called in order to run the Page Rank algorithm

    `using_alg_package(self, prob_mat)`
    :   Finding the principle left eigen vector for prob_mat using lin alg library
        Parameter:
          prob_mat: n*n probability transition matrix for which we need to find the pr left eigen vector
        Return value:
          left_eig: list representing the pr left eigen vector