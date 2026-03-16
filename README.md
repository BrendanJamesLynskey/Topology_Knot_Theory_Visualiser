# Topology & Knot Theory Visualiser

An interactive single-file HTML application for exploring surfaces, knots, and topological invariants through 3D visualisations.

### [Launch App](https://brendanjameslynskey.github.io/Topology_Knot_Theory_Visualiser/)

---

## Mathematical Background

### Surfaces and Classification

A **surface**, or **2-manifold**, is a topological space in which every point has a neighbourhood homeomorphic to an open subset of ℝ². Surfaces are the central objects of low-dimensional topology. The **Classification Theorem for Compact Surfaces** states that every compact, connected surface without boundary is homeomorphic to exactly one of the following: the sphere S², a connected sum of n tori T² # T² # ⋯ # T² (an orientable surface of genus n), or a connected sum of k copies of the real projective plane ℝP² (a non-orientable surface). This theorem, remarkable for its completeness, reduces the classification of all closed surfaces to a single non-negative integer together with an orientability flag.

The **Euler characteristic** χ = V − E + F is a topological invariant that can be computed from any polyhedral decomposition (or, more generally, any CW-complex structure) on a surface. For an orientable surface of genus g, one has χ = 2 − 2g; for a connected sum of k projective planes, χ = 2 − k. The Euler characteristic is additive under connected sum: χ(M # N) = χ(M) + χ(N) − 2. Together with orientability, it completely determines the homeomorphism type of a closed surface, making it one of the most powerful yet elementary invariants in topology.

**Orientability** captures whether a surface admits a consistent choice of "clockwise" across its entire extent. Formally, a surface is orientable if and only if it does not contain a Möbius band as a subspace. The **Möbius strip** — a surface with boundary obtained by identifying one pair of opposite edges of a rectangle with a half-twist — is the fundamental example of non-orientability. It has a single boundary component and Euler characteristic zero. The **Klein bottle**, obtained by identifying both pairs of opposite edges of a square (one pair with a reversal), is the simplest closed non-orientable surface; it cannot be embedded in ℝ³ without self-intersection, though it admits an immersion. The real projective plane ℝP², which can be constructed by identifying antipodal points on S², is likewise non-orientable and non-embeddable in ℝ³.

### Knot Theory

A **knot** is a smooth (or piecewise-linear) embedding of the circle S¹ into the 3-sphere S³ (equivalently, into ℝ³ via one-point compactification), considered up to **ambient isotopy** — that is, two knots are equivalent if there exists a continuous family of diffeomorphisms of the ambient space carrying one to the other. The simplest knot is the **unknot** (a standard round circle); the simplest non-trivial knot is the **trefoil** 3₁, which has three crossings in its minimal diagram. A **link** generalises the concept to multiple disjoint embedded circles.

A **knot diagram** is a projection of a knot onto a plane, decorated with crossing information (which strand passes over, which under). Reidemeister's theorem (1927) establishes that two knot diagrams represent the same knot type if and only if they are related by a finite sequence of three local moves: **Type I** (adding or removing a twist/loop), **Type II** (adding or removing two crossings where one strand passes over another), and **Type III** (sliding a strand over or under a crossing). These moves form the combinatorial foundation of knot theory, reducing a continuous problem to a discrete one.

**Knot invariants** are quantities or algebraic objects assigned to knots that remain unchanged under ambient isotopy and thus can distinguish inequivalent knots. The **crossing number** c(K) is the minimum number of crossings over all diagrams of K. The **unknotting number** u(K) is the minimum number of crossing changes needed to convert K into the unknot. More powerful are polynomial invariants: the **Alexander polynomial** Δ(t), introduced by J. W. Alexander in 1928 and computable from the Seifert matrix of a knot, was the first polynomial knot invariant. The **Jones polynomial** V(t), discovered by Vaughan Jones in 1984, is strictly stronger and has deep connections to statistical mechanics and quantum groups. The **HOMFLY-PT polynomial** P(l, m), discovered independently by several groups in 1985, generalises both the Alexander and Jones polynomials into a two-variable invariant. **Torus knots** T(p, q), which lie on the surface of a standard torus in ℝ³, winding p times around the meridional direction and q times around the longitudinal direction, form one of the best-understood families. A torus knot T(p, q) is non-trivial precisely when both |p| ≥ 2 and |q| ≥ 2, and T(p, q) is equivalent to T(q, p).

### Fundamental Polygons and the Classification Theorem

Every closed surface can be represented as a **fundamental polygon**: a 2n-gon with edges identified in pairs according to a **word** that encodes the topology completely. For the torus, the identification word is aba⁻¹b⁻¹; for the Klein bottle, abab⁻¹; for the real projective plane, aa (a digon with both edges identified in the same direction); for the sphere, aa⁻¹. The proof of the Classification Theorem proceeds by showing that any such identification word can be reduced, via a sequence of combinatorial operations (cutting, re-gluing, and re-labelling), to one of the standard normal forms: aa⁻¹ for S², a₁b₁a₁⁻¹b₁⁻¹a₂b₂a₂⁻¹b₂⁻¹⋯aₘbₘaₘ⁻¹bₘ⁻¹ for the orientable surface of genus m, or a₁a₁a₂a₂⋯aₖaₖ for the non-orientable surface with k crosscaps.

The **fundamental group** π₁ of a surface can be read directly from its fundamental polygon. For the torus, one obtains π₁(T²) ≅ ℤ × ℤ, generated by the two loops a and b with the single relation aba⁻¹b⁻¹ = 1 (i.e., the generators commute). For a closed orientable surface of genus g ≥ 2, the fundamental group has 2g generators a₁, b₁, …, aₘ, bₘ subject to the single relation [a₁, b₁][a₂, b₂]⋯[aₘ, bₘ] = 1, where [a, b] = aba⁻¹b⁻¹ denotes the commutator. These groups are non-abelian for g ≥ 2, reflecting the richer topology of higher-genus surfaces. The Klein bottle has fundamental group ⟨a, b | abab⁻¹ = 1⟩, which is non-abelian and contains a subgroup isomorphic to ℤ × ℤ of index 2.

## History

The origins of topology can be traced to Leonhard **Euler**, whose 1736 solution to the Königsberg bridge problem — demonstrating that no walk could cross each of the city's seven bridges exactly once — is widely regarded as the first theorem in graph theory and, more broadly, the birth of topology as a mathematical discipline. In 1758, Euler discovered the polyhedron formula V − E + F = 2 for convex polyhedra, an identity that would eventually be recognised as a manifestation of the Euler characteristic of the 2-sphere. These contributions established the principle that certain problems depend not on metric quantities (lengths, angles) but on qualitative, structural properties of spaces — the guiding idea of topology.

The mid-nineteenth century saw the emergence of surfaces as objects of independent study. In 1858, August Ferdinand **Möbius** and Johann Benedict **Listing** independently discovered the one-sided strip that now bears Möbius's name, providing the first explicit example of a non-orientable surface. Bernhard **Riemann**, in his 1857 doctoral work and subsequent papers, introduced the notion of Riemann surfaces as branched covering spaces of the complex plane, linking topology to complex analysis and algebraic geometry. His concept of genus — the number of "handles" on a surface — gave topologists their first systematic invariant for classifying surfaces. In 1882, Felix **Klein** described the surface now known as the Klein bottle, a closed non-orientable surface that cannot be realised in ℝ³ without self-intersection, further expanding the menagerie of topological objects beyond ordinary geometric intuition.

Henri **Poincaré**'s landmark 1895 paper *Analysis Situs* founded the discipline of algebraic topology. Poincaré introduced the fundamental group π₁, defined homology groups, formulated the concept of duality for manifolds, and posed the famous **Poincaré conjecture** — that every simply connected, closed 3-manifold is homeomorphic to S³. This conjecture would resist proof for over a century and drive enormous progress in geometric topology. The rigorous **Classification Theorem for Compact Surfaces** was established in stages: Max **Dehn** and Poul **Heegaard** gave an early version in their 1907 *Enzyklopädie* article, Henry Roy **Brahana** provided a cleaner combinatorial proof in 1921, and the definitive modern treatment appeared in the 1934 textbook *Lehrbuch der Topologie* by Herbert **Seifert** and William **Threlfall**, which also introduced the Seifert matrix construction central to knot theory.

The systematic study of knots began in the 1870s, motivated by Lord Kelvin's (William **Thomson**'s) speculative "vortex theory of atoms," which proposed that atoms were knotted vortex tubes in the aether. Peter Guthrie **Tait** undertook the first serious tabulation of knots, classifying all prime knots up to seven crossings by hand — a monumental combinatorial effort. Although the physical theory was abandoned, the mathematical structures endured. J. W. **Alexander** introduced the first polynomial knot invariant, the Alexander polynomial Δ(t), in 1928, demonstrating that algebraic methods could distinguish knots that were beyond the reach of purely combinatorial techniques. A revolution occurred in 1984 when Vaughan **Jones**, working on von Neumann algebras, unexpectedly discovered a new polynomial invariant — the **Jones polynomial** V(t) — which was strictly stronger than the Alexander polynomial and revealed deep connections between knot theory, statistical mechanics (the Yang–Baxter equation), and quantum groups. This discovery catalysed the development of quantum topology and topological quantum field theories (TQFTs). In 2003, Grigori **Perelman** posted a proof of the Poincaré conjecture using Richard Hamilton's **Ricci flow** programme, settling one of the seven Millennium Prize Problems and confirming William **Thurston**'s far-reaching **Geometrisation Conjecture**, which classifies all compact 3-manifolds in terms of eight model geometries. Modern topology continues to expand: TQFTs provide invariants of 3- and 4-manifolds with connections to theoretical physics; knot invariants find application in molecular biology (DNA topology) and chemistry; and **persistent homology**, a technique from topological data analysis, applies algebraic topology to extract qualitative features from high-dimensional data sets, bringing the methods pioneered by Euler, Riemann, and Poincaré into the domain of modern data science.

## Features

### 1. Surface Gallery
- **3D wireframe renderings** of classical surfaces using perspective projection on HTML5 Canvas
- Surfaces included: Mobius strip, Klein bottle, Torus, Sphere, Cross-cap (Real Projective Plane)
- Click-and-drag rotation, scroll-to-zoom
- Adjustable parameters (e.g., torus R/r ratio, Mobius twist count)
- Properties displayed: Euler characteristic, orientability, genus, boundary info

### 2. Euler Characteristic Calculator
- **Interactive simplicial complex editor** on a 2D canvas
- Click to add vertices, Shift+click two vertices to add edges, Ctrl+click inside a triangle to add faces
- Right-click to delete vertices
- Real-time computation and display of V - E + F = chi
- Preset examples: Tetrahedron, Cube, Octahedron, Torus triangulation

### 3. Knot Explorer
- **3D knot renderings** with depth-based crossing visualisation (over/under clearly shown)
- Common knots: Trefoil (3_1), Figure-Eight (4_1), Cinquefoil (5_1)
- Torus knot T(p,q) with adjustable p and q parameters
- Knot invariants displayed: crossing number, unknotting number, Alexander polynomial
- Rainbow color gradient along the knot curve for visual clarity

### 4. Fundamental Polygons
- **Edge identification diagrams** showing how surfaces are built from squares
- Surfaces: Torus (aba^{-1}b^{-1}), Klein bottle (abab^{-1}), RP^2 (abab), Sphere
- Animated folding/gluing process
- Adjustable animation speed

## Controls

| Action | Surface Gallery / Knot Explorer | Euler Calculator |
|--------|--------------------------------|------------------|
| Left-click + drag | Rotate 3D view | Add vertex |
| Scroll wheel | Zoom in/out | -- |
| Shift + click | -- | Add edge (click two vertices) |
| Ctrl/Cmd + click | -- | Add face (click inside triangle) |
| Right-click | -- | Delete vertex |

## Technical Details

- Pure vanilla JavaScript, HTML5 Canvas
- No WebGL -- all 3D rendering uses software perspective projection
- Wireframe rendering with depth-based alpha for visual depth cues
- Knot crossings rendered via depth-sorted segments with dark outlines
- Dark theme matching the project's math visualiser aesthetic
