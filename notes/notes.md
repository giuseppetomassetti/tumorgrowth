# Epithelial cancers

Epithelia are **sheets of cells** that line the walls of cavities and channels or, in the case of skin, serve as the outside covering of the body.  Beneath the epithelial cell layers in each of these tissues lies a *basement membrane*, which separates the epithelial cells from the underlying layer of supporting connective tissue cells, termed the *stroma*. **The majority of human tumors arise from *epithelial tissues***. Epithelial cancers spawn the most common human cancers—the *carcinomas*. These tumors are responsible for more than 80% of the cancer-related deaths in the Western world. ( [^1], section 2.2).

The invasion by carcinoma cells into the stroma is a consequence of several concurrent mechanisms. At the borders of many carcinomas, epithelial cancer cells often change gene expression programs and *take on attributes of the nearby stromal cells* of mesenchymal origin. 

However, some research suggests that *alterations in the mechanical behavior of cancer cells* have an important role in tumorigenesis. For example, [Sailbreaux et al. (2019)](https://doi.org/10.1038/s41586-019-0891-2) argue observe that in in pancreatic tubular epithelia of mice the diameter of the source epithelium instructs the morphology of growing tumors, and provide an explanation based on a mechanical model whereby *spontaneous bending* of the epithelial tissue takes place due to the interplay of cytoskeletal changes in transformed cells and the existing tubular geometry. This is exemplified in the following figure, which shows images of tumors bulging out for a small radius and bulging out for a large radius.

<img src="notes.assets/Annotation 2020-05-14 121409.png" style="height:200px" class="center"/>

# The vertex model

A popular model for the mechanical behavior of epithelial tissues is the so-called “vertex model”, introduced in by [Nagai & Honda in 2001](https://scholar.google.com/scholar?cluster=4196662009164092687&hl=en&as_sdt=0,5). This model describes the evolution of a two-dimensional polygonal pattern through a gradient-flow model with an energy due to the interfacial tension on cell boundaries. The original formula by Nagai & Honda reads:
$$
U_{1}=\sum_{\langle i j\rangle} \sigma_{\alpha \beta}\left|\mathbf{r}_{i}-\mathbf{r}_{j}\right|.
$$

where $\sigma_{\alpha \beta}$ denotes the boundary energy per unit length between cells $\alpha$ and $\beta,$ and vertices $i$ and $j$ are at the ends of the boundary line. The sum is taken over all the boundaries $\langle i j\rangle .$ The boundary energy per unit length can depend on the type (or the state) of cells $\alpha$ and $\beta .$ 

This model has been further extended to take into account [cortical tension](), and the compressibility of the cytoskeleton by an expression that includes *quadratic terms*. For example, the paper by [Bargmann et al.](http://dx.doi.org/10.1093/imammb/dqx008) write
$$
U\left(\left\{\mathbf{R}_{\alpha}^{i}\right\} ; \Gamma, \Lambda\right)=\sum_{\alpha=1}^{N_{c}}\left\{\frac{1}{2}\left(A_{\alpha}-1\right)^{2}+\frac{1}{2} \Gamma\left(L_{\alpha}-L_{0}\right)^{2}-U_{0}\right\}.
$$

# Plate models

The vertex model has been developed with the main focus on the behavior of flat epithelial tissues. To describe shape transformations associated to stroma invasion, such as bending deformations, several plate models have been developed, which consider a epithelial tissue as a two-dimensional polygonal pattern but allows the vertices to move out of plane, penalizing energetically bending deformations.

[Murisic et al. (2015)](http://www.lps.ens.fr/~hakim/15biophysj.pdf) introduce the following expression for the bending energy
$$
E_{\rm bend}=B \sum_{e^{\prime}}\left(1-\mathbf{N}_{f_{1}\left(e^{\prime}\right)} \cdot \mathbf{N}_{f_{2}\left(e^{\prime}\right)}\right)
$$
where the index $e^{\prime}$ runs over interior edges, i.e., edges belonging to two adjacent faces $f_{1}\left(e^{\prime}\right)$ and $f_{2}\left(e^{\prime}\right) $, and $\mathbf N_f$ denotes the unit normal to face $f$. 

<img src="notes.assets/Annotation 2020-05-14 115723.png" style="height:200px" class="center"/>

[Misra et. al (2016)](/notes.assets/misra2016.pdf), write
$$
E_{b e n d}=\beta \sum\left(\left(1-\mathbf{N}_{S 2\left(j^{\prime}\right)} \cdot \mathbf{N}_{S 1\left(j^{\prime}\right)}\right)-k_{j^{\prime}}\left(-\left(\mathbf{N}_{S 2\left(j^{\prime}\right)}-\mathbf{N}_{S 1\left(j^{\prime}\right)}\right) \cdot \mathbf{u}_{j^{\prime}}\right)\right.
$$
where the sum is over all interior edges $j^{\prime},$ i.e., edges shared by two adjacent cells $s 1\left(j^{\prime}\right)$ and $s 2\left(j^{\prime}\right) .$ This term represents the bending energy term, where $\beta$ is the bending elasticity coefficient and $k_{j^{\prime}}$ represents the local natural curvature of the shell ( $k_{j^{\prime}}$ is roughly the rest value of the dihedral angle between the faces adjacent to edge $j^{\prime}$. In this formula, S2.1 for details). Here $N_{s}$ denotes the outward unit normal to a cell $s$ (i.e., the normal vector of each cell points toward the outside of the closed shell). The value $\boldsymbol{u}_{j^{\prime}}$ is the unit vector joining the cell centers,
$$
\boldsymbol{u}_{j^{\prime}}=\frac{\boldsymbol{C}_{s 2\left(j^{\prime}\right)}-\boldsymbol{C}_{s 1\left(j^{\prime}\right)}}{\left|\boldsymbol{C}_{s 2\left(j^{\prime}\right)}-\boldsymbol{C}_{s 1\left(j^{\prime}\right)}\right|}
$$
where $C_{32\left(j^{\prime}\right)}$ and $C_{s 1\left(j^{\prime}\right)}$ are cell centers, defined as the mean position of the nodes belonging to the cells $s 1$ and $s 2$, respectively.  

# The 3D vertex model

The 3D vertex model is a nonplanar graph where vertices are arranged on the apical and on the basal surface.

<img src="notes.assets/Annotation 2020-05-14 122936.png" style="height:200px" class="center"/>

This model was introduced in [Bielmeier et al 2016. ](https://www.pks.mpg.de/fileadmin/user_upload/MPIPKS/group_pages/BiologicalPhysics/juelicher/publications/2016/ICbDFCDCEaCF2016.pdf) to model cyst formation in relate spontaneous bending to the **imbalance** between apical and basal cortical tension. <img src="notes.assets/Annotation 2020-05-14 122936b.png" style="height:200px" class="center"/>

Bielmeier et al. write, for the energy:
$$
W=\underbrace{\sum_{\alpha}-P_{\alpha} V_{\alpha}+\sum_{k} T_{k} A_{k}+\sum_{i j} \Lambda_{i j} l_{i j}}_{W_{i}}
$$
where $T_k$ is now the surface tension. 

[^1]: [R. A. Weinberg: “The Biology of Cancer, 2nd ed.”, Garland Science, New York and London, 2014](notes.assets/Weinberg_2013.pdf)

