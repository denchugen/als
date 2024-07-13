# als

## A240707_DEG_SCATAC
![image](https://github.com/user-attachments/assets/c42f91b7-083d-4b5d-91fe-a8ef20cd08c7)
/Volumes/TOSHIBA/ALS/A240707_DEG_SCATAC/SH07_UNIQ_PLOT_SIGN_0.6.R
(base) chia-pipe@simonpipe:/mnt/hgfs/H24D9/SM2409/ALS/A240707_DEG_SCATAC_SVR$ 
BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed
1. SV:  hit mm10 all isoform by BAMs from SAR4003AM and SAR4004AM.
2. hit --> RPM (by Deduplicated uniquely mappable read pairs) -->
3. Calculate the p-value using the cumulative distribution function (CDF) of the binomial distribution

*expected_prob == 0.6*

    ```p_value = 1 - binom.cdf(successes - 1, trials, expected_prob)```
4. cat SH04


## A240709_ASIGN_DEG240707_to_singleCell

#### SH01 scATAC cluster from cellranger
![image](https://github.com/user-attachments/assets/d4c5922e-5ba9-40c6-a811-ed53963ca74c)
/Volumes/TOSHIBA/ALS/A240709_ASIGN_DEG240707_to_singleCell/SH01_PLOT_DD.R

#### SH02 gene list

cat SH02.gene_list_type

cat BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign3.gene.tsv|cut -f5|grep -v gene|awk '{print $0"\t3GAO"}' > GAO3.list
cat BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign4.gene.tsv|cut -f5|grep -v gene|awk '{print $0"\t4GAO"}' > GAO4.list
 cat GAO3.list GAO4.list > CMB.gene_type.list






---

## A240712_YQ_BOX
![63081720781379_ pic](https://github.com/user-attachments/assets/2658facb-24d3-430a-9612-5103a90e1ab7)
E:\data\peak\peak10\AMB4003-AMB4004\TOP25peak
/mnt/hgfs/YQ2409/20240528-ATAC-peak-correlation/AMB4003-AMB4004/AMB4003-AMB4004-top25

![image](https://github.com/user-attachments/assets/f177c387-8248-474a-a270-1f975462b86f)

/Volumes/TOSHIBA/ALS/A240712_YQ_BOX/SH02_PLOT_SCATTER.R






## /Volumes/TOSHIBA/ALS/A240708_CMB4017PR50_4018GFP_CHIPcDNA
![image](https://github.com/denchugen/als/assets/8020391/6946aeb5-166e-46cb-951f-d1b3287b16ba)
```
/Volumes/TOSHIBA/ALS/A240708_CMB4017PR50_4018GFP_CHIPcDNA/SH07_UNIQ_PLOT_SIGN_0.9.R
/Volumes/TOSHIBA/ALS/A240708_CMB4017PR50_4018GFP_CHIPcDNA/SH08_UNIQ_PLOT_SIGN.R

BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_CMB4017GFP_CMB4018PR50_R2.cov.RPM.Prob_0.6.BINOM.yesSign.uniqisoCMB4017GFPgene.tsv.
BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_CMB4017GFP_CMB4018PR50_R2.cov.RPM.Prob_0.6.BINOM.yesSign.uniqisoCMB4018PR50gene.tsv
BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_CMB4017GFP_CMB4018PR50_R2.cov.RPM.Prob_0.9.BINOM.yesSign.uniqisoCMB4017GFPgene.tsv.
BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_CMB4017GFP_CMB4018PR50_R2.cov.RPM.Prob_0.9.BINOM.yesSign.uniqisoCMB4018PR50gene.tsv
```

![image](https://github.com/denchugen/als/assets/8020391/6ea2edb3-a9e8-47d8-a5dd-e7e06fa4a859)

```
BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso
/Volumes/TOSHIBA/ALS/A240707_DEG_SCATAC/SH07_UNIQ_PLOT_SIGN.R
BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.gene.txt
/Volumes/TOSHIBA/ALS/A240707_DEG_SCATAC/BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign3.gene.tsv
/Volumes/TOSHIBA/ALS/A240707_DEG_SCATAC/BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign4.gene.tsv
```

1. select all isoform of mm10
2. hit all isofom by SAR4003AM and SAR4004AM
3. calculate RPM by divided uniqpe-mapped_reads
4. calculate binom.test of the two rpm
5. set probabiliy = 0.5 and 0.6
6. plot x=log10(p), y=log(rpm)
7. plot  probabiliy = 0.5 and 0.6 as comaration
![image](https://github.com/denchugen/als/assets/8020391/2e7bfd4b-a9f2-48a0-a43e-5e0ef9c1e650)

SAR4003AM.RPM.x100.bedgraph.mm10
SAR4004AM.RPM.x100.bedgraph.mm10

1. 取mm10最长的isoform
2. 有这两个lib的信号去hit，算出RPM
3. 求出“差异”
```
(base) chia-pipe@simonpipe:/mnt/hgfs/H24D9/SM2409/ALS/A240707_DEG_SCATAC_SVR$ ls|cat
BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed
SAR4003Amm10.Dedup.L0.D34.Sorted.bam
SAR4003Amm10.Dedup.L0.D34.Sorted.bam.bai
SAR4004Amm10.Dedup.L0.D34.Sorted.bam
SAR4004Amm10.Dedup.L0.D34.Sorted.bam.bai```

(chia-pipe) chia-pipe@simonpipe:/mnt/hgfs/H24D9/SM2409/ALS/A240707_DEG_SCATAC_SVR$ bedtools multicov -bams SAR4003Amm10.Dedup.L0.D34.Sorted.bam SAR4004Amm10.Dedup.L0.D34.Sorted.bam -bed BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed > BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov

(base) chia-pipe@simonpipe:/mnt/hgfs/H24D9/SM2409/ALS/A240707_DEG_SCATAC_SVR$ head BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov 
chr1	3073253	3074323	ENSMUST00000193812.1	4933401J01Rik	+	45	24
chr1	3102016	3102126	ENSMUST00000082908.1	Gm26206	+	12	12
chr1	3252757	3253237	ENSMUST00000192857.1	Gm18956	+	66	65
chr1	3365731	3368550	ENSMUST00000195335.1	Gm37180	-	407	393
chr1	3375556	3377789	ENSMUST00000192336.1	Gm37363	-	187	253


```
```
(base) chia-pipe@simonpipe:/mnt/hgfs/JK2410/20240513/SAR4003A/SAR4003Amm10$ cat RPMCoverage.x100.sh 
#!/bin/bash

paste <(awk '{OFS="\t"; print $1,$2,$3}' SAR4003Amm10.Dedup.L0.D34.bedgraph.mm10)  <(awk '{OFS="\t"; printf("%.2f\n", ($4/109181054)*100000000)}' SAR4003Amm10.Dedup.L0.D34.bedgraph.mm10) > SAR4003AM.RPM.x100.bedgraph

(base) chia-pipe@simonpipe:/mnt/hgfs/JK2410/20240513/SAR4003A/SAR4003Amm10$ cd ../../SAR4004A/SAR4004Amm10/
(base) chia-pipe@simonpipe:/mnt/hgfs/JK2410/20240513/SAR4004A/SAR4004Amm10$ cat RPMCoverage.x100.sh 
#!/bin/bash

paste <(awk '{OFS="\t"; print $1,$2,$3}' SAR4004Amm10.Dedup.L0.D34.bedgraph.mm10)  <(awk '{OFS="\t"; printf("%.2f\n", ($4/104463600)*100000000)}' SAR4004Amm10.Dedup.L0.D34.bedgraph.mm10) > SAR4004AM.RPM.x100.bedgraph

(base) chia-pipe@simonpipe:/mnt/hgfs/JK2410/20240513/SAR4004A/SAR4004Amm10$ 

```
---

## A240705_MS_GO

![SH55_point_MSGO R](https://github.com/user-attachments/assets/0d8f772f-8ab3-4130-9d49-6e54ccb2b15b)

/Volumes/TOSHIBA/ALS/A240705_MS_GO/SH55_point_MSGO.R
![image](https://github.com/user-attachments/assets/42a790e7-4f5c-44ab-9a2f-549a8e1370db)

/Volumes/TOSHIBA/ALS/A240705_MS_GO/SH52_PLOT_MSSCATTER.R

---


### A240704_RMBDEG_AMGPEAK

![image](https://github.com/denchugen/als/assets/8020391/fcd5df71-f340-4fc8-9f89-2ba253e98379)


- /Volumes/TOSHIBA/ALS/A240704_RMBDEG_AMGPEAK/RMB40021_GO/SH54.R

![image](https://github.com/denchugen/als/assets/8020391/5cd83d6f-f5ba-406f-9be6-5e0a423e5a32)


- /Volumes/TOSHIBA/ALS/A240704_RMBDEG_AMGPEAK/RMB40021_GO/SH55_point_GO.R

![image](https://github.com/denchugen/als/assets/8020391/c2b98f77-9fd1-472c-81d9-0191090b5b09)


- /Volumes/TOSHIBA/ALS/A240704_RMBDEG_AMGPEAK/RMB40021_GO/SH55B_point_GO.R

## A240704_RMBDEG_AMGPEAK..RMB40021_GO
![image](https://github.com/denchugen/als/assets/8020391/c9fe70a1-d2f7-48db-bed6-fede92811a72)

```
/Volumes/TOSHIBA/ALS/A240704_RMBDEG_AMGPEAK/RMB40021_GO/SH44_MANU_GO_PLOT.R
IN="RMB40021_GO.RMB4002over4001.plusGreen615.tsv.gene.GOana_BP.ZMZselect.tsv"

/Volumes/TOSHIBA/ALS/A240704_RMBDEG_AMGPEAK/RMB40021_GO/SH44_MANU_GO_PLOT.R.RMB40021_GO.RMB4002over4001.plusGreen615.tsv.gene.GOana_BP.ZMZselect.tsv.png
```
## A240704_RMBDEG_AMGPEAK
![image](https://github.com/denchugen/als/assets/8020391/4d457246-de74-4db9-8dbc-88c5670d5bb4)
![image](https://github.com/denchugen/als/assets/8020391/8cc14f9c-00bc-407b-9428-bd6a3f0af90f)

```
/Volumes/TOSHIBA/ALS/A240704_RMBDEG_AMGPEAK/DEG-RMB4001-RMB4002/lfc2/SH02_plot_volcano.R
```
### 0.数据源头YQ
  
  ```
  /Users/zhengmeizhen/Nutstore Files/科研-郑田/ALS-3D2024/DATA_ALS
  ```

### 1.MATERIAL_ALS
