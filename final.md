# ChIP-seq (Chromatin Immunoprecipitation followed by NGS Sequencing)

Samuel Beppler 2018

*Hyperlink table of contents here*

1. Introduction(#1)
2. Experimental Technique 
3. Bioinformatic Analysis

---

## 1. Introduction

*intro text

---

## 2. Experimental Technique

The method can be summarized in the following four steps:

2.1. Crosslink<br>
2.2 Shear DNA<br>
2.3. Immunoprecipitate<br>
2.4. Purify DNA and Prepare for Sequencing 

#### 1) Crosslink

![CrosslinkDiagram](http://www.jbc.org/content/290/44/26404/F1.medium.gif "Diagram of Crosslinking")

**[Figure 1](http://www.jbc.org/content/290/44/26404.full).** Formaldehyde (*red dots*) reversably crosslinks associated proteins (*blue* and *purple*) and DNA (*black curve*) within the environment of a cell or nucleus. DNA is shown wrapped around nucleosomes (grey circles). **Figure provibed by Hoffman *et al*. The Journal of Biological Chemistry (2015).**

Crosslinking is a reversable process that covalently bonds associated molecules, such as proteins and DNA. In ChIP, we are interested in chromatin and as such, we focus on chromatin-protein interactions. Since chains of associated proteins can be crosslinked together, chromatin-protein-protein-... interactions are also of interest. Common proteins of interest are transcription factors and histones (with specific modifications).

#### 2) Shear DNA

![ShearedDiagram](https://github.com/bellpepper91/beng183/blob/master/sheared.jpg?raw=true "Diagram of Sheared DNA Complexes")

**Figure 2.** DNA is sheared to sequencable length while complexes are conserved.

DNA is sonicated to shear it to a sequencable length. Crosslinks are not broken in this process because the covalent bonds are strong. The result is small fragments of chromatin in complex with proteins that associated with that small fragment.

#### 3) Immunoprecipitate

![Immunoprecipitation](https://github.com/bellpepper91/beng183/blob/master/immunoprecipitation.jpg?raw=true "Diagram of Immunoprecipitation")

**Figure 3.** **A)** The structure of the selection method. A magnetic bead is attached to the antibody. The antibody ("*immuno*") selects specifically for a protein of interest. **B)** A magnet is used to pull the selected complexes aside ("*precipitation*").

Immunoprecipitation refers to the two step process of selecting and retrieving a protein of interest (and accompanying complexes) using antibodies.
- Selection employs the ability of antibodies to specifically bind to particular proteins of interest. This property makes them good selective markers.
- Retrieval is facilitated by using antibodies attached to magnetic beads. The magnetic bead provides a mechanism for recovering the antibody, along with any complexes of protein and/or DNA bound to it. In practice, unselected DNA fragments and proteins are aspirated off while the selected complexes are immunoprecipitated.

#### 4) Purify DNA and Prepare for Sequencing

In order to prepare the selected DNA for sequencing it must be purified and 
undergo standard sequencing library preparation.
Purifying the DNA starts with reverse crosslinking the complexes. This process occurs spontaneously under heat and is commonly done in the presence of Proteinase K to protect the DNA from nucleases.

Sequencing Library Preparation varies depending on which platform is used however a common option is paired-end Illumina sequencing, which requires poly-A tails capped with adapters.

---

## 3. Bioinformatic Analysis
* Intro to analysis

#### Map to Genome
#### Visualization
#### Applications


