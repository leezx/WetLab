
Design gRNA for CRISPR KO

1. CRISPick https://portals.broadinstitute.org/gppx/crispick/public
2. select Human GRCh38(Ensembl v.109) or Mouse GRCm38(Ensembl v.102)
3. select CRISPRko
4. select SpyoCas9(NGG)
5. select RS3seq-Chen2013+RS3target
6. choose gene (Tnfrsf12a)

Generate oligos:
1. GPT: 我现在需要做CRISPR KO实验，我已经通过CRISPick设计了一组sgRNA了，请帮我从里面选出最佳的三个sgRNA，我准备订oligos了。
2. 5'-CACCG-[sgRNA]-3'
3. 5'-AAAC-[rc sgRNA]-C-3'
4. IDT - https://www.idtdna.com/pages/products/custom-dna-rna/dna-oligos/custom-dna-oligos/sameday-oligos
5. upload template: template-paste-entry.xlsx, confirmed by GPT
6. 3 sgRNA sets (TOP+BOT) = $30

Validation:
- BLAT: https://genome.ucsc.edu/cgi-bin/hgBlat?hgsid=3302220047_o2hywqJ6nC3AYwnynWCN8GEJ7030&command=start
- should only have 1 unique genome binding

Plasmid: pCC01

Design PCR/Sanger primers (Detect Indel, Frameshift effect in cells) 原则：引物放在切割位点两侧较远位置（通常 ±200–300bp），扩增 500–600bp amplicon
1. use sgRNA to do BLAT: https://genome.ucsc.edu/cgi-bin/hgBlat
2. find your sgRNA, View - DNA sequence - -500 to +500 - get DNA
3. https://www.idtdna.com/PrimerQuest/Home/Index
  - Custom Design Parameters
  - Amplicon Size ( bp ) 600 - 700 bp
  - Included Region 200 - 800 bp
  - add to order
5. UCSC In-Silico PCR: https://genome.ucsc.edu/cgi-bin/hgPcr?hgsid=3302260901_mgABTR5vJpBB8AlpsolNAJxSipV4

ref:
1. Cancer实验系列之一 | 开篇 | Molecular cloning | 分子克隆 - https://www.cnblogs.com/leezx/p/17150023.html
2. 引物设计 | Primer design - https://www.cnblogs.com/leezx/p/17492590.html

