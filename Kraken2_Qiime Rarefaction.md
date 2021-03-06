Qiime Taxonomic Analysis (after Kraken2)

# Create Rarefaction Curves (All Kingdoms)

##--------------------------------
## Step 1: Summarize overall frequency feature table
## -------------------------------  

### Summarize feature table
qiime feature-table summarize \
  --i-table table.qza \
  --o-visualization overall_summary
  
### Export summary 
qiime tools export \
  --input-path overall_summary.qzv \
  --output-path overall_summary
  
## Determine --p-max-depth: look at "frequency per sample" and choose value around median or max frequency. Increase if needed (max freq per sample)

##--------------------------------
## Step 2: Create Rarefaction Plot
## -------------------------------  

qiime diversity alpha-rarefaction \
  --i-table table.qza \
  --p-max-depth 6400000 \
  --m-metadata-file sample-metadata.txt \
  --o-visualization overall_alpha-rarefaction.qzv
  
##--------------------------------
## Step 3: Visualize rarefaction plot in qiime2 viewer
## -------------------------------   

### View by shannon and observed features and by metadata

# Create Rarefaction Curves (Bacteria Only)

##--------------------------------
## Step 1: Summarize bacteria only table
## -------------------------------  

### Summarize feature table
qiime feature-table summarize \
  --i-table bacteria_only.qza \
  --o-visualization bacteria_only_summary
  
### Export summary 
qiime tools export \
  --input-path bacteria_only_summary.qzv \
  --output-path bacteria_only_summary
  
### Determine --p-max-depth: look at "frequency per sample" and choose value around median or max frequency. Increase if needed (max freq per sample)

##--------------------------------
## Step 2: Create Rarefaction Plot
## -------------------------------  

qiime diversity alpha-rarefaction \
  --i-table bacteria_only.qza \
  --p-max-depth 1000000 \
  --p-steps 30 \
  --o-visualization bacteria_alpha-rarefaction.qzv
  
##--------------------------------
## Step 3: Visualize rarefaction plot in qiime2 viewer
## -------------------------------   

### View by shannon and observed features and by metadata

# Create Rarefaction Curves (Eukaryota Only)

##--------------------------------
## Step 1: Summarize eukaryota frequency feature table
## -------------------------------  

### Summarize feature table
qiime feature-table summarize \
  --i-table eukaryota_only.qza \
  --o-visualization eukaryota_only_summary
  
### Export summary 
qiime tools export \
  --input-path eukaryota_only_summary.qzv \
  --output-path eukaryota_only_summary
  
### Determine --p-max-depth: look at "frequency per sample" and choose value around median or max frequency. Increase if needed (max freq per sample)

##--------------------------------
## Step 2: Create Rarefaction Plot
## -------------------------------  

qiime diversity alpha-rarefaction \
  --i-table eukaryota_only.qza \
  --p-max-depth 7000 \
  --p-steps 20 \
  --o-visualization eukaryota_alpha-rarefaction.qzv
  
##--------------------------------
## Step 3: Visualize rarefaction plot in qiime2 viewer
## -------------------------------   

### View by shannon and observed features and by metadata

# Create Rarefaction Curves (Archaea Only)

##--------------------------------
## Step 1: Summarize arachaea frequency feature table
## -------------------------------  

### Summarize feature table
qiime feature-table summarize \
  --i-table archaea_only.qza \
  --o-visualization archaea_only_summary
  
### Export summary 
qiime tools export \
  --input-path archaea_only_summary.qzv \
  --output-path archaea_only_summary
  
### Determine --p-max-depth: look at "frequency per sample" and choose value around median or max frequency. Increase if needed (max freq per sample)

##--------------------------------
## Step 2: Create Rarefaction Plot
## -------------------------------  

qiime diversity alpha-rarefaction \
  --i-table archaea_only.qza \
  --p-max-depth 2000 \
  --p-steps 20 \
  --o-visualization archaea_alpha-rarefaction.qzv
  
##--------------------------------
## Step 3: Visualize rarefaction plot in qiime2 viewer
## -------------------------------   

### View by shannon and observed features and by metadata

# Create Rarefaction Curves (Viruses Only)

##--------------------------------
## Step 1: Summarize viruses frequency feature table
## -------------------------------  

### Summarize feature table
qiime feature-table summarize \
  --i-table viruses_only.qza \
  --o-visualization viruses_only_summary
  
### Export summary 
qiime tools export \
  --input-path viruses_only_summary.qzv \
  --output-path viruses_only_summary
  
### Determine --p-max-depth look at "frequency per sample" and choose value around median or max frequency. Increase if needed (max freq per sample)

##--------------------------------
## Step 2: Create Rarefaction Plot
## -------------------------------  

qiime diversity alpha-rarefaction \
  --i-table viruses_only.qza \
  --p-max-depth 5000 \
  --p-steps 20 \
  --o-visualization viruses_alpha-rarefaction.qzv
  
##--------------------------------
## Step 3: Visualize rarefaction plot in qiime2 viewer
## -------------------------------   

### View by shannon and observed features and by metadata
