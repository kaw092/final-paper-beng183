  
# Precision Medicine with an emphasize in  Pharmacogenomics 

### Overview:
#### 1. [Introduction to Precision Medicine](#1) 
#### 2. [A Brief History on Pharmacogenetics & Pharmacogenomics.](#2)
#### 3. [Personalizing drugs through pharmacogenomics.](#3) 
#### 4. [Applications of Bioinformatic tools:RNASeq](#4) 
#### 5. [Next steps in pharmacogenomics.](#5)
#### 6. [References](#6)


### Part 1: Introduction to Precision Medicine<a name="1"></a>

>According to NIH,Precision medicine is “an emerging approach for disease treatment and prevention that takes into account individual variability in genes, environment, and lifestyle for each person.”[1]  

That is to say, precision medicine is a specific form of therapeutics tailored for each subpopulation of patients through the use of tools such as pharmacogenomics; an offspring of pharmacogenetics. Precision medicine aims to customize health care so that each treatment is tailored for every subpopulation in every possible way. Our main focus is pharmacogenomics with emphasis on genomic approaches. 

![pm](pm.PNG)
### Part 2: A Brief History on Pharmacogenetics & Pharmacogenomics<a name="2"></a>

To be able to understand how pharmacogenomics came to be, we must first introduce Pharmacogenetics, a science that was recognized in the late 1950s which was dependent on “ the occurrence of unusual reactions to drugs on the basis of biochemical individuality.”[1]Revolving around studies that focus on “many different genetic changes of the enzyme that altered its functional characteristics”.[2] It later became clear that drug effects differentiate not only between populations, genders, and races but also between individuals. Drug metabolism also differs between individuals due to polymorphisms in drug-metabolizing enzymes leading to variability in the effectiveness of drugs. For example, some metabolizers may absorb more of a specific drug than others across individuals, leading some of the drugs as well as some doses to be ineffective or inefficient to specific individuals. 

These findings were the building blocks of what we know today as Pharmacogenomics: the application of genomic technologies to drugs in clinical development. “ Pharmacogenomics exists a the intersection of pharmacology and genomics”[2], taking into consideration the “drug-metabolism phenotypes” of patients to better design drugs, drug combinations, and dosages for individual patients. Pharmacogenomic investigations require an increased use of methods designed to study many genes or gene patterns, that is to look simultaneously at the structure and expression of whole sets of genes. Such methods include high throughput sequencing technologies such as MALDI mass spectrometry, SAGE,  microarrays, RNA-Seq, linkage and haplotype analysis.

### Part 3: Drug production through pharmacogenomics <a name="3"></a>


### Part 4: Applications of Bioinformatic tools: RNA-Seq<a name="4"></a>

*Identifying genetic factors excluding people from conventional medicine*

The presence of an abnormal gene can lead to a line of descendants exhibiting sensitivity towards drugs that are otherwise beneficial to those bearing the same illness. The naive way, is to commission a control and treatment group so that sensitivity can be evaluated. However, it is not only a costly procedure but also unethical in cases where the illness necessitates drastic treatments like chemotherapy, which harms both healthy and ill individuals alike.

Instead, researchers utilized subjects who provided consent as well as a completed a survey to provide biographical information latter used to present phenotypic classification for the data. The subjects also provided saliva samples that were used to gather data about single nucleotide polymorphisms(SNPs). Through this, genome-wide association studies(GWAS) was able to analyze each class’s SNPs. The latter proves useful for genome-wide association studies(GWAS) that’ll analyze each class’s SNPs. The data from these GWAS can be subjected through association tests with logical regression that’ll produce a p-value determining significance. Small p values indicated that these patients are inheritors of unique markers or conditions that affect their ability to get regular medicine(Qs Li). The presence of these unique markers inform medical providers to select a more precise treatment for patients. 

Another example of genome-wide studies revealing problematic SNPs is a study by the SEARCH study collaborative group, who discovered that the rs4363657 SNP brought muscular degeneration to those who consumed statins, a drug known to treat hypertension. The group extracted DNA from their subjects and stained them so they’d fluoresce, amplified them with gel electrophoresis, and elongated them with PCR. Using a BeadChip to collect SNPs, they initiated single-SNP analysis and outed the troublesome polymorphism (SEARCH). 

*Connecting RNA-Seq* 

As previously discussed in regards to the naive approach, testing for drug sensitivity experimentally can be both costly and invasive to patients. However, with the advancement of high throughput sequencing, it has become possible to assess phenotypic reactions to treatment at a lower cost while obtaining more information on a molecular level. This allows researchers to have a better understanding of how gene expression differs between subpopulations who have different sensitivity to a given drug. Thus, RNA-Seq equips researchers to evaluate the complexities of drug responses through transcriptome data of  populations. RNA-seq can better advance pharmacogenomics since it connects drug sensitivity to gene expression which is crucial to the development of  more effective therapies.





#### Method 1: Making a drug network
A group led by Ke-Jia Xu pioneered the creation of a drug network. This network and the corresponding formula predicts synergistic drugs, thus saves time otherwise wasted on testing useless combinations by brute force.

Combining drugs allows them to accomplish what one alone cannot, enabling the ability to defend multiple points of attack from highly invasive diseases such as cancer. These drugs tend to be more selective, with a limited scope , granting more precise effects and lessened side effects. Incorporating selective medicines will form a medicinal team capable of launching several accurate defenses at multiple areas. However, careless combination can lead drugs to counter each other’s effects, a quality known as antagonism.

One efficient method is the construction of drug networks, where drugs are represented as nodes and connected by edges with widths proportional to their ability to complement one another also known as therapeutic similarity. The following equation depicts how the drug network is constructed. 

![equation](https://i.imgur.com/prcTXxT.gif)
N is the number of drugs in the network, n1 and n2 are the partners of drugs 1 and 2, and m is the number of chemicals they have in common with each other.
- Drugs not connected by edges would create useless, if not harmful combinations
- The closer this value is to 0, the likelier the chance a useful combo has been found, which will form an edge between these drug nodes.

![drug_network](https://i.imgur.com/TSMWvAu.jpg)
Drug nodes that are particularly popular with other drugs are colored red, meaning they’ll be crucial to many effective drug combos which can alert manufacturers to prioritize the production of this  specific drug/ingredient.

Alternatively, since drug networks aren’t the first attempt to calculate effective combinations, it’s also possible to draw data from previous forays to simplify the process, like the Drug Combination Database. After expelling the combos lacking Anatomical Therapeutic Chemical (ATC), which saves computational time, they feed the ATC of various drugs into the following formula 

![TS_equation1](https://i.imgur.com/QCzFsXv.gif)
ATCk(d) denotes the ATC codes at the Kth level. This is then used to calculate Therapeutic similarity:

![TS_equation2](https://i.imgur.com/btjOcUw.gif)
d1 and d2 are the two drugs represented as nodes to be connected or not and 'n' ranges from 1 to 5, representing all possible ATC levels.	

The combinations theorized by drug networks are tested through rigorous testing in clinical trials to determine the validity of this combination, trials that many have trumped.
 
To name a few that Xu favors, Dermatologists confirmed the efficacy of their combo drug named Tri-Luma amongst Asian subjects burdened with Melasma, a pigmentary disorder involving increased melanin. The questionnaires distributed to those consuming the drug combo and the conventional treatment revealed those of the former had much higher satisfaction scores than those of the latter. Similar degrees of success were found in experiments surrounding people with various comorbidities that negate the curative properties of a lone drug, but find themselves outmatched when confronted with a fusion of them. For instance, diabetes may worsen the high blood pressure normally present in those with hypertension, but Amiloride and Hydrochlorothiazide mixture defeated them both. 

One drawback to the network is that, while they identify complementary combos, they lack info on the dosages or drug concentrations. Many conventional medicine advise patients to take an arbitrary amount, an amount catered to average folks. But it defeats precision medicine’s purposes to generalize dosage, so longer trials, lengthened due to the need to gather results arising from different dosages and their effects on the subjects. With the billions of existing drugs, an amount growing by the second, the optimized methods described here may still take a frustratingly long amount of time. Certain diseases may need to be prioritized, meaning the treatment for others must endure delays. 

#### Method 2: Freshly-Made Compounded Medicine (Falconer) ![crushing_drugs](https://i.imgur.com/Hia7EMP.jpg)

In some cases, patients lack the time needed for analysts to finish constructing their graphs and verifying their results via clinical trials therefore leading to different methodologies, varying in difficulty, to produce medicine on demand. 

For instance, the simplest method is simply crushing the solid form of a medicine and mixing it into water. The liquid counterpart proves to be more amenable to those afflicted with dysphagia, a condition that impedes swallowing. Researchers may ascertain this condition’s presence by scanning for substitutions of Valine to Methionine due to polymorphism of rs2565 of the BDNF gene, a gene heavily involved the esophageal motor functions. Said polymorphism was discovered via transcranial magnetic stimulation which correlated with the SNPs locating the substitutions. However, some medicinal ingredients are insoluble, and attempts to mix them may create solid deposits that threaten to choke the drinker. Inactive excipients, components that accompany but have no effect on the drug’s active ingredients’ efficacy, can be incorporated to increase solubility. 

There are downsides to this approach since the distribution of these remedies have less standards to adhere to than the preparation of drug themselves which call into question to their stability and safety. As well as being vulnerable to degradation, such as oxidation or hydrolysis, which impairs the body’s ability to absorb the drugs or facilitates the synthesis of unexpected and potentially dangerous byproducts. Water content, which is prevalent in medicinal solutions, can devolve into breeding grounds for various microorganisms. Special attention must be paid, like controlling the pH or temperature, to maintain sterility. Since they’re brewed on demand, the combinations must be known beforehand, but since predictive methods like the drug network exist, it renders this limitation moot. 

However these downsides don’t brand this method as irredeemably bad since most of its products, which range from ointments to suppositories, are advised and designed for consumption moments after production, denying time that may otherwise be spent to degrade or contaminate the medicine. 


### Part 5: Next steps in pharmacogenomics <a name="5"></a>


### Part 6: References <a name="6"></a>

[1]Kalow, W. Pharmacogenetics and pharmacogenomics: origin, status, and the hope for personalized medicine. Pharmacogenomics J 6, 162–165 (2006) doi:10.1038/sj.tpj.6500361

[2]Innocenti, Federico. Pharmacogenomics Methods and Protocols. Human, 2016

[3]Liu, X. et al. A systematic study on drug-response associated genes using baseline gene expressions of the Cancer Cell Line Encyclopedia. Sci. Rep. 6, 22811; doi: 10.1038/srep22811 (2016).

[4]Qs Li, C Tian., et al. “Analysis of 23andMe antidepressant efficacy survey data: implication of circadian rhythm and neuroplasticity in bupropion response.” Translational Psychiatry, 2016, doi:10.1038/tp.2016.171

[5]SEARCH Collaborative group. “SLCO1B1 Variants and Statin-Induced Myopathy — A Genomewide Study.” The New England Journal of Medicine, 2008, doi:10.1056/ NEJMoa0801936. [PubMed: 18650507]

[6]Xu et al.: The drug cocktail network. BMC Systems Biology 2012 6(Suppl 1):S5.

[7]James R Falconer, Kathryn J Steadman. “Extemporaneously compounded medicines”. Australian Prescriber, 2017. doi:10.18773/austprescr.2017.001

[8] C. Kupiec, Thomas.  Raj, Vishnu. Vu, Nicole. Basics of Pharmacogenomics for the Compounding Pharmacist.  International Journal of Pharmaceutical Compounding, Vol. 9 No. 4 July/August 2005 




