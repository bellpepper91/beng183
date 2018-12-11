# ChIP-seq (Chromatin Immunoprecipitation followed by Next-Generation Sequencing)

Samuel Beppler 2018

1. [Introduction](#1)
2. [Experimental Technique](#2) 
3. [Bioinformatic Analysis](#3)

---

## 1. Introduction<a name="1"></a>

*intro text

---

## 2. Experimental Technique<a name="2"></a>

The method can be summarized in the following four steps:

2.1 [Crosslink](#2.1)<br>
2.2 [Shear DNA](#2.2)<br>
2.3 [Immunoprecipitate](#2.3)<br>
2.4 [Purify DNA and Prepare for Sequencing](#2.4) 

#### 2.1 Crosslink<a name="2.1"></a>

![CrosslinkDiagram](http://www.jbc.org/content/290/44/26404/F1.medium.gif "Diagram of Crosslinking")

**[Figure 1](http://www.jbc.org/content/290/44/26404.full).** Formaldehyde (*red dots*) reversably crosslinks associated proteins (*blue* and *purple*) and DNA (*black curve*) within the environment of a cell or nucleus. DNA is shown wrapped around nucleosomes (grey circles). **Figure provibed by Hoffman *et al*. The Journal of Biological Chemistry (2015).**

Crosslinking is a reversable process that covalently bonds associated molecules, such as proteins and DNA. In ChIP, we are interested in chromatin and as such, we focus on chromatin-protein interactions. Since chains of associated proteins can be crosslinked together, chromatin-protein-protein-... interactions are also of interest. Common proteins of interest are transcription factors and histones (with specific modifications).

#### 2.2 Shear DNA<a name="2.2"></a>

![ShearedDiagram](https://github.com/bellpepper91/beng183/blob/master/sheared.jpg?raw=true "Diagram of Sheared DNA Complexes")

**Figure 2.** DNA is sheared to sequencable length while complexes are conserved.

DNA is sonicated to shear it to a sequencable length. Crosslinks are not broken in this process because the covalent bonds are strong. The result is small fragments of chromatin in complex with proteins that associated with that small fragment.

#### 2.3 Immunoprecipitate<a name="2.3"></a>

![Immunoprecipitation](https://github.com/bellpepper91/beng183/blob/master/immunoprecipitation.jpg?raw=true "Diagram of Immunoprecipitation")

**Figure 3.** **A)** The structure of the selection method. A magnetic bead is attached to the antibody. The antibody ("*immuno*") selects specifically for a protein of interest. **B)** A magnet is used to pull the selected complexes aside ("*precipitation*").

Immunoprecipitation refers to the two step process of selecting and retrieving a protein of interest (and accompanying complexes) using antibodies.
- Selection employs the ability of antibodies to specifically bind to particular proteins of interest. This property makes them good selective markers.
- Retrieval is facilitated by using antibodies attached to magnetic beads. The magnetic bead provides a mechanism for recovering the antibody, along with any complexes of protein and/or DNA bound to it. In practice, unselected DNA fragments and proteins are aspirated off while the selected complexes are immunoprecipitated.

#### 2.4 Purify DNA and Prepare for Sequencing<a name="2.4"></a>

In order to prepare the selected DNA for sequencing it must be purified and 
undergo standard sequencing library preparation.
Purifying the DNA starts with reverse crosslinking the complexes. This process occurs spontaneously under heat and is commonly done in the presence of Proteinase K to protect the DNA from nucleases.

Sequencing Library Preparation varies depending on which platform is used however a common option is paired-end Illumina sequencing, which requires poly-A tails capped with adapters.

---

## 3. Bioinformatic Analysis<a name="3"></a>

The reads sequenced in this technique are specific for sequences associated (to any degree) with the protein of interest.

#### Map to Genome
Reads are aligned to the genome to determine their origin. The number of reads mapped to each position (or region) is counted. The frequency of reads mapped to a 
particular region reflects the frequency that region associates with the protein 
of interest under the experimental conditions. 
#### Visualization

![UCSCBrowser](https://github.com/bellpepper91/beng183/blob/master/ucsc_genome.png?raw=true "UCSC Browser Screenshot")

**Figure 4.** An image of the UCSC Genome Browser. The data used to produce the 
bottom two tracks (H3K4Me1 and H3K4Me3) come from ChIP-seq experiments. **Figure provided by Kent *et al*. Genome Research (2002).**

Visualizing these data helps interpret them. The UCSC Genome Browser visualizes 
ChIP-seq data by plotting the frequency of mapped reads as peaks alongside the 
location of genes and other genomic elements (see Figure 4).

#### Applications
ChIP-seq is a versatile technique because any chromatin-associated protein 
can be selected for, under many different conditions. Common proteins to select for include modified histones and transcription factors. 

Selecting for histone modifications provides information on the state of chromatin (ie. euchromatin vs heterochromatin) in a given environment. 
Differences between cell types, for example, can help 
uncover the relationship between genes and cell differentiation.

Selecting for transcription factors provides information on how and where 
they have their effect at the genomic level. The site that a sex determining 
factor binds DNA, for example, can be seen through ChIP-seq data and may 
elucidate the purpose of a particular gene.
 
## References
Hoffman EA, Frey BL, Smith LM, Auble DT. Formaldehyde crosslinking: a tool for the study of chromatin complexes. *Journal of Biochemistry* (2015).

Kent WJ, Sugnet CW, Furey TS, Roskin KM, Pringle TH, Zahler AM, Haussler D. The Human Genome Browser at UCSC. *Genome Research* (2002).


