# Farrell-Tate_cohomology_computations
Farrell-Tate cohomology computations, joint work with Tuan Anh Bui and Matthias Wendt

The authors have run a machine computation, starting with Voronoı̈ cell complexes with an action of
GL_3(O_Q(√−m)), constructed by Sebastian Schönnenbeck’s software described in his paper
"Resolutions for unit groups of orders, Journal of Homotopy and Related Structures 12 (2017), no. 4, 837–852, DOI 10.1007/s40062-016-0167-6".
This software has been released on 

https://github.com/schoennenbeck/VMH-ImaginaryQuadraticNumberFields

Pertinent cell complexes which it produces are available in the archive file

[GL3ImaginaryIntegers.tar.gz](https://github.com/arahm/Farrell-Tate_cohomology_computations/files/8797126/GL3ImaginaryIntegers.tar.gz)

These cell complexes can be loaded into the computer algebra system GAP with the package HAP (Homological Algebra Programming, developed and maintained by Graham J. Ellis).

More precisely, GL_3(O_Q(√−m)) acts on a certain space of quadratic forms, and there is an equivariant retraction to Ash’s well-rounded
retract. On the latter co-compact space, a suitable form of Voronoı̈’s algorithm yields an explicit cell structure with cell stabilizers and computable quotient space, as described by Braun, Coulangeon, Nebe and Schönnenbeck [3] in their paper
"Computing in arithmetic groups with Voronoı̈’s algorithm, J. Algebra 435 (2015), 263–285. Zbl 1323.16014".
In view of determining the parameters λ and µ of Theorem 1.1 of the paper by Bui, Rahm and Wendt, we want to extract the torsion subcomplexes from these Voronoı̈ cell complexes. Definition: For p a prime number, the p-torsion subcomplex is the set of all cells with stabilizers
containing some element(s) of order p. For the p-torsion subcomplex to be guaranteed to be a cell complex, and to consist only of fixed points
of order-p-elements (so to coincide with the p-singular part), we need a rigidity property: We want each cell stabilizer to fix its cell pointwise. This rigidity property is lacking on our Voronoı̈ cell complexes.
In theory, it is always possible to obtain this rigidity property via the barycentric subdivision. However, the barycentric subdivision of an n-dimensional cell complex can multiply the number of cells by (n + 1)! and thus easily let the memory stack overflow. In previous work of the authors, a cell subdivision algorithm was introduced (“rigid facets subdivision”), which refines the cell structure to get the rigidity
property, in an efficient enough way to treat the GL_3(O_Q(√−m))-cases. Its source code - which is contained in the GAP package HAP, and which is to be used by installing a recent version of HAP - is available here:

[TorsionSubcomplexesSubpackage.zip](https://github.com/arahm/Farrell-Tate_cohomology_computations/files/8797218/TorsionSubcomplexesSubpackage.zip)

[TorsionSubcomplexesSubpackage.tar.gz](https://github.com/arahm/Farrell-Tate_cohomology_computations/files/8797219/TorsionSubcomplexesSubpackage.tar.gz)

This allows us to extract the p-torsion subcomplexes.
