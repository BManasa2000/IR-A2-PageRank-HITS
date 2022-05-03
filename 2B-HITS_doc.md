Module ir_a2b_hits-2
====================

Functions
---------

    
`driver()`
:   driver code

Classes
-------

`HITS(G)`
:   Class for implementing the HITSalgorithm
    Class variables:
      query: list containing the word tokens in the query string
      G: networkx graph (web graph)
      adj: adjacency matrix of G
      A: adjacency matrix of sub graph of G
      root_set: root set of the query
      base_set: base set of the query
      base_edges: edges present in the sub graph of G (edges b/w nodes of base_set)
      hub_score: list containing the hub scores of the nodes
      auth_score: list containing the auth scores of the nodes
    
    Function for taking input and initializing variables

    ### Methods

    `find_auth_score(self)`
    :   Function to find the auth scores of the nodes

    `find_base(self)`
    :   Function to find the base set

    `find_hub_score(self)`
    :   Function to find the hub scores of the nodes

    `find_root(self)`
    :   Function to find the root set

    `initialize_adj(self)`
    :   Function to change the adjacent matrix according to the edges in G

    `run(self)`
    :   Function to run the HITS algorithm

    `validating(self)`
    :   Function to compare results obtained from 
        find_auth_score and find_hub_score with results obtained by using the library function