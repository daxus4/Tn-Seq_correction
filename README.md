# Tn-Seq_correction

Transposon insertion sequencing (Tn-seq) is a robust and sensitive method to tackle the discovery of quantitative genetic interactions of transposons in microorganisms [1]. After the creation of a transposon insertion library, a sequencing is carried out to calculate change in frequency for all insertion mutants. With these changes, it is possible to obtain a score that indicates if an inserted mutation has a negative or a positive effect on bacterial growth. 

Due to the circular shape of bacteria genome, when sequencing is carried out the nucleotides near origin of replication (ORI) are sequenced with more frequency than the other nucleotides, if the bacterial DNA is going through a replication process, and this can lead to bias in scores. 

The goal of this project is to remove this bias. To achieve this, first we transformed the genomic coordinates in radians, which give us a better formalization of the problem. Then, to remove the bias, we fitted some models using linear regression and a series of preliminary operations to data, for example dividing the genome in windows. Through those approaches we successfully removed the bias. 

Finally, we demonstrated how to use this bias to identify the ORI genomic coordinate, taking advantage of the fact that nucleotides near ORI are sequenced more frequently than others. We fitted a local linear regression, and its maximum value is an estimate of the ORI. 

[1] van Opijnen T, Bodi KL, Camilli A. Tn-seq: high-throughput parallel sequencing for fitness and genetic interaction studies in microorganisms. Nat Methods. 2009 Oct;6(10):767-72. doi: 10.1038/nmeth.1377. Epub 2009 Sep 20. PMID: 19767758; PMCID: PMC2957483. 
