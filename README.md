Nystrom Method for faster Computation

The purpose of Nystrom method is to improve the time complexity in matrix creation.

Dataset size = (s, 2)
1) Use brute force to make a KNN graph matrix(P: pxp) by using only 5% of the dataset with euclidean distance as the parameter.
2) Again create a KNN graph matrix(R: pxl), where l = s-p
3) Approximated Affinity Matrix(A: lxl):  inv(R)* P* R
4) Create a degree matrix(D: lxl), whose diagnol is the sum of rows of A and rest elements same as A.
5) Laplacian Matrix(L: lxl) = D-A
6) Find the eigen values and eigen vectors of L and use the first 4 eigen values to create clusters using K Means.
