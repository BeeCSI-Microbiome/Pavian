# Pavian

## In MobaXterm:
* Open an SFTP session
* Navigate to the directory where you ran the workflow, using the absolute path
   * eg, /isilon/lacombe-rdc/users/tranlan/cas_2020
   * Navigate to the file with a name similar to cas_kraken2
* Download the report.txt files

## At the [Pavian site](https://fbreitwieser.shinyapps.io/pavian/)
* On the “Data Selection” page:
   * Upload all the report.txt files
      * NB: the Pavian site times out after relatively short amount of time if left inactive, and when it does you have to re-upload the desired files
     * At the moment there have been some problems encountered when trying to run Pavian on R, but in theory it should be possible
### Retrieving specific taxa level tables:
* To access the resources needed to generated the NMDS and bar graphs, go to the “Comparison” page:
   * Change the rank preference from “Any Rank” to “Species”
   * Change “Reads” to “%” 
      * Make sure you unselect “Reads”, rather than just add percentages to the number of reads
 ![desired rank and read settings](https://github.com/BeeCSI-Microbiome/Pavian/blob/main/Rank.jpg)
   * Remove Apis mellifera and Varroa reads from the data by selecting their respective rows and then clicking the golf tee symbol at the top of the page
 ![how to filter unwanted species](https://github.com/BeeCSI-Microbiome/Pavian/blob/main/Filter.jpg)
    * Download a .tsv version of this data using the button at the bottom of the page
    
###  Retrieving 1 table with all taxa levels:
* Go to the "Comparison" page
* Make sure _Collapse taxa with no reads_ is **NOT** selected
* Choose Reads OR % (not both)
* Filter out taxa at your discretion
* Download a .tsv version of this data using the button at the bottom of the page

---

If you wish to see a Sankey visualization of all species present in each sample, go to the “Sample” page  
* NB: viruses, in particular the phiX bacteriophage, have been filtered out by the snakemake workflow. The BeeRoLaMa database does not contain virus sequences.


