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


# Getting Help

If you have questions or need additional help, please contact the PRIDE Helpdesk at the EBI: pride-support at ebi.ac.uk (replace at with @).

Please send us your feedback, including error reports, improvement suggestions, new feature requests and any other things you might want to suggest to the PRIDE team.

# This library has been used in:

* Wang, R., Fabregat, A., Ríos, D., Ovelleiro, D., Foster, J. M., Côté, R. G., ... & Vizcaíno, J. A. (2012). PRIDE Inspector: a tool to visualize and validate MS proteomics data. Nature biotechnology, 30(2), 135-137. [PDF File](http://www.nature.com/nbt/journal/v30/n2/pdf/nbt.2112.pdf), [Pubmed Record](http://www.ncbi.nlm.nih.gov/pubmed/22318026)
* Vizcaíno, J. A., Côté, R. G., Csordas, A., Dianes, J. A., Fabregat, A., Foster, J. M., ... & Hermjakob, H. (2013). The PRoteomics IDEntifications (PRIDE) database and associated tools: status in 2013. Nucleic acids research, 41(D1), D1063-D1069. [PRIDE-Archive](http://www.ebi.ac.uk/pride/archive/)

How to use ms-data-core-api
===============

# Using ms-data-core-api 

### Reading a mzIdentML file:

This example shows how to read an mzIdentML file and retrieve the information from them:

```java
//Open an inputFile mzIdentml File using memory 
MzIdentMLControllerImpl mzIdentMlController = new MzIdentMLControllerImpl(inputFile, true);

//Print size of the Sample List
List<Sample> samples = mzIdentMlController.getSamples();
System.out.println(samples.size());

//Print the Id of the first sample
System.out.println(samples.get(0).getId());

//Print size of the Software List
System.out.println(software.size());

//Print the Name of the first Software
System.out.println(software.get(0).getName());

//Retrieve the Identification Metadata    
IdentificationMetaData experiment = mzIdentMlController.getIdentificationMetaData();
// test SearchDatabase
List<SearchDataBase> databases = experiment.getSearchDataBases();
        
// test SpectrumIdentificationProtocol
List<SpectrumIdentificationProtocol> spectrumIdentificationProtocol = experiment.getSpectrumIdentificationProtocols();

// Retrieve the Protein Identification Protocol
Protocol proteinDetectionProtocol = experiment.getProteinDetectionProtocol();

//Retrieve all Protein Identifications
List<Comparable> identifications = new ArrayList<Comparable>(mzIdentMlController.getProteinIds());
```

### Reading a PRIDE XML file:

This example shows how to read an PRIDE XML file and retrieve the information from them:

```java
//Open an inputFile mzIdentml File using memory 
PrideXmlControllerImpl prideXMLController = new PrideXmlControllerImpl(inputFile);

// You can use the example above and the same functions to retrieve the data using this controller for example:
//Print size of the Sample List
List<Sample> samples = prideXMLController.getSamples();
System.out.println(samples.size());
```


