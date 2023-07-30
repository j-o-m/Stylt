# Stylt

A programming language built to enable its creator to code what they wanted in the way they wanted.

### Primary Design Criteria (**PDC**):
  
  - All language constructs and concepts are to be as minimal and orthogonal as possible, while maintaining maximal expressivity
  - Language Primitives (syntax, type theoretic, and semantically) are designed to be as low-level as possible
  - Maximize Expressivity and the Abilities of Computational Constructs
  - Well Defined and Specified Semantics
    - Categorical Semantics will be the primary method, but more traditional Denotational Semantics will be discussed
    - Operational Semantics will be presented at both the level of 'program' execution and for compilation (which are ultimately the same)
  - Syntax that enables the above considerations to be maximally expressive

### Design Decisions reached pursuing **PDC**:

  - Language Primitives motivated by a novel Process Calculus, Category Theory, Classical Linear Logic
    - The work by Spivak and others in Applied Category Theory on the Operad of Wiring Diagrams is particulary inspiring
  - 'Type' System which draws heavily from prior work in dependent types, modal logic, and *-Autonomous Categories
    - The work of Benton, Reed, Pfenning, et al on Modal Logic and Modal Type Theories and the subsequent work on Adjoint logic is a primary influence on the languages design
    - The continuing academic work on Multi-Mode Multi-Modal Dependent Type Theory influence several key aspects of the design
    - Type is used in scare quotes because, as Robert Constable said, Type Theory, and particulary the Function type  'is the most comprehensive theory of effective computability in the sense of deterministic sequential computation'; however, the basis for computation in the language is explicitly non-sequential (i.e. concurrent) and inherently non-deterministic (determinism must be forced on the system via 'types' and program design)
  - Semantics are expressed in a Static/Dynamic split presentation
    - The presentation is most clearly inspired by the work of Robert Harper as laid out in "Practical Foundations for Programming Languages"
    - However, there are several departures and significant alteration to accomodate the Modality Enforced Multi-Phase Semantics
  - Syntax is inspired and informed by the underlying composition-based semantics
  - Several common extentions to simple type theory (i.e. parametric and ad-hoc polymorphism, subtyping, type refinement, etc) are subsumed into the orthoganal basic constructs of the language and the interactions between those constructs
    - Parametric Polymorphism is achieved by combining dependent types and multi-stage programming
    - Ad-Hoc Polymorphism is achieved almost soley by multi-phase programming
    - Subtyping and Type Refinement are derivative achievements of the adjoint modal type theory
    - examples can continue...
   - Many common computational systems (i.e. lambda calculus) and type systems (i.e. session types) can be and SHOULD BE encoded in the language merely as distinct modes or types/Universes, not as privileged sublanguages or type theories

### A List of Anti-Features:

  - 'Developer Experience', at the expense of any PDC
    - An example would be having type inference at the expense of restrictions on expressivity
    - Another example would be having implicit arguments, types, modes where such would require a restriction on orthoganality
  - Simplification of base language to appeal to inexperienced users
  - Adherence to conventions, prior languages, or alledged concensus where such adherence would cut against any PDC
  - Removal or Restriction of capabilities to satisfy the needs of large scale development
    - There will be methods to allow large scale and distributed development to enforce requirements and specifications as needed
  - Sacrifice of PDC or specified development goals to satisfy or appeal to any external group of developers or commercial interests