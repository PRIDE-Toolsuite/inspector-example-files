inspector-example-files
===============

# About inspector-example-files 

The primary purpose of inspector example files repository is a set of file examples that can be use by the users of PRIDE Inspector to 
for testing purpose. The current set of examples are divided by file types in four main categories: (i) mzIdentML, (ii) PRIDE-XML, (iii) mzTab and (iv) peak-files.
# License

inspector-example-files is a PRIDE API licensed under [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0.txt).

**Note**: the PRIDE Inspector tool is still evolving, we are committed to expand this library and add more useful examples.

# mzIdentML

mzIdentML is one of the standards developed by the Proteomics Informatics working group of the PSI  [(More)](http://www.psidev.info/mzidentml)

The examples are listed by Search Engines exporters (Mascot Folder, MS-GF+, Scaffold, Myrimatch, ProteinPilot, peptide-shacker). For all the outputs we provided the mzIdentML and 
the corresponding peak files used for protein identification in mgf, mzML or mzXML, etc.

# PRIDE-XML


The default PRIDE Submission is a ProteomeXchange Complete Submission where the Result files are PRIDE XML files. Submitters can create PRIDE xml files out of the MS/MS output data using the PRIDE Converter 2 tool. 
PRIDE Converter 2 is completely free and open source. PRIDE Converter 2 converts MS/MS data from most common data formats into valid PRIDE XML files.
In PRIDE XML different to mzIdentML and mzTab the spectra and the protein/peptide identification information is included in the same file. [(More)](http://www.ebi.ac.uk/pride/help/archive/submission/pridexml)


# mzTab

mzTab is meant to be a light-weight, tab-delimited file format for proteomics data. The target audience for this format are
primarily researchers outside of proteomics. It should be easy to parse and only contain the minimal information required to
evaluate the results of a proteomics experiment. One of the goals of this file format is that it, for example, should be possible for a biologist 
to open such a file in Excel and still be able to "see" the data. This format should also become a way to disseminate proteomics
results through protocols such as DAS. [(More)](https://code.google.com/p/mztab/) 


# peak-files

Peak files is a list of spectra files in different file formats such as peak lists (mgf, pkl, ms2, dta) and standard file formats (mzMl, mzData, mzXML). 



