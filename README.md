/mnt/hgfs/JK2410/20240516
是联合PIPELINE ARC处理的


## A240714_6108_SAR40034004
![image](https://github.com/user-attachments/assets/695bdb16-8dda-4704-9eb3-f0b5fe5821d1)

![image](https://github.com/user-attachments/assets/8a7722dd-ed56-43ca-8357-3e50548cdb4b)


## /Volumes/TOSHIBA/ALS/A240714_6108_SAR40034004/SH01_ARC_Seurat.R
![image](https://github.com/user-attachments/assets/7af1ad46-1c77-49e6-bba5-dbeb9753691b)

![image](https://github.com/user-attachments/assets/8a127eae-c702-482d-94d4-d4f39f22e3c0)
![image](https://github.com/user-attachments/assets/daffa5f3-7084-462c-9e18-d7bb188172d1)

![image](https://github.com/user-attachments/assets/fb2a18da-f5c8-47a9-9107-aea3c1e06f71)
### UMI > 300 Number of nodes: 6970 Number of edges: 200959

![image](https://github.com/user-attachments/assets/d918c781-fad8-4b9c-84d9-76fb8cb6fe62)


![image](https://github.com/user-attachments/assets/49f0bf0c-5857-42b0-a2cc-30bd07c5f198)

![image](https://github.com/user-attachments/assets/97a4c06f-ef90-4f6b-b8e0-60ed5db2536b)
![image](https://github.com/user-attachments/assets/9722c889-e9b6-4c9c-840e-186490b4a54f)


### self_cluster
![image](https://github.com/user-attachments/assets/3ae51915-1d05-40ff-82b9-24bf80aaa15b)
![image](https://github.com/user-attachments/assets/0dab71a6-dcc1-4e53-a888-471623b7dfbf)
![image](https://github.com/user-attachments/assets/fa185691-7b26-4ea6-92fc-50091260ad3e)

### [1] "/Volumes/TOSHIBA/ALS/A240714_6108_SAR40034004/SH01_ARC_Seurat.R"
![image](https://github.com/user-attachments/assets/d24075aa-2f39-4341-9d33-ffce2ae4b1ad)

![image](https://github.com/user-attachments/assets/4b3adc14-8b99-4b04-950a-20fcd69a83a5)
![image](https://github.com/user-attachments/assets/4ec6902f-b071-4c80-9b0b-42279de75ffa)

## A240707_DEG_SCATAC
![image](https://github.com/user-attachments/assets/c42f91b7-083d-4b5d-91fe-a8ef20cd08c7)
/Volumes/TOSHIBA/ALS/A240707_DEG_SCATAC/SH07_UNIQ_PLOT_SIGN_0.6.R

#### /Volumes/TOSHIBA/ALS/A240714_6108_SAR40034004/SH20_read_DMN.R
![image](https://github.com/user-attachments/assets/f5fec5e0-1816-40b7-8fda-31fb09f46e6c)
![63371721128921_ pic](https://github.com/user-attachments/assets/b30b9ab2-13c2-43ec-a2b4-a9401744592a)

![63401721129524_ pic](https://github.com/user-attachments/assets/a68ce0d6-e711-4519-b54f-1014cb998078)
![63391721129194_ pic](https://github.com/user-attachments/assets/0c4bfca9-477f-42ed-bae3-5a91cbbf8b23)

![63411721129548_ pic](https://github.com/user-attachments/assets/8945958b-0d3f-4f86-a4da-43463ba0e3d5)



---
##### (base) chia-pipe@simonpipe:/mnt/hgfs/H24D9/SM2409/ALS/A240707_DEG_SCATAC_SVR$ 
##### BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed
1. （SERVER-END）hit mm10 all isoform by BAMs from SAR4003AM and SAR4004AM.
2. hit --> RPM (by Deduplicated uniquely mappable read pairs) -->
3. Calculate the p-value using the cumulative distribution function (CDF) of the binomial distribution

*expected_prob == 0.6*

    ```
    Python (v3.10.13)
    scipy (v1.12.0)
    
    from scipy.stats import binom
    p_value = 1 - binom.cdf(successes - 1, trials, expected_prob)
    ```
4. cat SH04
5.（MC END）选择 hit最大+最长的isoform-->uniqiso
6. plot

## A240709_ASIGN_DEG240707_to_singleCell
### SVR-END

(base) chia-pipe@simonpipe:/mnt/hgfs/H24D9/SM2409/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4003AMOUT$ 

(base) chia-pipe@simonpipe:/mnt/hgfs/H24D9/SM2409/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4004AMOUT$ 

1. SH00.data.sh
```
 1069  scp -r -P 1917 BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign3.gene.tsv chia-pipe@10.20.1.138:/mnt/hgfs/H24D9/SM2409/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4003AMOUT/
 1070  scp -r -P 1917 BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign4.gene.tsv chia-pipe@10.20.1.138:/mnt/hgfs/H24D9/SM2409/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4003AMOUT/
```

       438 BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign3.gene.tsv
      
       451 BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign4.gene.tsv
      
       889 total
   
2. combine XXX.sign3.gene.tsv and XXX. sign4.gene.tsv --(remove 乱七八糟chrom)> SM240707_peaks.bed.sC.clean
3. --(merge ovarlapeed peaks region)--> SM240707_peaks.all.sC.clean.lineID.merged.ID (864）
4. run "cellranger-atac reanalyze" 得到基于自定义peak的scATAC matrix

        -- /mnt/hgfs/H24D9/SM2409/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4004AMOUT/SH02.run_cellranger_atac.sh
        
        -- cellranger-atac-2.1.0
### MC-END
#### SH01 scATAC cluster from cellranger
![image](https://github.com/user-attachments/assets/d4c5922e-5ba9-40c6-a811-ed53963ca74c)
/Volumes/TOSHIBA/ALS/A240709_ASIGN_DEG240707_to_singleCell/SH01_PLOT_DD.R

#### SH02 ATAC变化大的基因list from A240707_DEG_SCATAC

cat SH02.gene_list_type

cat BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign3.gene.tsv|cut -f5|grep -v gene|awk '{print $0"\t3GAO"}' > GAO3.list
cat BASIC_UCSC_mm10_knownGene_GENECODE_VM23.bed.hitby_SAR4003AM_SAR4004AM.cov.RPM.Prob_0.6.BINOM.yesSign.uniqiso.sign4.gene.tsv|cut -f5|grep -v gene|awk '{print $0"\t4GAO"}' > GAO4.list
 cat GAO3.list GAO4.list > CMB.gene_type.list
 
#### SH10_cell_count.R
![image](https://github.com/user-attachments/assets/6fda3622-72e2-4f42-aa40-b9eb9d9f2a27)

#### SSH11_seurat.R
            seurat_obj_filtered_SO03A_matrix.csv
```
df_seurat_obj_matrix[1:5,1:10]
                       AAACAGCCAACTAGAA-1 AAACAGCCACTAAGAA-1 AAACATGCAAGCCAGA-1 AAACATGCAATTTAGC-1 AAACATGCACAAAGAC-1 AAACATGCACCTCACC-1 AAACATGCACGAATCC-1 AAACATGCATTGTCAG-1 AAACCAACAATATAGG-1 AAACCAACATGTCAGC-1
chr1:5644645-5644746                    0                  0                  0                  0                  0                  0                  0                  0                  0                  0
chr1:9191067-9192117                    0                  0                  0                  0                  0                  0                  0                  0                  0                  0
chr1:9802197-9802554                    0                  0                  0                  0                  0                  0                  0                  0                  0                  0
chr1:14182578-14182678                  0                  0                  0                  0                  0                  0                  0                  0                  0                  0
chr1:15757832-15757964                  0                  0                  0                  0                  0                  0                  0                  0                  0                  0
```
#### SH12_pheatmap.R
![image](https://github.com/user-attachments/assets/60723caf-8518-49de-9748-774dad83f6ef)
/Volumes/TOSHIBA/ALS/A240709_ASIGN_DEG240707_to_singleCell/SH12_pheatmap.R

####  SAR4003AM
![image](https://github.com/user-attachments/assets/3bd1ef23-2f96-48d1-8c79-683eacbb4470)


/Volumes/TOSHIBA/ALS/A240709_ASIGN_DEG240707_to_singleCell/SH20_plot_cellrange_cluster.R
#### SAR4004AM
![image](https://github.com/user-attachments/assets/a562f151-a85c-429b-8728-430b5f38d993)


/Volumes/TOSHIBA/ALS/A240709_ASIGN_DEG240707_to_singleCell/SH21_4004plot_cellrange_cluster.R

#### delete Cluster-1 (low fragment cell)
![image](https://github.com/user-attachments/assets/5904787c-0461-4c82-b19b-b350180c3335)

[1] "/Volumes/TOSHIBA/ALS/A240709_ASIGN_DEG240707_to_singleCell/SH20B_4003_filterout_cluster1.R"

![image](https://github.com/user-attachments/assets/f5fa9077-3430-4e96-a6e4-14cf0cbecf7e)
[1] "/Volumes/TOSHIBA/ALS/A240709_ASIGN_DEG240707_to_singleCell/SH21B_4004_filterout_cluster1.R"

#### send back to SVR cellrange analysis again
/mnt/hgfs/H24D9/SM2409/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4003AMNOCLU/
/mnt/hgfs/H24D9/SM2409/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4004AMNOCLU

```
$ cat SH02.run_cellranger_atac.sh 
OUT="SAR4003AMNOCLU1_OUTS"
rm -rf $OUT  __${OUT}.mro
nohup ./cellranger-atac reanalyze
--id $OUT
--peaks PEAK
--fragments atac_fragments.tsv.gz
--reference REF.mm10
--barcodes BC
--nopreflight
```
![image](https://github.com/user-attachments/assets/d925abe5-7cfc-4cd7-b6aa-543ab609af4c)

#### SAR4003AMNOCLU1_OUTS
![image](https://github.com/user-attachments/assets/657e05fe-ac57-483e-ad51-e2c4cadc7138)

 scp -r -P 1912 simon@10.20.1.138:/mnt/hgfs/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4003AMNOCLU1/SAR4003AMNOCLU1_OUTS/outs .
 /Volumes/TOSHIBA/ALS/A240709_ASIGN_DEG240707_to_singleCell/SAR4003AMNOCLU1_OUTS/outs




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
