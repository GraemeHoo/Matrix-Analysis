# Matrix-Analysis

This is a python library for basic matrix computation and analysis, topics(those are not included in numpy or scipy) of which include but are not limited to, special matrix transformation like householder, algorithms for orthogonal projection, eigenvalue problem with spectrum decomposition, and some popular matrix factorization methods for nonnegative matrix factorization.

### Nonnegative Matrix Factorization

Nonnegative matrix factorization is a computational technique of dimensional reduction of a given data to uncover the latent factors embedded in higher dimensions. Unlike traditional matrix decomposition methods such as SVD and full rank decomposition, the non-negativity constraint imposed by NMF is useful for learning part-based representations. Secondly, since that in many real world applications such as image and face recognition, the data matrices people are dealing with are usually nonnegative, and that intuitively parts are generally combined additively (not subtracted as what many face recognition problems using SVD do, which generate not nonnegative eigenfaces) to form a whole picture and physiological principles assume that humans learn objects as part-based, the non-negativity thereby enhances meaningful interpretations of information given by the data matrix and is applicable to real world problems.  

##### Definition

Suppose a nonnegative matrix <img src="http://chart.googleapis.com/chart?cht=tx&chl=$A \in R^{M \times N}$" style="border:none;"> is given. NMF returns the decomposed representation of $A$ with nonnegative matrix  <img src="http://chart.googleapis.com/chart?cht=tx&chl=$W$" style="border:none;"> and <img src="http://chart.googleapis.com/chart?cht=tx&chl=$H$" style="border:none;"> by solving a nonconvex optimization problem defined with Frobenius norm.

<img src="http://chart.googleapis.com/chart?cht=tx&chl=$$min \; f(W, \; H) = {|| A-WH^T ||}^2_F $$" style="border:none;">
,     
<img src="http://chart.googleapis.com/chart?cht=tx&chl=  subject \ to \ W \ge 0, \ H \ge 0" style="border:none;">

Since this optimization problem is nonconvex, only the local minimum should be expected from any good algorithm.


##### Algorithms

* **HALS**

![](/pic/1.PNG)

![](/pic/2.PNG)
