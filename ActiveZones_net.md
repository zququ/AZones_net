```mermaid
classDiagram
ActiveZones <|-- RIMs
ActiveZones <|-- RIMBPs
ActiveZones <|-- ELKS
ActiveZones <|-- liprins
ActiveZones <|-- Munc13s
ActiveZones <|-- Bassoon
ActiveZones <|-- Piccolo
VGCCs --> RIMs : cytoplasmic tails(PBM)
VGCCs --> RIMBPs : cytoplasmic tails(PRM)
CaM --> VGCCs : IQ motif
RIMs --> RIMBPs : PRM
RIMs --> ELKS : PDZ
RIMs --> CAST : PDZ
RIMs --> liprins : C2B
RIMs --> Munc13s : Zinc Finger
RIMs --> VGCCs : PDZ
RIMs --> Rab3 : Zinc Finger
RIMBPs --> RIMs : ALl three SH3
RIMBPs --> VGCCs : SH3
Munc13s --> RIMs : C-terminal C2A
Munc13s --> SNARE : C-terminal MUN
Munc13s --> CaM : CaMb
Bassoon --> Pra1 : zinc-finger
Piccolo --> Pra1 : zinc-finger
CAST <--> ELKS : hemo/hetero-oligomers
CAST --> Bassoon : 2nd CC to 3rd CC
CAST --> Piccolo : 2nd CC to 3rd CC
CAST --> RIMs : IWA
ELKS --> Bassoon : 2nd CC to 3rd CC
ELKS --> Piccolo : 2nd CC to 3rd CC
ELKS --> RIMs : IWA
ELKS *--* CAST
ELKS --> Rab6

synaptotagmin --> SNARE : C2B's KKKK

class ActiveZones{
+RIMs
+RIM-BPs
+ELKS
+liprins
+Munc13s
+Bassoon
+Piccolo
(key molecular organizers of AZs)
}

class RIMs{
+Zinc Finger : Rab3、Munc13
+PRM1 :
___ deletion greatly weaken
___ immediately preceding the PDZ domain aa 501–512
___ SH3-binding sequence
___ deletion greatly weakened LLPS
+PDZ : VGCC、ELKS
___ common structural domain
___ 80-90 AA
___ key role in anchoring receptor proteins in the membrane to cytoskeletal components
___ abundant protein interaction modules
___ often recognize short AA motifs at the C-termini of target proteins
+C2A : PIP2
___ regulates the fusion step of SVs exocytosis
+PRM2 :
___ 10 residues aa 871–880 from the N terminus of RIM1a-S
___ deletion greatly weakened LLPS
___ contains a "PFMPRR" sequence
___ fit class II SH3-binding
+PRM : RIM-BP --> SH3
___ proline-rich motif
___ SH3 domain binding
___ deletion greatly weakened LLPS
+C2B : Liprin、PIP2
___ forms weak dimer
(180 kDa)
(LLPS)
(tether Ca2+ channels to presynaptic active zones through PDZ)
}

class RIMBPs{
+SH3 : RIMS、VGCCs
___ LLPS
+FN3 : fibronectin type III
+FN3
+FN3
+SH3 : RIMS、VGCCs
___ LLPS
+SH3 : RIMS、VGCCs
___ LLPS
(LLPS)
}

class ELKS {
+CC : 
___ colied-coil
+CC
+CC
+CC
+IWA : RIMs
__ 
___ unique COOH-terminal amino acid motif
(ERC1)
(Rab6-binding protein)
(RAB6-Interacting)
(CAST Family Member 1) 
(ELKSa mainly in brain)
(longer ELKS don't have IWA)
(120 kDa)
}

class CAST {
+CC
___ colied-coil
+CC : Piccolo
+CC
+CC
+IWA : RIMs
___ unique COOH-terminal amino acid motif
(Cytomatrix at the active zone-associated structural protein)
(ERC2)
(Rab6-binding proteins)
(close relative to ELKS)
}

class liprins{
+ CC1
+ CC2 : ELKS, RIM
+ SAH : GIT
___ single-alpha-helical region
___ GIT -> G-protein-coupled receptor-kinaseinteracting protein
+ SAM1 : LAR, CASK
___ sterile-alpha-motif
+ SAM2 : LAR, CASK
___ LAR -> leukocyte common antigen-related receptor
___ CASK -> calcium/calmodulin-dependent serine protein kinase
+ SAM3 : LAR, CASK
}

class Munc13s{
+C2A : RIMs
___ 120 -> 140 AA
___ Ca dependent
___ targeting proteins to cell membranes
___ regulates the fusion step of SVs exocytosis
___ bind negatively charged phospholipids
+CaMb : calmodulin or named CaM
___ calmodulin-binding domain
+C1 : DAG with Ca2+
___ 50 AA
___ Cysteine-rich
___ recruitment of proteins to the membrane
___ binds to DAG and Phorbol esters 
___ -- which interact with PKC
+C2B : PIP & PIP2 with Ca2+
___ binds to PIP3 without Ca2+
___ binds to PIP2 with Ca2+
+MUN : SNARE
___ bind SNARE and/or Munc18?
+C2C
(200 kDa)
(very large multi-domain scaffold protein)
}

class VGCCs{
+ TM
___ 4x6 transmembrane regions, I-IV
+ PxxP or PRM : RIM-BP's SH3
___ conserved SH3-domain binding sequences
___ --RQLPGTP
___ critical for enrichment to RIM/RBP LLPS
+ PNGY
+ PBM : RIM's PDZ
___ PDZ binding motif
___ critical for enrichment to RIM/RBP LLPS
+ DxWC
___ C-terminal sequence motifs
___ DDWC for P/Q-type
___ DHWC for N-type
(Here, P/Q- and N-type channels)
(Voltage-gated calcium channels) 
(a permeability to Ca2+)
(VGCCs mediate Ca2+ influx )
(VGCCs are divided into)
(-- L-type (CaV1.1, CaV1.2, CaV1.3, and CaV1.4))
(-- P/Q-type (CaV2.1)) 
(-- N-type (CaV2.2))
(-- and R-type (CaV2.3))
}


class SNARE{
(soluble NSF attachment protein receptor)
(SNARE fusion machinery to connect clustered VGCCs)
(mediate vesicle fusion)
(classified as vesicular (v-) or target (t-) membrane SNAREs)
(secondly classified depending on whether a Q or R encoded)
(-- at highly conserved central hydrophilic layer)
(SV fusion: v-SNAREs synaptobrevin 2, Syb2 or VAMP)
(-- and t-SNAREs Syntaxin 1, Syx1)
(-- and SNAP-25)
}

class Bassoon {
+ zinc-finger
+ zinc-finger
+ CC
+ CC
+ CC : CAST
(420 kDa)}

class Piccolo {
+ zinc-finger
+ zinc-finger
+ CC
+ CC
+ CC : CAST
+ PDZ
+ C2
+ C2
(500 kDa)
(Aczonin)
}

class Pra1 {
(prenylated Rab3 A-associated protein-1)
(%control vesicle docking fusion)
(%mediating the action of Rab GTPases to the SNARE complexes)
(%regulate the trafficking of these vesicles to the axon during early synapse formation)
}

class Rab3 {
+ 
(G protein 3)
(GTPase)
(peripheral membrane proteins)
(generally possess a GTPase fold)
}

class Rab6 {
+
(G protein 6)
}

class synaptotagmin {
+TMD or TMR
___ N-terminal transmembrane region
+C2A : Ca2+ by Asp, 
___ coordinates 3 Ca2+
___ C-terminal C2 domain
+C2B : Ca2+ by Asp, SNARE and PIP2 by KKKK
___ KKK at polybasic region with acidic residus 
___ -- from syntaxin1 and SNAP-25 of SNARE
___ coordinates 2 Ca2+
___ C-terminal C2 domain
+ basic AA RR : membrane
___ at bottom end
(a Ca2+ sensor in pre-synaptic axon temrinal)
(-- for fast exocytosis)
(Syt1)
(contains two tandem C2 regions)
(-- homologous to PKC)
(coded by gene SYT1)
}

class CaM{
+ IQ motifs : regulate VGCCs
___ at C-terminal
}
```
