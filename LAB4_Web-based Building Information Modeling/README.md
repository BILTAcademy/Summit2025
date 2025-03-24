# Summit2025 LAB4: Web-based Building Information Modeling
In LAB4, we'll dive into the world of Web-based Building Information Modeling.
Building Information Modeling is a common method in practice to model information related to buildings. It has a standardized information schema (Industry Foundation Classes, IFC) that helps exchanging information between stakeholders and software tools. However, the core exchange format, IFC STEP, has significant challenges in data interoperability, data integration across different domains, and reasoning and inferencing. 
Novel technologies aim to alleviate those challenges. In this LAB, we'll specifically explore two of such technologies, namely Semantic Web Technologies and Large Language Models. The three blocks each have a key learning objective, being:
1. Understand the basics of semantic web technologies to represent building information in graphs
2. Create and use ontologies and query information using SPARQL
3. Understand how Large Language Models could be used in combination with linked building data

This repositry is created by dr. ir. [Alex Donkers](https://research.tue.nl/nl/persons/alex-ja-donkers), Eindhoven University of Technology. 

### Prerequisites
In order to participate in LAB4, students are expected to:
- Have a basic understanding of BIM and the IFC schema;
- Have a basic understanding of coding languages, preferably Python;
- Understanding of databases and query langauges is preferred, but not necessary to join this lab.

### Preparation
In order to not lose too much time in the lab, participants are required to:
- Bring a laptop
- Have a coding environment (such as [Visual Studio Code](https://code.visualstudio.com/)) installed.
- Have [GraphDB Free](https://www.ontotext.com/products/graphdb/?utm_source=adwords&utm_medium=ppc&utm_term=graphdb%20free&utm_campaign=Search+Graphdb&hsa_cam=21938209598&hsa_mt=b&hsa_ver=3&hsa_src=g&hsa_ad=722528532177&hsa_net=adwords&hsa_tgt=kwd-806325731642&hsa_acc=9129462532&hsa_grp=173328703560&hsa_kw=graphdb%20free&gad_source=1&gclid=Cj0KCQjwhYS_BhD2ARIsAJTMMQYrKYlW3LJW0IfwP_Kufg4AglDrVz1r--V3KVZ47ls9aDSyApivGuAaAiqjEALw_wcB) installed.
- Have [Stanford Protégé](https://protege.stanford.edu/software.php#desktop-protege) installed.
- Have a stable version of Python installed. 

GraphDB requires you to ask access to get the free license, which may take some time. Please try and install these a.s.a.p..

## Resources

### Data
During this lab, participants are allowed to make use of the IFC and TTL files in the [Resources](https://github.com/AlexDonkers/Summit2025/tree/main/LAB4_Web-based%20Building%20Information%20Modeling/Resources) folder. These files are created by Selahattin Dulger and Alex Donkers as part of the Eureka ITEA4 FireBIM project.

### Tools
- [Comunica web client with the OpenFlat](https://query.comunica.dev/#datasources=https%3A%2F%2Fraw.githubusercontent.com%2FAlexDonkers%2Fofo%2Fmain%2FSWJ_Resources%2FOpenFlat%2FOpenFlat_Donkers.ttl&query=PREFIX%20bot%3A%20%3Chttps%3A%2F%2Fw3id.org%2Fbot%23%3E%0Aselect%20*%20where%20%7B%0A%20%20%20%20%3Fs%20%3Fp%20bot%3ABuilding%20.%0A%7D%20limit%20100)
- [Public SPARQL endpoint of the city of Florence](https://opendata.comune.fi.it/content/sparql)
- [DBpedia SPARQL endpoint](https://dbpedia.org/sparql)
- [LD-BIM](https://ld-bim.web.app/)
- [LBDviz](https://alexdonkers.github.io/LBDviz/dist/)
- [SPARQL-visualizer](https://madsholten.github.io/sparql-visualizer/)

### Python-based graph interactions
- [01_Check python version](https://colab.research.google.com/github/AlexDonkers/RUB-IIB-Workshops-2024/blob/main/01_CheckPythonInstallation.ipynb)
- [02_RDFlib](https://colab.research.google.com/github/AlexDonkers/RUB-IIB-Workshops-2024/blob/main/02_RDFlib.ipynb)
- [03_SPARQLWrapper](https://colab.research.google.com/github/AlexDonkers/RUB-IIB-Workshops-2024/blob/main/03_SPARQLWrapper.ipynb)
- [04_RDFlib + python variables](https://colab.research.google.com/github/AlexDonkers/RUB-IIB-Workshops-2024/blob/main/04_RDFlib-plus-python-variables.ipynb)

### LBDviz
- [LBDviz](https://alexdonkers.github.io/LBDviz/dist/)
- [Tutorial](https://github.com/AlexDonkers/Frontends-and-LBD/)
- [A Visual Support Tool for Decision-Making over Federated Building Information](https://link.springer.com/chapter/10.1007/978-3-031-37189-9_32)

## KLO 1 Understand the basics of semantic web technologies to represent building information in graphs
[Presentation](https://github.com/AlexDonkers/Summit2025/raw/refs/heads/main/LAB4_Web-based%20Building%20Information%20Modeling/Presentation.pptx)
Activity: Open the OpenFlat.ttl in GraphDB. Explore the Graph in the Visual Explorer.
Activity: Run a query in the SPARQL tab.
Activity: Draw a graph containing the information related to your exercise. 
Activity: Create a small TTL file with the graph. Take a look at the ExampleTriples.ttl file in the [Resources](https://github.com/AlexDonkers/Summit2025/tree/main/LAB4_Web-based%20Building%20Information%20Modeling/Resources) folder.

## KLO 2 Create and apply ontologies, introduction to the basics of querying via both SPARQL and large language models 
[Presentation](https://github.com/AlexDonkers/Summit2025/raw/refs/heads/main/LAB4_Web-based%20Building%20Information%20Modeling/Presentation.pptx)
Activity: Draw an ontology using the information related to your exercise.
Activity: Formalize the ontology in Protégé. 
Activity: Use the ontology to enrich your TTL. 
Activity: Load the TTL in GraphDB. 

## KLO 3 Understand how Large Language Models could be used in combination with linked building data
[Presentation](https://github.com/AlexDonkers/Summit2025/raw/refs/heads/main/LAB4_Web-based%20Building%20Information%20Modeling/Presentation.pptx)
Activity: Load the OpenFlat in [LD-BIM](https://ld-bim.web.app/). Also load all your TTL data. 
Activity: Copy one of the queries from GraphDB into LD-BIM. Do you get the same results?
Activity: Take a text in natural language, and prompt it to one of the LLMs. Ask to convert it to a TTL format. (zero-shot prompting)
Activity: Then add the TTL that you already created to the LLM, and ask to convert the text a TTL format following the similar logic as that manually created TTL. (one-shot prompting)
Activity: Then add the ontology that you created, and ask the LLM to map terms to those classes.

