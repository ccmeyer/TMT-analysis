# TMT-analysis
### The code included in this repository was used in the publication "Holistic engineering of cell-free systems through proteome-reprogramming synthetic circuits" by Luis E. Contreras-Llano and Conary Meyer et al. 2020.
### The following pipeline is used to normalize and analyze protein abundance values from Tandem Mass Tag (TMT) proteomics analysis. Prior to entry into the included pipeline, the raw mass spectrometry results should be analyzed with the [PAW_pipeline](https://github.com/pwilmart/PAW_pipeline).

#### Order of scripts in pipeline:
1. `convert_PAW_results.ipynb` - Maps the TMT-labels to the experimental condition of each sample. Filters the proteins included by their sequence coverage.
2. `TMT_normalization.ipynb` - Normalizes the intensities of each protein based on an internal reference. This code was modeled after Phil Wilmarth's [IRS Normalization](https://pwilmart.github.io/IRS_normalization/understanding_IRS.html).
3. `information_mapping.ipynb` - Maps the protein metadata included in a UNIPROT proteome to the protein identifiers. Identifies intentionally over-expressed proteins. Compares protein intensities across each sample.
4. `gene_ontology_assignment.ipynb` - Assigns each protein to a specific and general functional group based on their assigned gene ontological identifiers.
5. `PCA_analysis.ipynb` - Conduct and plot principal component analysis of all proteins and within each specific category.
6. `comparing_individual_protein_intensities` - Visualizes the differences in protein abundance at the individual, specific category, and general category.
