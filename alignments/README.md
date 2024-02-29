### Initial and Experimental Alignment Results of CE-related Ontologies

In our prior work, we have conducted a comprehensive survey of ontologies related to the CE domain and multiple cross-industry domains, and 37 ontologies were identified as presented in this [repository](http://w3id.org/CEON/catalogue).

Aiming to enhance the interoperability and reusability within the CE domain by providing alignments among related ontologies, we expanded our ontology base beyond the ones identified to include newcomers after the previous survey was published, and included the top-level ontology, EMMO (Elementary Multiperspective Material Ontology)[https://github.com/emmo-repo/EMMO].
Therefore, we have 6 CE-related ontologies, a number of domain-specific ontologies (5 for sustainability, 13 for materials, 14 for manufacturing, 9 for products, and 8 for logistics) and 1 top-level ontology (EMMO) to conduct ontology matching tasks on in this work.


#### Task a: CE-CE
The 6 CE-related ontologies are: BCAO, BiOnto, CAMO, CEO, DPPO and CEON. Therefore we have 15 alignments.

|        |  BiOnto | CAMO | CEO | DPPO | CEON |
|--------|--------|------|-----|------|------|
| BCAO   | [:heavy_check_mark:](./task_a/BCAO-BiOnto/)|[:heavy_check_mark:](./task_a/BCAO-CAMO/)|[:heavy_check_mark:](./task_a/BCAO-CEO/)|[:heavy_check_mark:](./task_a/BCAO-DPPO/)|[:heavy_check_mark:](./task_a/CEON-BCAO/)|
| BiOnto |        |[:heavy_check_mark:](./task_a/BiOnto-CAMO/)|[:heavy_check_mark:](./task_a/BiOnto-CEO/)|[:heavy_check_mark:](./task_a/BiOnto-DPPO/)|[:heavy_check_mark:](./task_a/CEON-BiOnto/)|
| CAMO   |        |      |[:heavy_check_mark:](./task_a/CAMO-CEO/)|[:heavy_check_mark:](./task_a/CAMO-DPPO/)|[:heavy_check_mark:](./task_a/CEON-CAMO/)|
| CEO    |        |      |     |[:heavy_check_mark:](./task_a/CEO-DPPO/)|[:heavy_check_mark:](./task_a/CEON-CEO/)|
| DPPO   |        |      |     |      |[:heavy_check_mark:](./task_a/CEON-DPPO/)|

#### Task b: CEON-IndusDom
##### Sustainability Domain
For the sustainability domain, we have 5 ontologies which are BONSAIcore, ENVO, SAREF4ENVR, SAREF4ENVI, SDGIO.
|      | BONSAIcore | ENVO | SAREF4ENVR | SAREF4ENVI | SDGIO |
|------|------------|------|------------|------------|-------|
| CEON |[:heavy_check_mark:](./task_b/CEON-SU/CEON-BONSAIcore/)|[:heavy_check_mark:](./task_b/CEON-SU/CEON-ENVO/)|[:heavy_check_mark:](./task_b/CEON-SU/CEON-SAREF4ENVR/)|[:heavy_check_mark:](./task_b/CEON-SU/CEON-SAREF4ENVI/)|[:heavy_check_mark:](./task_b/CEON-SU/CEON-SDGIO/)|
##### Materials Doamin
For the materials domain, we have  13 ontologies which are AMO, BUILDMAT, BWMDDomain, IOFcore, MATONTO, MDO, MPO, NMRVOCAB, PMDco, MECH, MSEO, MTO, MAMBO.
|      | AMO | BUILDMAT | BWMDDomain | IOFcore | MATONTO | MDO | MPO | NMRVOCAB | PMDco | MECH | MSEO | MTO | MAMBO |
|------|-----|----------|------------|---------|---------|-----|-----|----------|-------|------|------|-----|-------|
| CEON |     |          |            |         |         |     |     |          |       |      |      |     |       |
##### Manufacturing Domain
For the manufacturing domain, we have 14 ontologies which are AMO, BWMDDomain, CHAMP, COMPOSION, GPO, GRACE, IOFcore, ManuService, MSDL, MSOOFM, PSS,SAREF4INMA, VERONTO, ZBRE4K.
|      | AMO | BWMDDomain | CHAMP | COMPOSION | GPO | GRACE | IOFcore | ManuService | MSDL | MSOOFM | PSS | SAREF4INMA | VERONTO | ZBRE4K |
|------|-----|------------|-------|-----------|-----|-------|---------|-------------|------|--------|-----|------------|---------|--------|
| CEON |     |            |       |           |     |       |         |             |      |        |     |            |         |        |
##### Product Domain
For the product domain, we have 9 ontologies which are AMO, BONSAIcore, BPO, CHAMP, GRACE, ManuService, PRONTO, UNSPSC, VERONTO.
|      | AMO | BONSAIcore | BPO | CHAMP | GRACE | ManuService | PRONTO | UNSPSC | VERONTO |
|------|-----|------------|-----|-------|-------|-------------|--------|--------|---------|
| CEON |     |            |     |       |       |             |        |        |         |
##### Logistics Domain
For the logistics domain, we have 8 ontologies which are COMPOSION, GPO, IMAMO, ManuService, MSOOFM, ROMAIN, SCONTO, SCOR.
|      | COMPOSION | GPO | IMAMO | ManuService | MSOOFM | ROMAIN | SCONTO | SCOR | VERONTO |
|------|-----------|-----|-------|-------------|--------|--------|--------|------|---------|
| CEON |           |     |       |             |        |        |        |      |         |
#### Task c: CEON-EMMO
