# This is a summary of what you can find here as a back-up resource list for [He and Williams et al. 2020 Nature](https://www.nature.com/articles/s41586-020-2536-x) 

The MATLAB code used to perform clustering analyses and PCA can be found [here](He_2020_ENCODE3_RNA/Notebook_1_BulkRNA.md).

The Linux shell script and MATLAB code to plot correlations between GROseq, RNAseq and 3'UTR can be found [here](He_2020_ENCODE3_RNA/Notebook_2_GROseq_3primeUTR_analysis.md).

A detailed description of each cluster and cell type can be found [here](https://static-content.springer.com/esm/art%3A10.1038%2Fs41586-020-2536-x/MediaObjects/41586_2020_2536_MOESM1_ESM.docx)

Scripts to generate the network graphs are [here](https://github.com/hamrhein/mouse_embryo)

Explore the data interactively in the UCSC Cell Browser:

- [Bulk RNA-seq data browser](https://cells-test.gi.ucsc.edu/?ds=mouse-encode-rna&layout=3)
- Bulk RNA-seq genomic coverage browser session: [data](https://genome-test.gi.ucsc.edu/cgi-bin/hgTracks?hgS_doOtherUser=submit&hgS_otherUserName=Gerardo&hgS_otherUserSessionName=timecourseSignal_track) · [description](https://genome-test.gi.ucsc.edu/cgi-bin/hgTrackUi?db=mm10&g=developmentTimecourseSignalMm10#TRACK_HTML)
- [Limb cell atlas data browser](https://cells.ucsc.edu/?ds=mouse-limb)

<details>
<summary><strong>ENCODE data &amp; UCSC Genome Browser track hubs</strong></summary>

### ENCODE data

- [ENCODE publication: The changing mouse embryo transcriptome at whole tissue and single-cell resolution](https://www.encodeproject.org/publications/e0d01543-9965-4edb-933c-778a40575cd9/): publication object for He and Williams et al. 2020 (*Nature*). Companion resources include the developmental epigenomic matrix, computed network components, and IDEAS chromatin segmentations.
- [Bulk RNA-seq dataset (ENCSR574CRQ)](https://www.encodeproject.org/publication-data/ENCSR574CRQ/): RNA-seq of mouse whole tissue embryonic developmental time course (Barbara Wold lab, Caltech).
- [ENCSR574CRQ metadata and download links](https://www.encodeproject.org/documents/ab75e52f-64d9-4c39-aea0-15372479049d/@@download/attachment/ENCSR574CRQ_metadata.tsv): TSV with sample metadata and download URLs for all files attached to the dataset by default on ENCODE.

### UCSC Genome Browser track hubs

These track hubs were generated during the C1 mouse development paper work (original compilation by Diane Trout). Opening any link should launch UCSC with the hub pre-loaded.

### Annotation track hubs

- [GENCODE M4](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_combined/M4/hub.txt): GENCODE M4 exon annotations.
- [IDEAS regions](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_combined/ideas_regions/hub.txt): IDEAS regions (0.2 threshold).

### C1 track hubs

- [C1 aggregated by cluster](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_combined/C1_cluster_aggregates/c1_cluster_aggregates.hub.txt): C1 cells grouped by cluster and merged to one BAM per cluster; depths normalized by total reads per million.
- [920 cell clusters](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_timecourse/paper_by_cluster/paper_by_cluster.hub.txt): smaller C1 clusters as one cell per track.
- [920 cell Mesenchyme](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_timecourse/paper_by_mesenchyme/paper_by_cluster_mesenchyme.hub.txt): mesenchyme C1 cluster as one cell per track (very large hub).
- [920 cells perichondrium](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_timecourse/paper_by_perichondrium/paper_by_cluster_perichondrium.hub.txt): perichondrium C1 cluster as one cell per track.
- [920 cells cluster, largest clusters capped at 30 cells](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_timecourse/subsample_by_cluster/subsample_by_cluster.hub.txt): one cell per track; largest clusters capped at 30 cells.
- [35 cell subset](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/peng_clustering_35cells/C1_peng_clustering_35cells.hub.txt): subset of “peng clustering 35 cells” including green/red/dark red/yellow/orange clusters (Muscle 1/2/3, EMP, Macrophage).

### 10x track hubs

- [10x muscle cluster aggregate](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_combined/10x_tracks/hub.txt): 10x muscle clusters and proximal mesenchyme including all reads from the cell-barcode filtered 10x runs.
- [10x muscle cluster aggregate (UMIs removed)](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_mouse_limb_combined/10x_tracks/cb_ub_chr_start_hub.txt): collapses reads with the same (cell barcode, molecular barcode, chromosome, start). This is more permissive than Cell Ranger’s UMI counting rules (see note below).

### PacBio track hubs

- [Shredded Sequel long reads](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/pac-bio-umi-search/sequel-shred.hub.txt): PacBio Sequel reads shredded into 100 bp reads and mapped with the ENCODE M4 STAR/RSEM pipeline.
- [PacBio (UCI collection)](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http://crick.bio.uci.edu/ENCODE-PacBio/hub.txt&genome=mm10): collection of PacBio reads hosted by UCI (hub created by Dana).

### Additional annotation hubs

- [ENCODE Candidate Regulatory Elements (mm10)](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://screen.encodeproject.org/api/ucsc_trackhub/9ec89a89-49f8-4304-8f43-f53ac55ecfb0/hub_2.txt): ENCODE cCREs from SCREEN.
- [Hub (search: ChIP-seq Bing Ren, UCSD limb H3K27)](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=https://www.encodeproject.org/batch_hub/type=Experiment,,assembly=mm10,,organ_slims=limb,,lab.title=Bing+Ren,+UCSD,,assay_title=ChIP-seq,,searchTerm=H3K27/hub.txt): (empty) H3K27 tracks from ENCODE portal batch hub.
- [Hub (search: ChIP-seq Bing Ren, UCSD limb H3K4me3)](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=https://www.encodeproject.org/batch_hub/type=Experiment,,assembly=mm10,,organ_slims=limb,,lab.title=Bing+Ren,+UCSD,,assay_title=ChIP-seq,,searchTerm=H3K4me3/hub.txt): (empty) H3K4me3 tracks from ENCODE portal batch hub.
- [Hub (search: DNase-seq ENCODE3 limb DNase)](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=https://www.encodeproject.org/batch_hub/searchTerm=limb+DNase,,type=Experiment,,assay_title=DNase-seq,,award.rfa=ENCODE3,,assembly=mm10/hub.txt): limb DNase tracks from ENCODE portal batch hub.

### Gigio transfection hub

- [Gigio Transfection Track](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http://woldlab.caltech.edu/~diane/encode3-transfection/hub.txt&genome=mm10): includes some tracks hosted by Peng; previously included ENCODE H3K27 marks organized by Georgi but those links later broke after directory reorganization.

### Tracks deemed misleading

- [920 cells C1 clusters aggregated (misleading)](http://genome.ucsc.edu/cgi-bin/hgTracks?db=mm10&hubUrl=http://woldlab.caltech.edu/~diane/C1_peng_20180710_cluster_bigwigs/C1_peng_20180710_cluster.hub.txt): built by summing bedgraphs across all cells in a cluster, which skews normalized values by cluster size.

### Note on Cell Ranger UMI counting (for interpreting “UMIs removed” tracks)

Per 10x Genomics (“Which reads are considered for UMI counting by Cell Ranger?”), Cell Ranger UMI counting considers reads with valid UMI + valid 10x barcode, and additionally requires:

- MAPQ 255 (STAR uniquely mapped)
- maps to exactly one gene (GX tag)
- overlaps an exon by ≥50% consistent with annotated splice junctions and strand annotation

The “UMIs removed” aggregate hub above required valid UMI + cellular barcode but did **not** require MAPQ 255, did not check the GX tag, and did not check exon overlap criteria.

</details>

# Mouse tissue development bulk RNA-seq co-expression clusters

[1 - Keratin](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%201.txt)

[2 - Muscle](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%202.txt)

[3 - Contractile](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%203.txt) 

[4 - Bladder](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%204.txt) 

[5 - Thymus immune](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%205.txt) 

[6 - Hormone](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%206.txt) 

[7 - Transport and apical](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%207.txt) 

[8 - Inflammatory and exosome](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%208.txt)

[9 - Immunoglobin](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%209.txt)

[10 - Immune](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2010.txt)

[11 - Brush border](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2011.txt)

[12 - NA](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2012.txt)

[13 - Lung](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2013.txt)

[14 - Cornified envelope](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2014.txt)

[15 - Technical A](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2015.txt) 

[16 - ECM](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2016.txt) 

[17 - Technical B](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2017.txt)

[18 - Eye and melanin](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2018.txt)

[19 - Hox9-13](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2019.txt)

[20 - Wnt signaling](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2020.txt)

[21 - Cell cycle](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2021.txt) 

[22 - Technical C](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2022.txt)

[23 - Technical D](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2023.txt)

[24 - Lipid](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2024.txt)

[25 - Hox1-9](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2025.txt)

[26 - Neurohypophyseal](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2026.txt)

[27 - Mesonephros](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2027.txt)

[28 - Cilium](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2028.txt)

[29 - Thymus](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2029.txt)

[30 - Metal ion transport](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2030.txt)

[31 - Neuron fate](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2031.txt) 

[32 - Adenylate cyclase](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2032.txt) 

[33 - Cell projection](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2033.txt) 

[34 - Synapse](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2034.txt)

[Ubiquitous](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%20Ubiquitous.txt)

# Seven types of cross-contaminations in dissection:

muscle contamination - [2 - Muscle](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%202.txt)

thymus contamination - [5 - Thymus immune](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%205.txt)

incomplete removal of adrenal gland from kidney - [6 - Hormone](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%206.txt)

differences in gut tissues’ anatomical definition between labs - [11 - Brush border](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2011.txt)

skin contamination - [14 - Cornified envelope](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2014.txt)

failure to remove the eyes from craniofacial prominence - [18 - Eye and melanin](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2018.txt)

differences in neural tube dissection between labs - [19 - Hox9-13](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2019.txt) and [25 - Hox1-9](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2025.txt)


# Four lists of batch effect-specific genes:

[15 - Technical A](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2015.txt) 

[17 - Technical B](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2017.txt)

[22 - Technical C](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2022.txt)

[23 - Technical D](He_2020_ENCODE3_RNA/GeneLists/Bulk%20Cluster%2023.txt)


# Mouse forelimb cell types based on 10X scRNA-seq:

[0 - Mesenchymal cell 1](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%200%20-%20Mesenchymal%20cell%201.txt)

[1 - Perichondrial cell](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%201%20-%20Perichondrial%20cell.txt)

[2 - Mesenchymal cell 2](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%202%20-%20Mesenchymal%20cell%202.txt)

[3 - Chondrocyte](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%203%20-%20Chondrocyte.txt)

[4 - Muscle 2 (PAX7+ muscle progenitor)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%204%20-%20Muscle%202%20(PAX7%2B%20muscle%20progenitor).txt)

[5 - Epithelial cell 1](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%205%20-%20Epithelial%20cell%201.txt)

[6 - Fibroblast](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%206%20-%20Fibroblast.txt)

[7 - Muscle 1 (PAX3+ muscle progenitor)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%207%20-%20Muscle%201%20(PAX3%2B%20muscle%20progenitor).txt)

[8 - Macrophage](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%208%20-%20Macrophage.txt)

[9 - Endothelial cell](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%209%20-%20Endothelial%20cell.txt)

[10 - FOXP1+ perichondrial cell](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2010%20-%20FOXP1%2B%20perichondrial%20cell.txt)

[11 - Tenocyte](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2011%20-%20Tenocyte.txt)

[12 - Muscle 4 (muscle fibre)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2012%20-%20Muscle%204%20(muscle%20fibre).txt)

[13 - Early erythrocyte (Primitive erythrocyte)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2013%20-%20Early%20erythrocyte%20(Primitive%20erythrocyte).txt)

[14 - Neural crest (and Schwann cell)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2014%20-%20Neural%20crest%20(and%20Schwann%20cell).txt)

[15 - Stressed mesenchymal cell (high mitochondria)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2015%20-%20Stressed%20mesenchymal%20cell%20(high%20mitochondria).txt)

[16 - Osteoblast (or interzone cartilage cell)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2016%20-%20Osteoblast%20(or%20interzone%20cartilage%20cell).txt)

[17 - Muscle 3 (MYOG+ myocyte)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2017%20-%20Muscle%203%20(MYOG%2B%20myocyte).txt)

[18 - Epithelial 2](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2018%20-%20Epithelial%202.txt)

[19 - Smooth muscle cell](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2019%20-%20Smooth%20muscle%20cell.txt)

[20 - EMP (and mast cell)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2020%20-%20EMP%20(and%20mast%20cell).txt)

[21 - Megakaryocyte](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2021%20-%20Megakaryocyte.txt)

[22 - COL1A1+ muscle 4 (or interstitial muscle cell)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2022%20-%20COL1A1%2B%20muscle%204%20(or%20interstitial%20muscle%20cell).txt)

[23 - Late erythrocyte (definitive erythrocyte)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2023%20-%20Late%20erythrocyte%20(definitive%20erythrocyte).txt)

[24 - IHH+ chondrocyte (prehypertrophic chondrocyte)](He_2020_ENCODE3_RNA/GeneLists/Limb%20Cell%20Type%2024%20-%20IHH%2B%20chondrocyte%20(prehypertrophic%20chondrocyte).txt)
