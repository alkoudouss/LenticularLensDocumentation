<!--# <span style="color:purple"> <div align="center"> THE LENTICULAR LENS </div> </span>-->

<h1 style="font-size:4vw; color:purple"> <div align="center">THE LENTICULAR LENS</h1>

###### <div align="center"> A platform for addressing various aspects of the <span style="color:blue"> disambiguation of Entities </span>. <br> These aspects include the <span style="color:blue">creation</span>, <span style="color:blue"> manipulation</span>, <span style="color:blue"> validation</span>, <span style="color:blue"> provenance</span> and <span style="color:blue"> visualisation </span> of links. <br> Developped in the context of **RISIS** & the **Golden Agents Projec**t</div>

![LL](Images/LL.jpg)


<!--https://stackoverflow.com/questions/11948245/markdown-to-create-pages-and-table-of-contents/33433098#introduction-->
<!--------------------------------------------------------->
# </span> <div id='CONTENTS'/>
# <BR> <span style="color:purple"> TABLE OF CONTENTS (TOC) </span>
<!--------------------------------------------------------->


<!--<ol>
	<li> **[1. Introduction](#Introduction)** </li>
	<li> Second item< /li>
	<li>Third item
		<ul>
			<li>Indented item</li>
			<li>Indented item</li>
		</ul>
	</li>
	<li>Fourth item</li>
</ol>-->


**[1. Introduction](#Introduction)**<br>
**[2. Terminologies](#Terminologies)**<br>
**[3. The Lenticular Lens Menu](#The-Lenticular-Lens-Menu)**<br>
**[4. Link Construction](#Link-Construction)**

  * [4.1 Defining the Research’s Scope](#Defining-the-Researchs-Scope)
  * [4.2 Data Selection and Restrictions](#Data-Selection-and-Restrictions)
      * [4.2.1 Data Selections](#Data-Selections)
      * [4.2.2 Data Exploration](#Data-Exploration)
      * [4.2.3 Entity Restrictions](#Entity-Restrictions)
      * [4.2.3.1 Entity restriction options](#Entity-restriction-options) 
      
  * [4.3 Entity Resolution/Matching](#Entity-Resolution/Matching)
      * [4.3.1 Resolution Methods](#Resolution-Methods)
      * [4.3.2 Complex Methods](#Complex-Methods)
          * [4.3.2.1 T-norms ](#T-norms)
          * [4.3.2.1 T-conorms ](#T-conorms)	
      * [4.3.3 Matching in Practice](#Matching-in-Practice)
          * [4.3.3.1 Case Study: ](#Case-Study-1)
          * [4.3.3.2 Case Study: ](#Case-Study-2)
          * [4.3.3.3 Case Study: ](#Case-Study-3)
          * [4.3.3.4 Case Study: ](#Case-Study-4)

**[5. Link Manipulation](#Link-Manipulation)**

  * [5.1 Union](#Union)
  * [5.2 Intersection](#Intersection)
  * [5.3 Difference](#Difference)
  * [5.4 Composition](#Composition)
  * [5.5 In Set](#InSet)

**[6. Link Validation](#Link-Validation)**<br>
**[7. Link Export](#Link-Export)**

  * [7.1 Export Structure](#Export-Structure)
  * [7.2 Export Restrictions](#Export-Restrictions)
  * [7.3 Export Formats](#Export-Formats)
  * [7.4 Default Export Table](#Default-Export-Table)

**[8. Data Integration](#Data-Integration)**<br>
  
  * [8.1 Integration Model](#Integration-Model)
  * [8.2 Data Extraction](#Data-Extraction)

**[9. Installation](#Installation)**

**[10. API](#API)**





# </span> <div id=''/>

<!--------------------------------------------------------->
# </span> <div id='Introduction'/>
# <BR> <span style="color:purple">  1. INTRODUCTION (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!--------------------------------------------------------->

Time and again, researchers are presented with problems for which they postulate and test hypotheses in order to provide us with robust explanations for research questions successfully investigated. Often enough, solid explanations for complex problems require exploring a multitude of datasources. This is the case, for example, in domains such as e-science (multiple scientific datasets), e-commerce (multiple product vendors), tourism (multiple data providers), e-social science, digital humanities, etc. 
 
<span style="color: purple"> **DATA INTEGRATION.** </span> The use of various datasources come at the expense of heterogeneity which obfuscates the path to data integration and thereby hinders accurately addressing complex problems.
Dealing with multiple datasources or data providers highlights the freedom at which providers document facets of the same entity. Indeed, this feature of oriented freedom for entity descriptions can explain, to a certain extent, the inherent difficulty to integrate heterogeneous datasources.
<!--The inherent difficulty to integrate heterogeneous datasources can be explained, to a certain extent, by the lack of uniform entity description or vocabulary when the feature of oriented freedom for entity descriptions is exploited. 
-->
In the Semantic Web, this problem is partially circumvented as any pair of resources can be linked regardless to the uniformity of data representation or vocabulary used, i.e. uniformizing data/schema <!--uniform view --> is not a prerequisite for data integration provided that links between co-referent entities across heterogeneous datasets exist.


<span style="color: purple"> **RESULT QUALITY.** </span> The quality of supporting evidence for accepting or rejecting the hypothesis under investigation for a complex problem greatly depends on the correctness of the links integrating the underlying datasources. 
This begs for questions regarding the aboutness and correctness of the links, such as: <br>

* How to create correct links? More specifically, are there reliable tools for linking co-referent descriptions of entity scattered across various heterogeneous datasets? Can different tolls be combined?
* How to judge the applicability of links? Can their quality be estimated? Can they be improved, manipulated, visualised for validation purposes, reproduced? More specifically, is there a platform that supports all of the aforementioned concerns?

<!--
<span style="color:blue"> **CONNECTING DATASOURCES.** </span> 
Links connecting datasources are created under a context that provides evidence for its quality, on the basis of which they will be accepted or rejected as results supporting the investigation of a complex problem ...

The correctness of the links that integrate heterogenous datasets greatly depends on the quality of supporting evidence for accepting or rejecting the results of the investigation of a complex problem 
-->

<span style="color: purple"> **LINK CONSTRUCTION.** </span> Through the years, a number of entity matching tools have been developed and tested. 
However, some of theses tools have been developed for specific datasets, while others have limited applicability as they have mainly been tested in domain specific areas using synthetic or simplistic data, generally from at most two datasets. For example, as research in social sciences is increasingly based on multiple heterogeneous datasources, it becomes problematic to be limited to the integration of two datasets. 
Furthermore, in practice, the heterogeneity, messiness, incompleteness of data raise the bar higher in terms of entity matching complexity. <br>
In other words, most matching algorithms have been successfully applied in limited and controlled environments. This motivates the need for having the means to (re)use and combine generic matching approaches in order to solve specific problems.


<!--This is the case for example in domains such as e-science (multiple scientific datasets), e-commerce (multiple product vendors), tourism (multiple data providers), e-social science, digital humanities, etc. -->

<span style="color: purple"> **ENTITY DISAMBIGUATION PROPOSAL.** </span> In this document, we present a tool that supports disambiguation over multiple datasets: the **Lenticular Lens**. As a domain agnostic approach, the **Lenticular Lens** tool reuses existing matching approaches to allow for the user to reach their goals in ways that alleviates some of the main aforementioned issues:

<!--As opposed to black-box approaches, the Lenticular Lens tool allows machine and user to interact in ways that enable alleviating some of the main issues:
-->
* User-dependent and context-specific link discovery.
* User-based explicit concept mapping.
* Integration of more than two datasets.
* Combining entity matching algorithms and results.
* Structure-based evaluation of identity link networks.
* Enabling visualisation to support link/cluster validation.
* Metadata for documenting the link aboutness and enabling reproducibility.


<!--It is a user guided tool for links discovery, links manipulation (combination and validation) and for modelling RDF data integration while documenting links’ provenance.-->
<!--J. Euzenat and P. Shvaiko.Ontology matching. Springer-Verlag, Heidelberg (DE),2nd edition, 2013.-->

The context dependent link discovery idea developed and implemented in the **Lenticular Lens** ==[Refs]== is an extension of the Linkset and Lens concepts introduced by the Open PHACTS project  ==[Ref]== in the quests for building an infrastructure for integrating pharmacological data. Our extension and broadening of these concepts enabled us to design and build a flexible tool for undertaking entity disambiguation in a broader perspective.




<!---------------------------------------------------------->
# <br> <div id='Terminologies'/>
# <span style="color:purple">  2. TERMINOLOGIES </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!---------------------------------------------------------->


Before diving into how to use the **Lenticular Lens**, we define a number of terms we believe to be important for a better comprehension of what is offered by the tool. For some of the concepts defined here, we opt for a broader scope which fits best problems encounter in every day life
<!-- definition in [VoID](https://www.w3.org/TR/void/)-->.


<span style="color: purple">  **RESOURCE.** </span> "Anything can be a resource, including physical things, documents, abstract concepts, numbers and strings." [RDF 1.1](https://www.w3.org/TR/rdf11-concepts/#data-model)

<span style="color: purple">  **IRI - URI - URL - URN .** </span> These constitute ways in which things (resources) in the real world can be referred to in the digital world. "The resource denoted by an IRI is called its **referent**, and the resource denoted by a literal is called its literal value." [RDF 1.1](https://www.w3.org/TR/rdf11-concepts/#data-model). In the IRI example provided below, we illustrate six IRIs referents of resources of various types (hero, villain and vocabulary). 


```
Example: IRIs
-------------
 A resource's REFERENT is an IRI.
 A resource's LITERAL VALUE is a LITERAL.

	http://example.org/villain#Green-Goblin
	http://example.org/villain#Thanos
	http://example.org/hero#Spiderman
	http://example.org/person#Peter-Parker
	http://www.perceive.net/schemas/relationship/enemyOf
	http://xmlns.com/foaf/0.1/name


```

[Fusion](https://fusion.cs.uni-jena.de/fusion/blog/2016/11/18/iri-uri-url-urn-and-their-differences/) provides nice wording of all these terms as provided below. In short, URL, URN and URI are all specific types of an IRI. 

* **URI.** "A Uniform Resource Identifier is a compact sequence of characters that identifies an abstract or physical resource. The set of characters is limited to US-ASCII excluding some reserved characters. Characters outside the set of allowed characters can be represented using Percent-Encoding. A URI can be used as a locator, a name, or both. If a URI is a locator, it describes a resource’s primary access mechanism. If a URI is a name, it identifies a resource by giving it a unique name. The exact specifications of syntax and semantics of a URI depend on the used Scheme that is defined by the characters before the first colon. [RFC3986]"

* **URN.** "A Uniform Resource Name is a URI in the scheme urn intended to serve as persistent, location-independent, resource identifier. Historically, the term also referred to any URI. [RFC3986] A URN consists of a Namespace Identifier (NID) and a Namespace Specific String (NSS): urn:<NID>:<NSS> The syntax and semantics of the NSS is specific specific for each NID. Beside the registered NIDs, there exist several more NIDs, that did not go through the official registration process. [RFC2141]"

* **URL** "A Uniform Resource Locator is a URI that, in addition to identifying a resource, provides a means of locating the resource by describing its primary access mechanism [RFC3986]. As there is no exact definition of URL by means of a set of Schemes, URL is a useful but informal concept, usually referring to a subset of URIs that do not contain URNs [RFC3305]."

* **IRI** "An Internationalized Resource Identifier is defined similarly to a URI, but the character set is extended to the Universal Coded Character Set. Therefore, it can contain any Latin and non Latin characters except the reserved characters. Instead of extending the definition of URI, the term IRI was introduced to allow for a clear distinction and avoid incompatibilities. IRIs are meant to replace URIs in identifying resources in situations where the Universal Coded Character Set is supported. By definition, every URI is an IRI. Furthermore, there is a defined surjective mapping of IRIs to URIs: Every IRI can be mapped to exactly one URI, but different IRIs might map to the same URI. Therefore, the conversion back from a URI to an IRI may not produce the original IRI. [RFC3987]"



<span style="color: purple">  **RDF.** </span> As described by the [W3C](https://www.w3.org/RDF/), RDF is a **graph-based data model** for interchanging data on the Web and it stands for Resource Description Framework. In other words, [Lexico](https://www.Lexico.com/en/definition/rdf), the Oxford supported dictionary, emphasises on the semantic aspect by defining it as a model for encoding semantic relationships between items of data so that these relationships can be interpreted computationally. Expressing a relationship between a pair of RDF resources is done as a sequence 〈subject relation object .〉 of three terms. The sequence of terms is called a triple where each of its terms is separated by whitespace and the sequence is terminated by '.'. The example below illustrates two simple triple syntax. The triples, not only do they provid Spiderman's mane and assert that Spiderman and Peter Parker are the same, but they also provid identification for `Spiderman`, `Peter Parker` and the vocabulary terms `name` and `sameAs`. <br>
In RDF, any triple is an **RDF STATEMENT**. There exist various syntaxes for representing triple statements. For further reading, see
 [N-Triples](https://www.w3.org/TR/n-triples/), [Notation3](https://www.w3.org/TeamSubmission/n3/), [N-Quads](https://www.w3.org/TR/n-quads/), [Turtle](https://www.w3.org/TR/turtle/),  [RDF XML](https://www.w3.org/TR/rdf-syntax-grammar/#:~:text=Definition%3A,as%20defined%20in%20this%20document.), [RDFa](https://www.w3.org/MarkUp/2004/rdf-a),[JSON-LD](https://www.w3.org/TR/json-ld11/)... <br>

```
-----------------------------------------
-- Example: TRIPLES IN N-TRIPLE SYNTAX --
-----------------------------------------
<http://example.org/hero#Spiderman>  <http://xmlns.com/foaf/0.1/name>        "Peter-Parker" .
<http://example.org/hero#Spiderman>  <http://www.w3.org/2002/07/owl#sameAs>  <http://example.org/person#Peter-Parker>


```

<!--<span style="color: purple">  **URI.** </span> The term stands for Uniform Resource Identifier. As described, literally, it is a string of characters that represents a unique identification of a resource described using the Resource Description Framework model.-->



```
---------------------------------------
-- Example: TRIPLES IN TURTLE SYNTAX --
---------------------------------------
@prefix  ex: <http://example.org/#> .
@prefix rel: <http://www.perceive.net/schemas/relationship/> .

ex:green-goblin>  rel:enemyOf  ex:Spiderman .
ex:spiderman      foaf:name     ex:Peter-Parker.
```

<span style="color: purple">  **RDF LINK.** </span> It is also known as a **correspondent triple** <span style="color:blue">[*Euzenat*]</span> or simply **link** in RDF==??== and <span style="color:blue">[*VoID*]</span>. Links are triples in the form of 〈subject relation object〉 and are meant to exist only between two datasets. However, beside the incentive for providers to link their data to existing datasets, we do not see a good reason for a link not to exist within the same dataset. Thereby, in this document, an RDF link is a  relation between two resources (*digital representations of entities presented as URIs*) regardless of the datasource they stem from. This means a that a link can involve a minimum of one dataset and a maximum of two.


<span style="color: purple">  **IDENTITY LINK.** </span> </span> An **equality relation** between two resources (*digital representations of the same real world entity presented as URIs*) regardless of the datasource they stem from. In this document we often use the term **link** to denote **identity link** unless otherwise stated. Mainly described using the predicate `owl:sameAs`, such encoded semantic relationship entails full equality between two resources. This Semantic interpretation applies independently of context even though in real life problems, the equality between resources depends not only on their intrinsic properties but also on the purpose or task for which they are used. In this regard, we present the in the `Export` menu section the **Lenticular Lens** approach on the use and documentation of identity links in practice.


<span style="color: purple">  **LINK VALIDATION.** </span> The process of accepting or rejecting a link. This process is documented with the validation status (accepted or rejected) of the link and the supporting reasons.

<span style="color: purple">  **LINK SPECIFICATION.** </span> In the **Lenticular Lens**, a link specification can be view as a reproducibility metadata. It provides information on how set of links came to be. In other worlds, it explicitly defines the context in which a link hold and supports decisions making during the validation process (accepting or rejecting a link). 


<span style="color: purple">  **LINKSET/ALIGNMENT.** </span> In <span style="color:blue">[*VoID*]</span>, a linkset is a collection of RDF links between **two datasets** where all subjects stem from one dataset and all objects from the other dataset. In here, we alleviate such strict restriction by allowing a linkset to be a set of triples using the same link predicate (regardless of the link being an equality predicate or not) over one or two datasets. This predicate is called the linktype of the linkset. <br>
In the **Lenticular Lens**, all links within a linkset share the same generic link-specification.

<span style="color: purple">  **LENS.** </span> A type of linkset involving one, two or more datasets and a set-like link manipulation operators such as Union, Intersection, Difference or Transitivity.


<span style="color: purple">  **IDENTITY LINK NETWORK.** </span> A set of co-referent entities regardless of the data they stem from. This can also be viewed as an **Identity Cluster** of co-referent entities.


<span style="color: purple">  **NAMED GRAPH.** </span>  According to [Wikipedia](https://en.wikipedia.org/wiki/Named_graph), named graphs are a key concept of Semantic Web architecture in which a set of Resource Description Framework statements (a graph) are identified using a IRI, allowing descriptions to be made of that set of statements such as context, provenance information or other such metadata.

```
--------------------------
-- Example: NAMED GRAPH --
--------------------------
Turtle named graph syntax of a linkset of three links using the owl:sameAs linktype. 
In the example, http://example.org/#linkset-1 is the IRI of the named graph. For 
more detail on Turtle RDF syntax, See https://www.w3.org/TR/turtle/#simple-triples. 
where EXAMPLE 9 illustrates  all the different ways of writing IRIs in Turtle.

@base <http://example.org/> .
@prefix   ex: <http://example.org/#> .
@prefix  owl: <http://www.w3.org/2002/07/owl#> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix  sim: <http://purl.org/ontology/similarity/> .

ex:linkset-1
{
	ex:Chiara	owl:sameAs	ex:Latronico .
	ex:Al		owl:sameAs	ex:Al_Idrissou .
	ex:Al		owl:sameAs	ex:Al_Koudous .
}
```


<span style="color: purple">  **DEFAULT GRAPH.** </span> In a triple-store jargon, any triple without a specific named-graph ends up in the default graph. In the example below, the triple at line 4 is located in the default graph while triples at line 8 and 9 are in an **explicitly stated graph**, in the named-graph: ex:linkset-1.

```
----------------------------------
-- Example: DEFAULT NAMED-GRAPH --
----------------------------------

ex:Chiara	owl:sameAs	ex:Latronico .

ex:linkset-1
{
	ex:Al		owl:sameAs	ex:Al_Idrissou .
	ex:Al		owl:sameAs	ex:Al_Koudous .
}
```


<span style="color: purple">  **PREFIX.** </span>

Further prefixes used in this document are:

```
-----------------------------------------------
-- Example 5.1: PREFIXES USED IN THIS MANUAL --
-----------------------------------------------

   @prefix          A: <http://example.org/A#> .
   @prefix          B: <http://example.org/B#> .
   @prefix          C: <http://example.org/C#> .
	@prefix    dataset: <http://example.org/dataset#> .
	@prefix    dcterms: <http://purl.org/dc/terms/> .
	@prefix         ex: <http://example.org/#> .
	@prefix     format: <http://www.w3.org/ns/formats/> .
	@prefix       hero: <http://example.org/hero#> .
	@prefix        law: <http://www.opendatacommons.org/>
	@prefix        owl: <http://www.w3.org/2002/07/owl#> .
	@prefix     person: <http://example.org/person#> .
	@prefix       prov: <http://www.w3.org/ns/prov#> .
	@prefix        rdf:	<http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
	@prefix        rel: <http://www.perceive.net/schemas/relationship/> .
	@prefix        sim: <http://purl.org/ontology/similarity/> .
	@prefix       void: <http://rdfs.org/ns/void#> .
	@prefix   voidPlus: <http://vocabulary/voidPlus#> .
	@prefix validation: <http://vocabulary/validation#> .
	
```


<!--------------------------------------------------------------------->
# </span> <div id='The-Lenticular-Lens-Menu'/>
# <br> <span style="color:purple"> 3. THE LENTICULAR LENS MENUS </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!--------------------------------------------------------------------->

As a preview of what can be done with the **Lenticular Lens** tool, we list here the main manus composing the tool and provide a brief description of what can be done in each of the menu. 

* <span style="color:blue"> **RESEARCH.** </span> In this menu, we illustrates how to defined the scope of a research.

* <span style="color:blue"> **SELECT.** </span>  In this menu, we illustrates how to:
	* Use the default Golden Agent's endpoint or to provide other GraphQL locations so that remote datasources can be located and made available to the user;
	* Select (datasources and data-types) from the available list of datasources at the remote location so that data can be integrated and vital information can be extracted in order to conduct our experiment; 
	* Define restrictions over selected entity-types. 

* <span style="color:blue"> **CREATE.** </span>  In this menu, we show how to use and combine resolution methods.

* <span style="color:blue"> **MANIPULATE.** </span>  In this menu, we show how to apply set like operations (Union, Intersection, Difference, Composition and In-Set) over linksets and lenses.

* <span style="color:blue"> **VALIDATE.** </span>  In this menu, we show how to validate existing links (accept, reject, validation rational) for analysis or method accuracy. We also show in this menu how to use the visualisation feature to ease to some extent the validation task.

* <span style="color:blue"> **EXPORT.** </span> This menu illustrates the reach options supporting the export of a linkset or lens.

* <span style="color:blue"> **EXTRACT.** </span>  In this last menu, we show how the user can materialise the entity-based integration of her selected datasource for the extraction of information vital to her analysis. 

The rest of the manual will first discuss **LINK CONSTRUCTION** (it includes the `RESEARCH`, `SELECT` and `CREATE` menus), then **LINK MANIPULATION** (it includes the `MANIPULATE`, and `VALIDATION` menus), followed by **LINK EXPORT** (it explicitly about the `EXPORT` menus) and finally **INTEGRATION MODEL** (it explicitly about the `EXTRACT` menus).


<!--* <span style="color:blue"> **LINK CONSTRUCTION.** </span> It includes the `RESEARCH`, `SELECT` and `CREATE` menus.
* <span style="color:blue"> **LINK MANIPULATION.** </span> It includes the `MANIPULATE`, and `VALIDATION` menus.
* <span style="color:blue"> **LINK EXPORT.** </span> It explicitly about the `EXPORT` menus.-->





<!------------------------------------------------------------->
# </span> <div id='Link-Construction'/>
# <br> <span style="color:purple"> 4. LINK CONSTRUCTION </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!------------------------------------------------------------->

Linking co-referent entities across a variety of datasources is a pragmatic and fast way to seamlessly navigate across datasets without having to agree in a uniform vocabulary. This solution offered in the Semantic Web architecture appears attractive as the ultimate goal for the researcher executing this task is not the integration of data but the extraction of vital information for reaching valid conclusions about problems under scrutiny. 
This said, the **Lenticular Lens** offers means to reach that ultimate goal of the researcher while making sure that the steps taken by the researcher are documented such that other researchers can easily re-generate the data leading to specific conclusions if need be.

Along the way of entity-based data integration and data extraction, the **Lenticular Lens** aims to document among others: (1) reasons behind a specific integration; (2) datasources to integrate; (3) entity types and restrictions that ensure correctness in bridging across datasources of interest; and (4) matching methods and specifications justifying the existence of a set of links. It also aims to provide generic methods that allows a broader audience suffering the same problems undertaken by the le **Lenticular Lens**.

The first step in creating and documenting links using the **Lenticular Lens** is defining the scope in witch links are to be created and possibly validated. For that, the tool offers the `RESEARCH` menu followed by the `SELECT` and `CONSTRUCT` menus.

We now go through each of these first three menus underlying the existence of links.


# </span> <div id="Defining-the-Researchs-Scope"/>
## <span style="color:purple"> 4.1 Defining the Research's Scope</span>
<!------------------------------------------------------------------->

The `RESEARCH` menu is the starting point in learning how to interact with the **Lenticular Lens** tool. In general, a research question somehow sets the scope in which link creations, manipulations or validation take place. This provides the first building block supporting the user with defining the context in which a particular alignment is generated. Using this menu, part of the context is made explicit by selecting the datasets and entity types necessary to continue the investigation.

As an overview, the `RESEARCH` menu provides researchers with means to describe the research of interest in terms of:

* `Research Question` for inserting the main research question driving the integration. 
* `Hypothesis` for pointing out the hypothesis in mind prior to the data extraction. 
* `Link` and `Citation` to ensure that, if the results happen to be published, the researcher still has the facility to add a link to the publication and and a bibliographic reference for future reuse.

Fig. 4.1 illustrates the different fields to be filled in by the researcher for a quick overview of what can happen in this research project and why. Once providing the information is done, the `Save` button at the bottom of the page can be clicked to save the provided information and exit the **Lenticular Lens** if the user which to continue with other tasks. Or, should the user choose to continue the alternative `Save and next` button can be used to save the project and move to the next window.

 <div align="center"> ![The Lenticular Lens Research window](Images/LL_Research.jpg)Fig. 4.1:  Describing the scope of he research question. </div>
 <br>


# </span> <div id='Data-Selection-and-Restrictions'/>
## <span style="color:purple"> 4.2 Data Selection and Restrictions </span>
<!----------------------------------------------------------------------->

In the previous step or window, the researcher has defined the scope of the research for which data are to be extracted and analysed. In this second window labelled `SELECT`, the user is to describe and select the entity types involved in his research. For that, the location of the datasource needs to be provided and the datasets in which the respective entities of interest reside need to be selected.


# </span> <div id='Data-Selections'/>
### <span style="color:purple"> 4.2.1 Data Selections </span>
<!--------------------------------------------------------->

As the user activates the `Saves and next` button at the end of the previous page, she is presented with a new window with a single  card labelled `Entity-Type Selection 1` as presented in Fig. 4.2.  The plus  <sub>![](Images/LL_PlusButton.jpg)</sub> button at the right side of the picture enables the user to create new cards when needed while the arrow-head <sub>![](Images/LL_ArrowHead.jpg)</sub> button at the left side of the card's label allows for the unveiling of the card as displayed in Fig 3.

 <div align="center"> ![Explore Sample 1](Images/LL_Enty-Type-Selection-1.jpg) Fig. 4.2:  The card view for data selection </div>
<br>

Describing the type of an entity can be done using the `Description` text box for each entity type. To provide the location of the data, the `GraphQL Endpoint` text box can be use to fill in the URL of any GraphQL end point. Once the endpoint is given and loaded, a dataset can be selected from the list of datasets available at the provided endpoint. The selection of a dataset will prompt a new dropdown text box as `Entity type`, providing the user with the facility to select the entity type of interest. After loading the provided URL of the default Golden Agent's endpoint, Fig. 4.3 shows the list of datasets available at that location to choose from.

 <div align="center"> ![The Lenticular Lens Research window](Images/LL_Enty-Type-Selection.jpg) Fig. 4.3:  List of datasets available at the default Golden Agent's GraphQL endpoint. </div> <br>

# </span> <div id='Data-Exploration'/>
### <span style="color:purple"> 4.2.2 Data Exploration</span>
<!---------------------------------------------------------->

At this point, successfully providing the required information (`Dataset` and `Entity-Type`) triggers the appearance of the `Explore Sample` button at the right side of the card's label (`Entity-type selection 1`) as displayed in Fig. 4.4. As illustrated in Fig. 4.5, with this button, users are now able to explore information of their choice about the entities of interest by selecting properties describing them. Keep in mind that this feature is only intended as exploration alternative to make sure of the choices (dataset, entity-type and restrictions) made.

 <div align="center"> ![Explore Sample 1](Images/LL_Enty-Type-Selection-2.jpg) Fig. 4.4:  Example of the `Explore sample` button showing only after the entity type is selected. </div> <br>

 <div align="center"> ![Explore Sample 1](Images/LL_Enty-Type-Selection-3.jpg) Fig. 4.5:  Exploring the description of entities of choice, stemmed from the dataset of interest. </div> <br>


# </span> <div id='Entity-Restrictions'/>
### <span style="color:purple"> 4.2.3 Entity Restrictions </span>
<!-------------------------------------------------------------->

If need be to filter entities based on specific conditions, this is also possible with the `Filter` card shown in Fig. 4.6. <div align="center"> ![Entities Restrictions](Images/LL_Enty-Type-Selection-4-Filter.jpg) Fig. 4.6: The card for defining entity restrictions. </div> 

Once the <sub>![](Images/LL_PlusButton.jpg)</sub> button is clicked, this card presents the user with a Filter-Logic box which enable the creation of a relatively complex and versatile entity restrictions. Fig. 4.7 for example show the list of available filtering options while Fig. 4.8 illustrates an example where the `has minimum date` and `has maximum date` filtering options are used to isolate entities of interest. These entities are now those between with a registration date between [1600, 1659] and having their respective literal name exempt of trailing dots (...).

 <div align="center"> ![List of restriction options](Images/LL_Enty-Type-Selection-4-Filter-3.jpg) Fig. 4.7: List of restriction options. </div> <br>


 <div align="center"> ![Entities Restrictions](Images/LL_Enty-Type-Selection-4-Filter-2.jpg) Fig. 4.8: The card for defining entity restrictions. </div> <br>


# </span> <div id='Entity-restriction-options'/>
#### <span style="color:purple"> 4.2.3.1 Entity restriction options </span>
<!--------------------------------------------------------------------->

* <span style="color:blue"> **Equal to / Not Equal to.** </span> This option allows one to select entities that have the value of a certain property equal (or not) to a certain value. For example, all entities with property `ex:workLocation` equal (or not) to `Amsterdam`.<br>

* <span style="color:blue"> **Contains / Does not contain.** </span> This option is used to make sure that the property-value of the entities of interest **contains** or **does not contain** a specific sequence of characters. For example, `%...%` could be used for (i) excluding people whose names contain trailing dots or (ii) to select those entities to apply a particular modification onto their names, like adding the surname of the father for a baptised child whose surname is given as `...`.
<!--notifying that entities with names containing trailing dots are not to be included or that we would like to applied a particular modification onto those names.
-->

* <span style="color:blue"> **Has property / Has no property.** </span> This option is used to select entities based on the existence (or not) of a certain property. Let assume, for example, that the user is interested in entities that are parents. This option allows one to filter all entities for which the a value exists for the property `ex:parentOf` for example.  It also allows you to exclude all entities that are parents if the option `Has no property ` is used instead.<br>

* <span style="color:blue"> **Has minimum / maximum value.** </span> This option allows for restricting entities to be **within** or **outside** a **specified range** given user's specified property-values of type **number** over which the restriction can be applied. To delimit both upper and lower bounds, the user can combine minimum and maximum using the logical box AND.

* <span style="color:blue"> **Has minimum / maximum date.** </span> This option allows for restricting entities to be **within** or **outside** a **specified range** given user's specified property-values of type **date** over which the restriction can be applied. Within this option, a date format can be specified. The default format is `YYYY-MM-DD`. The values 10, 300 and 1990 for example will be considered as year while 10-1, 300-1 and 1990-1 will be considered as the first month of the respective year values. To delimit both upper and lower bounds, the user can combine minimum and maximum using the logical box AND.

* <span style="color:blue"> **Has minimum / maximum appearances.** </span> This option allows for restricting entities for which a given property value occurs **within** a **specified range**. For example, to avoid excessive number of possible matches, one can delimit that only entities whose name value occur less than 5 times in the dataset will be included. To delimit both upper and lower bounds, the user can combine minimum and maximum using the logical box AND.

* <span style="color:blue"> **In set.** </span> This option allows the filtering of a collection of resources of interest based on a set of resources. These set of resources is not manually provided but can be obtained through a list of existing linksets or lenses. The example below provides a detailed understanding of this filtering approach. 


	```
	---------------------
	-- Example: IN SET --
	---------------------
	Two collections A and B to be matched via whatever method would create a se of 
	links labelled linkset-AB. However, we are only interested in a subset of 
	linkset-AB, such that it's resources (subject, object or both) are present in 
	another given set, namely an input-linkset I. For efficiency purposes, 
	linkset-AB does not need to be fully created to be filtered later on. This 
	implies that the collections A and/or B need to be filtered such that 
	A' = A ∩ I and/or B' = B ∩ I before executing the matching algorithm.
	
		
		######################################################
		# 		  	Linksets as named graphs	             #
		######################################################
		
		ex:input-linkset
		{
			A:Chiara  owl:sameAs	  C:Latronico .
			A:Al      owl:sameAs	  C:Al_Idrissou .
			A:Al      owl:sameAs	  C:Al_Koudous .
		}
		
		ex:linkset-AB
		{
			A:Chiara  owl:sameAs	 B:Chiara .
			A:Kerim   owl:sameAs	 B:Kerim .
		}
		
		######################################################
		# 				In Resource Set			             #
		######################################################
		### The set S of resources from input-linkset is:
		### S = {A:Chiara, A:Al, C:Latronico, C:Al_Idrissou, C:Al_Koudous}
		
		ex:linkset-SubjectInSet
		{
			A:Chiara	owl:sameAs	B:Chiara .
		}
```
<br>
	
# </span> <div id='Entity-Resolution/Matching'/>
## <span style="color:purple"> 4.3 Entity Resolution/Matching </span>
<!----------------------------------------------------------------->

So far, the `RESEARCH` and `SELECT` menus set the scene for allowing the user to create the links that will enable the integration of datasources selected within the `SELECT` menus. In the current menu, the `CREATE` menu, we will describe the built-in entity resolution algorithms for finding links between entities stemmed from the user-selected datasets. Using the **Lenticular Lens** Logic-Box, we will show how the tool makes it possible to combine the available resolution algorithms and matching rules for the discovery of links within and/or across the datasources of interest.

# </span> <div id='Resolution-Methods'/>
### <span style="color:purple"> 4.3.1 Resolution Methods </span>
<!----------------------------------------------------------->

<p> <span style="color:blue">**​1. Embedded.** </span> The method extracts an alignment already provided within the source dataset. The extraction relies on the value of the linking property, i.e. property of the source that holds the identifier of the target. However, the real mechanism used to create the alignment is not explicitly provided by the source.

<span style="color:blue">**2. Exact.** </span> This method is used to align source and target’s IRIs whenever their respective user selected property values are identical.

<span style="color:blue">**3. Intermediate.** </span> The method aligns the source and the target’s IRIs via an intermediate database by using properties that potentially present different descriptions of the same entity, such as country name and country code. This is possible by providing an intermediate dataset that binds the two alternative descriptions to the very same identifier.

```
-----------------------------------
-- Example: INTERMEDIATE DATASET --
-----------------------------------
In the example below, it is possible to align the source and target country 
entities using the properties country and iso-3 via the intermediate dataset
because it contains the information described at both, the Source and Target.

dataset:Source-Dataset                       dataset:Intermediate-Dataset
{                                            {
	ex:1  rdfs:label  "Benin" .                 ex:7
	ex:2  rdfs:label  "Cote d'Ivoire" .              ex:name "Cote d'Ivoire" ;
	ex:3  rdfs:label  "Netherlands" .                ex:code "CIV" .
}	
                                                ex:8                             
dataset:Target-Datas                                ex:name "Benin" ;
{                                                   ex:code "BEN" .
	ex:4 ex:iso-3 "CIV" .
	ex:5 ex:iso-3 "NLD" .                       ex:9
	ex:6 ex:iso-3 "BEN" .                           ex:name "Netherlands" ;
}	                                                ex:code "NLD" .
	                                         }

ALIGNMENT: 
  • If rdfs:label is aligned with ex:name 
  • AND ex:iso-3 is aligned with ex:code,
  • We then get the following linkset:

	linkset:Match-Via-Intermediate
	{
		ex:1 owl:sameAs ex:6 .
		ex:2 owl:sameAs ex:4 .
		ex:3 owl:sameAs ex:5 .
	}

dataset:Source-Dataset                       dataset:Intermediate-Dataset
{                                            {
	ex:10  rdfs:label  "Rembrandt" .             ex:70
	ex:20  rdfs:label  "van Gogh" .                  ex:name "Vincent Willem van Gogh" ;
	ex:30  rdfs:label  "Vermeer" .                   ex:name "Vincent van Gogh" ;
}	                                                 ex:name "van Gogh" .
                                                ex:80                             
dataset:Target-Datas                                ex:name "Rembrandt" ;
{                                                   ex:name "Rembrandt van Rijn" .
	ex:40 schema:name "Rembrandt van Rijn" .
	ex:50 schema:name "Vincent van Gogh" .       ex:90
	ex:60 schema:name "Johannes Vermeer" .           ex:name "Johannes Vermeer" ;
}	                                                 ex:name "Vermeer" .
	                                         }
	
ALIGNMENT: 
  • If rdfs:label is aligned with ex:name 
  • AND schema:name is also aligned with ex:name,
  • we then get the following linkset:

	linkset:Match-Via-Intermediate
	{
		ex:10 owl:sameAs ex:40 .
		ex:20 owl:sameAs ex:50 .
		ex:30 owl:sameAs ex:60 .
	}
	
	
```

<br> <span style="color:blue"> **4. Levenshtein Distance.** </span> This ​method is used to align ​​source a​nd ​​target’s IRIs whenever the similarity score of their respective user selected property values are ​​above a given ​Levenshtein Distance threshold​.

Edit distance is a way of quantifying how ​dissimilar two strings (e.g., words) are to one another by counting the minimum number of operations ​ε ​ (​removal, insertion, or substitution of a character in the string)​ required to transform one string into the other. For example, ​the ​Levenshtein distance between "kitten" and "sitting" is ​ε ​= 3 as it requires a two substitutions ("s" for "k" and "i" for "e") and one insertion of "g" at the end [https://en.wikipedia.org/wiki/Edit_distance]​.

**Normalisation ​Ω​:** Because in this application, the ​similarity score ​Ω ​of a matching pair needs to be quantified in the interval ​[0, 1]​, the​ dissimilarity score ​ε expressing the ​minimum number of operations ​between two strings ​is then normalised as ​Ω based on the length of the longest string. The ​dissimilarity score​​ ε​ = 3 ​between ​"kitten" and "sitting" is then normalised to a ​similarity score Ω​ ​=​ ​1 - 3 / 7 = 0.57​.​

**Minimum threshold ​φ:** Using this algorithm, ​a ​minimum threshold valueφ​ ​must be set in the interval ​[0,1], ​such that finding any matched pairs of IRIs based on the similarity of their respective property values depends on whether or not the computed ​Ω is ​equal or above ​φ​. A threshold ​φ = 1 equates an exact match. In our previous example, if a ​minimum threshold of ​φ = ​0.7 is set, "kitten" and "sitting" will not be matched. ​In short, ​φ is the user defined threshold when the similarity score ​Ω is selected for accepting or rejecting a match.

**Maximum character error threshold ​𝛿:​** In case the ​original edit distance score ​ε (minimum number of operations score) is preferred, the number of character errors ​𝛿 ​of choice is used instead as threshold for deciding whether a match is accepted or rejected. However, for consistency purposes, the corresponding normalisation value ​Ω is still computed for the minimum number of operations score computed ​ε​. For instance, in our previous example, if a ​maximum ​characters errors i​s set to ​𝛿 = 3, "kitten" and "sitting" will be matched but the computed strength will be ​Ω = ​0.57 a​nd ​not ​ε = 3 as is it only serves the purpose of decision maker. I​n short, ​𝛿 i​s the user defined threshold when the dissimilarity score ε​ ​is selected for accepting or rejecting a match.

```
----------------------------
-- Example: NORMALIZATION --
----------------------------

	1. l_dist(Rembrand van Rijn, Rembrandt Harmensz van Rijn) = 10
	2. Normalised_l_dist ​(Rembrand van Rijn, Rembrandt Harmensz van Rijn) = 0.63
	
	>>> If ​φ (Minimum threshold) = 0.7 
	>>> t​hen ​[​Rembrand van Rijn] owl:sameAs [Rembrandt Harmensz van Rijn] 
	>>> is rejected​ 
	>>> because Ω​ = 0.63 < φ​.
	
	>>> If ​δ (Maximum character error threshold) = 5 
	>>> t​hen [​​Rembrand van Rijn] and [Rembrandt Harmensz van Rijn] is ​rejected 
	>>> because ε ​= 10 >​ ​δ.
```

<br> <span style="color:blue">**5. Soundex Distance.** </span> “Soundex is a phonetic algorithm for indexing names by sound, as pronounced in English. The goal is for homophones to be encoded to the same representation so that they can be matched despite minor differences in spelling. The algorithm mainly encodes consonants; a vowel will not be encoded unless it is the first letter” [ https://en.wikipedia.org/wiki/Soundex]. <br


```
--------------------------------
-- Example: SOUNDEX CODE SIZE --
--------------------------------
The examples below shows the encoding of different names. Here, the size 
parameter indicates a degree of similarity through the length of the 
respective soundex codes. For example at  size=3, Albert and Albertine 
have the same soundex representation while at size=5 their  respective 
representations differ. In the Lenticular lens, the default size is set 
to 3.

	-----------------------------
	INPUT 	 	 SIZE 3   SIZE 5  
	-----------------------------
	A.      	 A000     A00000                                  
	AL			 A400     A40000                                 
	ALI			 A400     A40000                               
	ALBERT		 A416     A41630                                
	ALBERTINE	 A416     A41635 
```
In the **Lenticular Lens**, Soundex is used as a normaliser in the sense that an edit distance is run over the soundex code version of a name. For example, the in the table below, the normalisation of both `Louijs Rocourt ` and ``Lowis Ricourt` becomes `L200 R263` leading to an edit distance of 0 and a relative strength of 1. However, computing the same names using directly an edit distance results in an edit distance of 3 and a relative matching strength of 0.
79.

```
---------------------------------------------------------------
-- Example: THE USE OF SOUNDEX CODE FOR STRING APPROXIMATION --
---------------------------------------------------------------
The example below shows the implementation of Soundex Distance 
in the Lenticular Lens and how it compares with Edit Distance
over the original names (no soundex-based normalisation).

------------------------------------------------------------------------------------------------------------------------------------------------------
Source                      Target                     E. Dist  Rel. distance  Source soundex       Target  soundex       Code E. Dist  Code Rel. Dist
------------------------------------------------------------------------------------------------------------------------------------------------------
Jasper Cornelisz. Lodder    Jaspar Cornelisz Lodder          2           0.92  J216 C654 L360       J216 C654 L360                   0             1.0
Barent Teunis               Barent Teunisz gen. Drent       12           0.52  B653 T520            B653 T520 G500 D653             10            0.47
Louijs Rocourt              Louys Rocourt                    2           0.86  L200 R263            L200 R263                        0             1.0
Louijs Rocourt              Lowis Ricourt                    3           0.79  L200 R263            L200 R263                        0             1.0
Louys Rocourt               Lowis Ricourt                    3           0.77  L200 R263            L200 R263                        0             1.0
Cornelis Dircksz. Clapmus   Cornelis Clapmuts               10            0.6  C654 D620 C415       C654 C415                        5            0.64
Geertruydt van den Breemde  Geertruijd van den Bremde        4           0.85  G636 V500 D500 B653  G636 V500 D500 B653              0             1.0


```


<br> <span style="color:blue">**6. Gerrit Bloothooft.** </span> This approximation method is specifically tailored for accessing the similarity between a pair of  IRIs for which the user selected property values are Dutch names. The algorithm basically normalises the given names by removing or replacing specific characters…. 
The resulting normalised names are then pairwise compared using the Approximated Levenshtein Distance (see the description of Approximated Levenshtein Distance).

```
Example
-------
                              
```

<br> <span style="color:blue">**7. Word Intersection.** </span> This approximation method is originally designed to find a subset of words within a larger text. However, it could also be used for any  pair of strings regardless of the strings sizes. Several options are available: 

* Whether or not the order in which the words are found is important.
* Whether or not the computed strength of each word should be approximated or identical.
* Whether or not abbreviation should be detected.
* Whether the default stopping character should be used, not used or modified.
* A threshold on the number of words not approximated/identical.
* An overall  threshold for accepting or rejecting a match.


```
---------------------------
-- Example: EXPECTATIONS --
---------------------------
	For example, it can be used for aligning 
	 - [Rembrand van Rijn] and [van Rijn Rembrandt]
	 - [Herdoopers anslagh op Amsterdam] and [Herdoopers anslagh op Amsterdam. 
	    Den x. may: 1535. Treur-spel.]
	regardless of the words' order.

```



<br> <span style="color:blue">**9. Numbers.** </span> The method is used to align the source and the target by approximating the match of the (number/date) values of the selected properties according to a delta. For example, if two entities have been aligned based on the similarity of their names but an extra check is to be investigated based on their respective year of birth, setting the delta to 1 will ensure that the two entities are born within the same year, give or take a year. 


<br> <span style="color:blue">**10. TeAM.** </span> This method allows for the approximation of the relevance of a document to a query. Such approximation can be done using lexical similarity (word level similarity), semantic similarity or hybrid similarities. In this method, the focus is rather on the lexical similarity. Although tailored to text, it has been adapted to also be applicable to name-based similarity. We now provide an overview of the motivation context supporting the design and implementation of the algorithm.

The Amsterdam's city archives (SAA) possesses physical handwritten inventories records where a record may be for example an inventory of goods (paintings, prints, sculpture, furniture, porcelain, etc.) owned by an Amsterdamer and mentioned in a last will. Interested in documenting the ownership of paintings from the 17th century, the Yale University Professor John Michael Montias compiled a database by transcribing 1280 physical handwritten inventories (scattered in the Netherlands) of goods. Now that a number of these physical inventories have been digitised using handwriting recognition, one of the goals of the Golden Agent project is to identify Montias' transcriptions of painting selections within the digitised inventories. This problem can be generically reformulated as, given a <span style="color:blue">*source-segment database (e.g. Montias DB)*</span> and a <span style="color:blue">*target-segment database (e.g. SAA)*</span>, *find the best similar target segment  for each source segment*. 



 <div align="center"> ![Inventory](Images/Inventory.jpg) Fig 4.9: An example of the digitisation of inventory documents available at the Amsterdam's city archives. </div> 

<br>

# </span> <div id='Complex-Methods'/>
### <span style="color:purple"> 4.3.2 Complex Methods </span>
<!--https://en.wikipedia.org/wiki/T-norm-->

This section addresses **Complex Methods** as ways to combine matching methods, not to be confused with the complexity of the underlying the methods. 
All of the matching methods described earlier generate links with matching strength scores in the interval ]0, 1]. 
We saw for example that the relative strength score between ​`Rembrand van Rijn` and `Rembrandt Harmensz van Rijn` is 0.63 using the Levenshtein algorithm and 0.74 using Soundex. 
Those methods can be combined at time of creation of the linkset, using logic boxes, or afterwards, using lenses operators.

When such combination happens, a decision is necessary regarding the calculation of the resulting strength score.
For example, let us assume that links are created whenever a pair of datasets items (subject, object) either **sounds alike** or **looks alike character-wise**. 
To accomplish that, it means that two methods have to be combined, for example, Soundex and Levenshtein. 
Although combining the methods seems relatively easy, deciding on the matching score requires some extra thoughts. 
In the example above of Rembrandt, shall we consider 0.63 or 0.74? Or their product?
Here we discuss the rationals used in the **Lenticular lens** to support such decision.

<!--In this section, **Complex Method** is not related to the complexity of the underlying method. Instead, here, any user combined matching method is what we denote as a **Complex Method**. All of the matching methods described earlier generate links with matching strength scores in the interval ]0, 1]. We saw for example that, using the Levenshtein algorithm, the relative strength score between ​`Rembrand van Rijn` and `Rembrandt Harmensz van Rijn` is 0.63. 
Now, let us assume that we want to generate links whenever the pair of datasets items (subject, object) either **sounds alike** or **looks alike character-wise**. To accomplish that, it means that two methods have to be combined, namely Soundex and Levenshtein. Well, combining the methods sounds relatively easy. However deciding on the matching score requires some extra thoughts. Here we discuss the rational used in the **Lenticular lens** for such computations.
For combining methods, two logic operators are available: Conjunction (AND) and Disjunction (OR). <br>
When combing methods with the traditional `AND` logic operator its requires both side to be valid. Here, because we are dealing with **fuzzy logic**, we decide to use the **T-norm binary operations** as provided below.
-->

<!--The two standard logic operators traditionally used are **Conjunction (AND)** and **Disjunction (OR)**. The first takes the minimum strength and the latter takes the maximum.
-->
The two standard logic operators traditionally used are **Conjunction (AND)** and **Disjunction (OR)**. 
The first takes the minimum strength and the latter takes the maximum strength. This applies for both **classic values** (True -1- or False -0-) and **fuzzy values** ( between 0 and 1 ). 
<!--The table bellow illustrates the default behaviour of the Lenticular Lens when combining fuzzy values resulting from matching methods.
-->
Since the results from matching methods are **fuzzy values** in the interval ]0,1], the table bellow illustrates the default behaviour of the Lenticular Lens when combining them.



```

Source                      Target                       Levenshtein  Soundex      OR(max)    AND(min)
------------------------------------------------------------------------------------------------------
Jasper Cornelisz. Lodder    Jaspar Cornelisz Lodder             0.92     1.00        1.00         0.92
Rembrand van Rijn           Rembrandt Harmensz van Rijn         0.63     0.74        0.74         0.63
Barent Teunis               Barent Teunisz gen. Drent           0.52     0.47        0.52         0.47


```  

However, more sophisticated operations can also be used, such as the **T-norm binary operations** as alternatives for **Conjunction (AND)** and the **T-conorm binary operations** as alternatives for **Disjunction (OR)** as provided in the next subsections.

# </span> <div id='T-norms'/>
### <span style="color:purple"> 4.3.2.1 T-norms </span>

A list of six different operations can be applied when dealing with methods combined by **Conjunction**. Here, we present them:

* Minimum t-norm ⊤<sub>min</sub> (a, b) = min{a, b}
* Product t-norm ⊤<sub>prod</sub> (a, b) = a . b
* Łukasiewicz t-norm ⊤<sub>Luk</sub> (a, b) = max(0, a+b-1)
* Drastic t-norm ⊤<sub>D</sub> (a, b) = b (if a = 1) , a (if b = 1), 0 (otherwise)
* Nilpotent minimum ⊤<sub>nM</sub> (a, b) = min{a, b} (if a + b > 1), 0 (otherwise)
* Hamacher product ⊤<sub>H<sub>0</sub></sub> (a, b) = 0 (if a = b = 0), ab / (a + b - ab) (otherwise)


<!--|Source, Target                                                        | Levenshtein, Soundex | T<sub>min</sub> | T<sub>prod</sub> | T<sub>Luk</sub> | T<sub>D</sub>  | T<sub>nM</sub> | <sub>H<sub>0</sub></sub> |
|--------------------------------------------------------------------------|----------------------|-----------------|------------------|-----------------|----------------|----------------|--------------------------|
| **Src**: Jasper Cornelisz. Lodder <br> **Trg**: Jaspar Cornelisz Lodder  |           0.92, 1.00 |     0.920       |            0.92  |           0.920 |          0.920 |          0.920 |                    0.920 |
| **Src**: Rembrand van Rijn <br> **Trg**: Rembrandt Harmensz van Rijn     |           0.63, 0.74 |     0.630       |            0.466 |           0.370 |              0 |          0.630 |                    0.516 |
| **Src**: Barent Teunis <br> **Trg**: Barent Teunisz gen. Drent           |           0.52, 0.47 |     0.470       |            0.244 |           0.000 |              0 |          0.000 |                    0.328 |-->

The following table provides three case studies to illustrate the application of each of the aforementioned **T-norm binary operations**. They are presented in order from the less strict (**⊤<sub>min</sub>**) to the most strict (**⊤<sub>D</sub>**).

|Source, Target                                                            | Levenshtein, Soundex | ⊤<sub>min</sub> | ⊤<sub>H<sub>0</sub></sub> | ⊤<sub>prod</sub> | ⊤<sub>nM</sub>  | ⊤<sub>Luk</sub> | ⊤<sub>D</sub> |
|--------------------------------------------------------------------------|:--------------------:|-----------------|---------------------------|-------------------|-----------------|-----------------|----------------|
| **Src**: Jasper Cornelisz. Lodder <br> **Trg**: Jaspar Cornelisz Lodder  |           0.92, 1.00 |     0.920       |                     0.920 |             0.920 |           0.920 |           0.920 |          0.920 |
| **Src**: Rembrand van Rijn <br> **Trg**: Rembrandt Harmensz van Rijn     |           0.63, 0.74 |     0.630       |                     0.516 |             0.466 |          0.630  |           0.370 |          0.000 |
| **Src**: Barent Teunis <br> **Trg**: Barent Teunisz gen. Drent           |           0.52, 0.47 |     0.470       |                     0.328 |             0.244 |          0.000  |           0.000 |          0.000 |


# </span> <div id='T-conorms'/>
### <span style="color:purple"> 4.3.2.2 T-conorms </span>

A list of six different operations can also be applied when dealing with methods combined by **Disjunction**. Here, we present them:

* Maximum t-conorm ⊥<sub>max</sub> (a, b) = max{a, b}
* Probabilistic sum ⊥<sub>sum</sub> (a, b) = a + b - a.b
* Bounded sum ⊥<sub>Luk</sub> (a, b) = min{a + b, 1}
* Drastic t-conorm ⊥<sub>D</sub> (a, b) = b (if a=0), a (if b=0), 1 (otherwise)
* Nilpotent maximum ⊥<sub>nM</sub> (a, b) = max(a, b) (if a + b < 1), 1 (otherwise)
* Einstein sum ⊥<sub>H<sub>2</sub></sub> (a, b) = (a + b) / (1 + ab)

|Source, Target                                                            | Levenshtein, Soundex | ⊤<sub>D</sub>   | ⊤<sub>Luk</sub>  | ⊤<sub>H<sub>2</sub></sub> | ⊤<sub>sum</sub> | ⊤<sub>nM</sub>  |   ⊤<sub>max</sub> |
|--------------------------------------------------------------------------|:--------------------:|-----------------|------------------|----------------------------|-----------------|-----------------|--------------------|
| **Src**: Jasper Cornelisz. Lodder <br> **Trg**: Jaspar Cornelisz Lodder  |           0.92, 1.00 |     1.000       |            1.000 |                      1.000 |           1.000 |           1.000 |              1.000 |
| **Src**: Rembrand van Rijn <br> **Trg**: Rembrandt Harmensz van Rijn     |           0.63, 0.74 |     1.000       |            1.000 |                      0.934 |          0.904  |           1.000 |              0.740 |
| **Src**: Barent Teunis <br> **Trg**: Barent Teunisz gen. Drent           |           0.52, 0.47 |     1.000       |            0.990 |                      0.796 |          0.746  |           0.520 |              0.520 |


# </span> <div id='Example-of-complex-methods'/>
### <span style="color:purple"> 4.3.2.3 Example of complex method </span>
<!--For a higher level of accuracy, let us assume that, two data items representing persons are co-referent, if then pass the following tests:
-->

Let us assume that, two data items representing persons are co-referent, if then pass the following tests:

1. AND (score must be greater than 0.8) 
  * OR: Name Comparison
  	 * 	Levenshtein (score must be greater than 0.7) 
  	 *  Soundex (score must be greater than 0.7) 
  * OR: Parent Name Comparison
  	 *  Fathers (Levenshtein greater than 0.6)
  	 *  Mothers (Levenshtein greater than 0.6)
  * OR: Dates Comparison
  	 * Identical birth dates  
  	 * The delta between marriage and child's baptisms is less than 25 years


Now we take the following data to compute and compare results obtained using different operations:

```

** MATCHING RESULTS: **
Levenshtein(Titus Rembrandtsz. van Rijn, T. Rembrandtszoon van Rijn) => 0.74
Soundex(Titus Rembrandtsz. van Rijn, T. Rembrandtszoon van Rijn)     => 0.85
Levenshtein(Rembrand van Rijn, Rembrandt Harmensz van Rijn)          => 0.63
Levenshtein(Saskia Uylenburgh, Saske van Uijlenburg)                 => 0.65
ExactDate(1641-09-22, 1641-09-22)                                    => 1.00
Delta(1668-02-28, 1669-03-22, 25)                                    => 1.00


** DISJUNCTIONS **
names   = t_conorm(0.74, 0.85, 'MAXIMUM')          => names   = 0.850
parents = t_conorm(0.62, 0.65, 'PROBABILISTIC')    => parents = 0.867
dates   = t_conorm(1.00, 1.00, 'MAXIMUM')          => dates   = 1.000


** PARTIAL CONJUNCTIONS **  ### Ops.t_norm(names, parents, OPERATION)
partial_1 = Ops.t_norm(0.850, 0.867, 'NILPOTENT')  => partial_1 = 0.850
partial_2 = Ops.t_norm(0.850, 0.867, 'PRODUCT')    => partial_2 = 0.737
partial_3 = Ops.t_norm(0.850, 0.867, 'MINIMUM')    => partial_3 = 0.850
partial_4 = Ops.t_norm(0.850, 0.867, 'HAMACHER')   => partial_4 = 0.752


** FINAL CONJUNCTIONS **  ### Ops.t_norm(partial_i, dates, OPERATION)
result_1 = Ops.t_norm(0.850, 1.0, 'NILPOTENT')     => result_1 = 0.850
result_2 = Ops.t_norm(0.737, 1.0, 'DRASTIC')       => result_1 = 0.737
result_3 = Ops.t_norm(0.850, 1.0, 'MINIMUM')       => result_1 = 0.850
result_4 = Ops.t_norm(0.752, 1.0, 'HAMACHER')      => result_1 = 0.752


``` 

Given the operations described above, only result_1 and result_3 would pass the final threshold defined as 0.8.

# </span> <div id='Matching-in-Practice'/>
### <span style="color:purple"> 4.3.3 Matching in Practice </span>
<!--------------------------------------------------------------->
Now that we have gone through possible methods available in the **Lenticular Lens**, we show how these methods can be used individually or in combination to align resources stemmed from various datasources of one's choice.

# </span> <div id='Case-Study-1'/>
#### <span style="color:purple"> Case Study:  </span>

# </span> <div id='Case-Study-2'/>
#### <span style="color:purple"> Case Study:  </span>

# </span> <div id='Case-Study-3'/>
#### <span style="color:purple"> Case Study:  </span>

# </span> <div id='Case-Study-4'/>
#### <span style="color:purple"> Case Study:  </span>


# </span> <div id='Matching-Results'/>
### <span style="color:purple"> 4.3.2 Matching Results </span>
<!----------------------------------------------------------->


<span style="color: purple">  **LINKSET.** </span>

<span style="color: purple">  **LENS.** </span>


<!------------------------------------------------------------->
# </span> <div id='Link-Manipulation'/>
# <br> <span style="color:purple"> 5. LINK MANIPULATION </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!------------------------------------------------------------->
After generating a number of linksets and lenses, one may want to combine or split some of the links. Others may want to infer new links using existing alignments. The `MANIPULATE` menu provides means for exacting doing that by making it possible to apply set like operators such as UNION, INTERSECTION, DIFFERENCE, TRANSITIVE and IN-SET over alignments in ways that suits bets the user according to her envisaged final integration goal. <br>


```
-----------------
-- Example 5.1 --
-----------------
Deduplicating Greatest Comics Superheroes.

ex:DCHeroesIdentity
    a                     void:Linkset ;
    dcterms:description   "Identifying DC's comics superheroes" ;
    void:subjectsTarget   dataset:DC-Comics;
    void:objectsTarget    dataset:DC-Comics;
    void:triples          10 ;
    • • •
    
ex:MarvelHeroesIdentity
    a                     void:Linkset ;
    dcterms:description   "Identifying Marvel Universes' superheroes" ;
    void:subjectsTarget   dataset:Marvel-Univers;
    void:objectsTarget    dataset:Marvel-Univers ;
    void:triples          10 ;
    • • •

ex:DCHerosIdentity
{
	<<hero:Superman         owl:sameAs  person:Clark-Kent>>          validation:status "True" .
	<<hero:Batman           owl:sameAs  person:Bruce-Wane>>          validation:status "True" .
	<<hero:Flash            owl:sameAs  person:Barry-Allen>>         validation:status "True" .
	<<hero:GreenLantern     owl:sameAs  person:Alan-Scott>>          validation:status "True" .
	<<hero:WonderWoman      owl:sameAs  person:Diana-Prince>>        validation:status "True" .
	<<hero:Aquaman          owl:sameAs  person:Arthur-Curry>>        validation:status "True" .
	<<hero:GreenArrow       owl:sameAs  person:OliverQueen>>         validation:status "True" .
	<<hero:BoosterGold      owl:sameAs  person:Michael-Jon-Carter>>  validation:status "True" .
	<<hero:Spider-man       owl:sameAs  person:Piter-Parker>>        validation:status "False" .
	<<hero:Iron-man         owl:sameAs  person:Tony-Stark>>          validation:status "False" .   
}

ex:MarvelHerosIdentity
{
    <<hero:Captain-Marvel   owl:sameAs  person:Carol-Danvers>>     validation:status "True" .
    <<hero:Captain-America  owl:sameAs  person:Steve-Rogers>>      validation:status "True" .
    <<hero:Deadpool         owl:sameAs  person:Wade-Wilson>>       validation:status "True" .
    <<hero:Black-Panther    owl:sameAs  person:T-Challa>>          validation:status "True" .
    <<hero:Spider-man       owl:sameAs  person:Piter-Parker>>      validation:status "True" .
    <<hero:Iron-man         owl:sameAs  person:Tony-Stark>>        validation:status "True" .
    <<hero:Ant-man          owl:sameAs  person:Tony-Stark>>        validation:status "True" .
    <<hero:Black-Widow      owl:sameAs  person:Natasha-Romanoff>>  validation:status "True" .
    <<hero:Hulk             owl:sameAs  person:Bruce-Banner>>      validation:status "True" .
    <<hero:Hawkeye          owl:sameAs  person:Clint-Barton>>      validation:status "True" .
}
```


# </span> <div id='Union'/>
## <br> <span style="color:purple"> 5.1 Union </span>
<!------------------------------------------------------------->
Imagine having  


```
##############################################################
#     MARVEL: Annotated Linkset of 6 Identity Statements     #
##############################################################

ex:Marvel-Heroes-Identity-1
    a                       void:Linkset ;
    dcterms:subject         "Fictitious Heroes" ;
    dcterms:description     "Identifying Marvel Universes' superheroes" ;
    void:subjectsTarget     dataset:Superheroes ;
    void:objectsTarget      dataset:Fictitious-Persons ;
    void:triples            6 .

ex:Marvel-Heroes-Identity-1
{
 	<<hero:Black-Widow      owl:sameAs  person:Natasha-Romanoff>>  validation:status true .
 	<<person:Bruce-Banner   owl:sameAs  hero:Hulk>>                validation:status true .
	<<hero:Captain-America  owl:sameAs  person:Steve-Rogers>>      validation:status true .
    <<hero:Captain-Marvel   owl:sameAs  person:Carol-Danvers>>     validation:status true .
    <<hero:Deadpool         owl:sameAs  person:Wade-Wilson>>       validation:status true .
    <<hero:Black-Panther    owl:sameAs  person:T-Challa>>          validation:status true .
}

##############################################################
#     MARVEL: Annotated Linkset of 4 Identity Statements     #
##############################################################

ex:Marvel-Heroes-Identity-2
    a                       void:Linkset ;
    dcterms:subject         "Fictitious Heroes" ;
    dcterms:description     "Identifying Marvel Universes' superheroes" ;
    void:subjectsTarget     dataset:Fictitious-Persons ;
    void:objectsTarget      dataset:Superheroes ;
    void:triples            4 .

ex:Marvel-Heroes-Identity-2
{
    <<person:Piter-Parker      owl:sameAs  hero:Spider-man>>       validation:status true .
    <<person:Tony-Stark        owl:sameAs  hero:Iron-man>>         validation:status true .
    <<person:Tony-Stark        owl:sameAs  hero:Ant-man>>          validation:status true .
    <<person:Clint-Barton      owl:sameAs  hero:Hawkeye>>          validation:status true .
}

##############################################################
# DC-COMICS: Non Annotated Linkset of 10 Identity Statements #
##############################################################
ex:Marvel-Heroes-Identity-2
    a                       void:Linkset ;
    dcterms:subject         "Fictitious Heroes" ;
    dcterms:description     "Identifying DC Comics Universes' superheroes" ;
    void:triples            9 .
    
ex:DC-Heros-Identity
{
    hero:Superman       owl:sameAs  person:Clark-Kent .
    hero:Batman         owl:sameAs  person:Bruce-Wane .
    hero:GreenLantern   owl:sameAs  person:Alan-Scott .
    hero:WonderWoman    owl:sameAs  person:Diana-Prince .
    hero:Aquaman        owl:sameAs  person:Arthur-Curry .
    hero:GreenArrow     owl:sameAs  person:OliverQueen .
    hero:BoosterGold    owl:sameAs  person:Michael-Jon-Carter .
    hero:Spider-man     owl:sameAs  person:Piter-Parker .
    hero:Iron-man       owl:sameAs  person:Tony-Stark .   
}


##############################################################
#                      UNION of 3 LINKSETS                   #
##############################################################	

ex:Union-Marvel-DC-Heroes
    a                       void:Linkset ;
    dcterms:description     "Identifying Marvel Universes' superheroes" ;
    void:target             ex:Marvel-Heroes-Identity-1 ;
    void:target             ex:Marvel-Heroes-Identity-2 ;
    void:target				ex:DCHerosIdentity-1 ;
    void:triples            10 .
    
ex:Union-Marvel-Heroes
{
    <<hero:Black-Widow      owl:sameAs  person:Natasha-Romanoff>>    prov:wasDerivedFrom  ex:Marvel-Heroes-Identity-1 .
	<<hero:Captain-America  owl:sameAs  person:Steve-Rogers>>        prov:wasDerivedFrom  ex:Marvel-Heroes-Identity-1 .
    <<hero:Captain-Marvel   owl:sameAs  person:Carol-Danvers>>       prov:wasDerivedFrom  ex:Marvel-Heroes-Identity-1 .
    <<hero:Deadpool         owl:sameAs  person:Wade-Wilson>>         prov:wasDerivedFrom  ex:Marvel-Heroes-Identity-1 .
    <<hero:Black-Panther    owl:sameAs  person:T-Challa>>            prov:wasDerivedFrom  ex:Marvel-Heroes-Identity-1 .
    
    <<hero:Spider-man       owl:sameAs  person:Piter-Parker>>
    	prov:wasDerivedFrom    ex:Marvel-Heroes-Identity-2 ;
    	prov:wasDerivedFrom    ex:Marvel-Heroes-Identity.
    
    <<hero:Iron-man         owl:sameAs  person:Tony-Stark>> 
    	prov:wasDerivedFrom    ex:Marvel-Heroes-Identity-2 ;
    	prov:wasDerivedFrom    ex:Marvel-Heroes-Identity.
    	
    <<hero:Ant-man          owl:sameAs  person:Tony-Stark>>          prov:wasDerivedFrom  ex:Marvel-Heroes-Identity-2 .
    <<hero:Hulk             owl:sameAs  person:Bruce-Banner>>        prov:wasDerivedFrom  ex:Marvel-Heroes-Identity-2 .
    <<hero:Hawkeye          owl:sameAs  person:Clint-Barton>>        prov:wasDerivedFrom  ex:Marvel-Heroes-Identity-2 .

    <<hero:Superman         owl:sameAs  person:Clark-Kent>>          prov:wasDerivedFrom  ex:Marvel-Heroes-Identity.
    <<hero:Batman           owl:sameAs  person:Bruce-Wane>>          prov:wasDerivedFrom  ex:Marvel-Heroes-Identity .
    <<hero:Flash            owl:sameAs  person:Barry-Allen>>         prov:wasDerivedFrom  ex:Marvel-Heroes-Identity .
    <<hero:GreenLantern     owl:sameAs  person:Alan-Scott>>          prov:wasDerivedFrom  ex:Marvel-Heroes-Identity .
    <<hero:WonderWoman      owl:sameAs  person:Diana-Prince>>        prov:wasDerivedFrom  ex:Marvel-Heroes-Identity .
    <<hero:Aquaman          owl:sameAs  person:Arthur-Curry>>        prov:wasDerivedFrom  ex:Marvel-Heroes-Identity .
    <<hero:GreenArrow       owl:sameAs  person:OliverQueen>>         prov:wasDerivedFrom  ex:Marvel-Heroes-Identity .
    <<hero:BoosterGold      owl:sameAs  person:Michael-Jon-Carter>>  prov:wasDerivedFrom  ex:Marvel-Heroes-Identity . 
}
```


<!--```
----------------------------------------------
-- Example 5.1: Greatest Comics Superheroes --
----------------------------------------------

ex:ComicsHeroesIdentity
    a                     voidPlus:LensUnion ;
    dcterms:description   "Identifying superheroes from Marvel and DC comics" ;
    voidPlus:expression   "ex:DCHerosIdentity UNION ex:MarvelHerosIdentity" ;
    void:target           ex:DCHerosIdentity , ex:MarvelHerosIdentity ;
    void:triples          22 ;
    • • •
    
ex:ComicsHeroesIdentity
{
	• • •
	<<hero:WonderWoman      owl:sameAs  person:Diana-Prince>>        prov:wasDerivedFrom  ex:DCHerosIdentity .
	<<hero:BoosterGold      owl:sameAs  person:Michael-Jon-Carter>>  prov:wasDerivedFrom  ex:DCHerosIdentity .
	
	<<hero:Spider-man       owl:sameAs  person:Piter-Parker>>
		prov:wasDerivedFrom   ex:DCHerosIdentity ;
		prov:wasDerivedFrom   ex:MarvelHerosIdentity .
		
		
	<<hero:Iron-man         owl:sameAs  person:Tony-Stark>> 
		prov:wasDerivedFrom   ex:DCHerosIdentity ;
		prov:wasDerivedFrom   ex:MarvelHerosIdentity .

    <<hero:Captain-Marvel   owl:sameAs  person:Carol-Danvers>> prov:wasDerivedFrom  ex:MarvelHerosIdentity .
    <<hero:Captain-America  owl:sameAs  person:Steve-Rogers>>  prov:wasDerivedFrom  ex:MarvelHerosIdentity .    
    <<hero:Deadpool         owl:sameAs  person:Wade-Wilson>>   prov:wasDerivedFrom  ex:MarvelHerosIdentity .
    • • •
}
```
-->


# </span> <div id='Intersection'/>
## <br> <span style="color:purple"> 5.2 Intersection </span>
<!------------------------------------------------------------->

```
----------------------------------------------
-- Example 5.1: Greatest Comics Superheroes --
----------------------------------------------

ex:ComicsHeroesIdentity
    a                     voidPlus:LensUnion ;
    dcterms:description   "Quality Check: Identifying superheroes from both Marvel and DC comics" ;
    voidPlus:expression   "ex:DCHerosIdentity INTERSECTION ex:MarvelHerosIdentity" ;
    void:target           ex:DCHerosIdentity , ex:MarvelHerosIdentity ;
    void:triples          4 ;
    • • •
    
ex:ComicsHeroesIdentity
{	
	<<hero:Spider-man       owl:sameAs  person:Piter-Parker >>
		prov:wasDerivedFrom   ex:DCHerosIdentity ;
		prov:wasDerivedFrom   ex:MarvelHerosIdentity .
		
	<<hero:Iron-man         owl:sameAs  person:Tony-Stark>> 
		prov:wasDerivedFrom   ex:DCHerosIdentity ;
		prov:wasDerivedFrom   ex:MarvelHerosIdentity .
}
```

 





# </span> <div id='Difference'/>
## <br> <span style="color:purple"> 5.3 Difference </span>
<!------------------------------------------------------------->

```
-----------------
-- Example 5.1 --
-----------------
Greatest Comics Superheroes

ex:ComicsHeroesIdentity
    a                     voidPlus:LensUnion ;
    dcterms:description   "Quality Check: Identifying superheroes from both Marvel and DC comics" ;
    voidPlus:expression   "ex:DCHerosIdentity DIFFERENCE ex:MarvelHerosIdentity" ;
    void:target           ex:DCHerosIdentity , ex:MarvelHerosIdentity ;
    void:triples          4 ;
    • • •

ex:DCHerosIdentity
{
	<<hero:Superman         owl:sameAs  person:Clark-Kent>>          validation:status "True" .
	<<hero:Batman           owl:sameAs  person:Bruce-Wane>>          validation:status "True" .
	<<hero:Flash            owl:sameAs  person:Barry-Allen>>         validation:status "True" .
	<<hero:GreenLantern     owl:sameAs  person:Alan-Scott>>          validation:status "True" .
	<<hero:WonderWoman      owl:sameAs  person:Diana-Prince>>        validation:status "True" .
	<<hero:Aquaman          owl:sameAs  person:Arthur-Curry>>        validation:status "True" .
	<<hero:GreenArrow       owl:sameAs  person:OliverQueen>>         validation:status "True" .
	<<hero:BoosterGold      owl:sameAs  person:Michael-Jon-Carter>>  validation:status "True" .  
}
```








# </span> <div id='Composition'/>
## <br> <span style="color:purple"> 5.4 Composition </span>
<!------------------------------------------------------------->





# </span> <div id='InSet'/>
## <br> <span style="color:purple"> 5.5 In Set </span>
<!------------------------------------------------------------->
To learn on favourite superheroes, we create a linkset between the Marvel superheroes and IMDB. Only, the interest is not on any Marvel superheroes but instead, the interest lies only on those matched in the ex:MarvelHerosIdentity linkset. So, instead of matching Marvel's superheroes against IMDB resources and then filter the resulting links. We rather ran the Marvel's superheroes extracted from 


```
ex:MoviesRate
{
	movie:WonderWoman 
		schema:character        hero:WonderWoman;
		schema:contentRating   7.4.
		
	movie:WonderWoman-Bloodlines 
		schema:character        hero:Superman;
		schema:contentRating   5.8.
		
	movie:Superman 
		schema:character        hero:Superman;
		schema:contentRating   7.3.
		
	movie:Superman-Returns 
		schema:character        hero:Superman;
		schema:contentRating   6.
		
	movie:Man-of-Steel 
		schema:character        hero:Superman;
		schema:contentRating   7.
		
	movie:Batman 
		schema:character        hero:Batman;
		schema:contentRating   7.5.
	
	movie:Batman-Returns
		schema:character        hero:Batman;
		schema:contentRating   7.
		
	movie:Batman-Robin
		schema:character        hero:Batman;
		schema:contentRating   3.7.
		
	movie:Spider-man  
		schema:character        hero:Spider-man;
		schema:contentRating   7.3.
		
	movie:The-amazing-Spider-man  
		schema:character        hero:Spider-man;
		schema:contentRating   6.5.
		
	movie:Spider-man-home-coming 
		schema:character        hero:Spider-man;
		schema:contentRating   7.4.
}
```

```
ex:MovieCharacter
{
	movie:WonderWoman             schema:character  hero:WonderWoman .
	movie:WonderWoman-Bloodlines  schema:character  hero:Superman .
	movie:Superman                schema:character  hero:Superman .
	movie:Superman-Return         schema:character  hero:Superman .
	movie:Man-of-Steel            schema:character  hero:Superman .
	movie:Batman                  schema:character  hero:Batman .
	movie:Batman-Returns          schema:character  hero:Batman .
	movie:Batman-Robin            schema:character  hero:Batman .
	movie:Spider-man              schema:character  hero:Spider-man .
	movie:The-amazing-Spider-man  schema:character  hero:Spider-man .
	movie:Spider-man-home-coming  schema:character  hero:Spider-man .
}

-------------------------------------------------------------
-- Example 5.1: SET OF MATCHED RESOURCES (SOURCE & TARGET) --
-------------------------------------------------------------
Derived Marvel's matched universe set
{
	hero:Captain-Marvel,   person:Carol-Danvers,  hero:Captain-America,  person:Steve-Rogers,
	hero:Deadpool,         person:Wade-Wilson,    hero:Black-Panther,    person:T-Challa,
	hero:Spider-man,       person:Piter-Parker,   hero:Iron-man,          person:Tony-Stark,
	hero:Ant-man,          person:Tony-Stark,     hero:Black-Widow,       person:Natasha-Romanoff,
	hero:Hulk,             person:Bruce-Banner,   hero:Hawkeye,           person:Clint-Barton
}

---------------------------------------------------------------
-- Example 5.1: Movie Characters from ex:MovieCharacter that --
--      are derived from Marvel's matched universe set       --
---------------------------------------------------------------
ex:MovieCharacter
{
	movie:Spider-man              schema:character  hero:Spider-man .
	movie:The-amazing-Spider-man  schema:character  hero:Spider-man .
	movie:Spider-man-home-coming  schema:character  hero:Spider-man .
}

```

<!--{
    hero:Superman,     person:Clark-Kent,    hero:Batman,        person:Bruce-Wane,
    hero:Flash,        person:Barry-Allen,   hero:GreenLantern,  person:Alan-Scott, 
    hero:WonderWoman,  person:Diana-Prince,  hero:Aquaman,       person:Arthur-Curry, 
    hero:GreenArrow,   person:OliverQueen,   hero:BoosterGold,   person:Michael-Jon-Carter,
    hero:Spider-man,   person:Piter-Parker,  hero:Iron-man,      person:Tony-Stark   
}-->
 


<!----------------------------------------------------------->
# </span> <div id='Link-Validation'/>
# <br> <span style="color:purple"> 6. LINK VALIDATION </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!----------------------------------------------------------->
Imagine a researcher in the need of integrating data on publications, authors and education institutions. Wrongly executing this integration task could mean, for example, assigning the h-index of author A to author B or wrongly saying that author A is affiliated to an institution he has never been involved with. To reaching a solid investigation result, this highlights the crucial importance of link validation once links have been created and possibly improved.



## <br> <span style="color:purple"> Validation </span>
<!--------------------------------------------------->



## <br> <span style="color:purple"> Validation Support </span>
<!----------------------------------------------------------->

### <span style="color:purple"> Cluster-based validation </span>
### <span style="color:purple"> Vizualition </span>









<!------------------------------------------------------->
# </span> <div id='Link-Export'/>
# <br> <span style="color:purple"> 7. LINK EXPORT </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!------------------------------------------------------->

At this point, links have ben created and possibly improved. Now, interesting questions are:

* Could these links be exported for external usage? 
* In what format are there available for export? 
* What metadata can be exported in combination with the links?
* Can the linktype be modified prior to an export?

All these questions will be answered here. 



  
# </span> <div id='Export-Structure'/>
## <span style="color:purple"> 7.1 Export Structure </span>
<!---------------------------------------------------->
The **Lenticular Lens** design imposes to itself and motivates its users to provide as much documentation as possible for explaining why (understandability) and how (reproducibility) a set of links is generated. This metadata in the **Lenticular Lens** can be organised into **Generic** and **Specific** metadata. A *generic metadata* is the annotation that applies to a set of links as a whole while a *specific metadata* applies to individual links. 
Indeed, all links residing in the **Lenticular Lens** can be exported. However, prior to doing that, one has to choose whether the metadata is to be included or not and if it is to be included, should it include Generic and/or Specific metadata? 


<span style="color:blue">**Identity Set in the Default Graph.**</span> In the Example-1, using the turtle RDF syntax, we present a standard identity linkset where equivalent resources are linked with the well known linktype owl:sameAs. 

```language-turtle
---------------
-- Example-1 --
---------------
Linkset in the default graph.
	
	hero:BlackWidow  owl:sameAs	  person:Nat .
	hero:BlackWidow  owl:sameAs	  person:Romanoff .
	hero:BlackWidow  owl:sameAs	  person:Natalia-Romanova .
	hero:BlackWidow  owl:sameAs	  person:Natasha .
	hero:Spiderman   owl:sameAs	  person:Peter-parker  .
	hero:Spiderman   owl:sameAs	  person:Tom-Holland .
	hero:Superman    owl:sameAs	  person:Clark-Kent .
	hero:Superman    owl:sameAs	  person:Joseph .
	hero:Superman    owl:sameAs	  person:Kal-El .
	
```
<br>


<span style="color:blue">**Identity Set in a Named Graph.**</span> In Example-2, the set of links illustrated in Example-1 as triples populating the default graph can now be referred to as the graph with IRI ex:herosIdentity. This IRI can now be used to document any generic information deemed relevant such as the source and target datasets, the aligning method... 

```
---------------
-- Example-2 --
---------------
Linkset in a named graph syntax.
	
ex:herosIdentity
{
	hero:BlackWidow  owl:sameAs	  person:Nat .
	hero:BlackWidow  owl:sameAs	  person:Romanoff .
	hero:BlackWidow  owl:sameAs	  person:Natalia-Romanova .
	hero:BlackWidow  owl:sameAs	  person:Natasha .
	hero:Spiderman   owl:sameAs	  person:Peter-parker  .
	hero:Spiderman   owl:sameAs	  person:Tom-Holland .
	hero:Superman    owl:sameAs	  person:Clark-Kent .
	hero:Superman    owl:sameAs	  person:Joseph .
	hero:Superman    owl:sameAs	  person:Kal-El .
}
```
<br>


Example-3 illustrates the complete structure of linksets and lenses in the **Lenticular Lens**. Here, by default, a linkset/lens is annotated with both, generic and specific metadata. <br>
<span style="color:blue"> **Generic Metadata.** </span> As shown in Example-3, the generic annotation associated with the superheroes identity linkset is composed of 14 triples, which are all element of the default graph (triple without a specific named graph). Among others, these triples convey information such as the type, subjects, license, description, format, number of triples, number of distinct entities, number of identity clusters... of the set. 
<span style="color:blue"> **Specific Metadata.** </span> This type of metadata remains in the linkset's graph (applicable to a lens). It enable the reification of specific triples. One can for example provide the confidence strength of each of linkset's statement. As illustrated in Example-3, the `hero:Spiderman   owl:sameAs   person:Tom-Holland` is annotated as a non valid statement followed by the rational supporting its rejection. Such annotation enable the selection of specific triples. For example, on can select the 8 validated triples or the 7 triples validated as correct. <br>
<span style="color:blue"> **Separation of Concern.** </span> The linkset and lens presentation enable separation of concern in the sense that it provides the user with a number of options: **Flat Representation:** non reified triples optionally within a named graph; **Partial Representation:** the choice of exclusively including only the generic or the specific metadata; **Full Representation:** as intended in the **Lenticular Lens**, the linkset comes along with its generic and specific metadata if applicable. 

```
---------------
-- Example-3 --
---------------
Default RDF* turtle syntax annotation structure of a linkset in the the Lenticular Lens.
	
ex:heroesIdentity
	a                     void:Linkset ;
	dcterms:description   "Identifying Marvel's superheroes" ;
	dcterms:license       law:odc-public-domain-dedication-and-licence ;
	dcterms:subject       <http://example.org/resource/Person> ;
	dcterms:subject       <http://example.org/resource/Hero> ;
	void:subjectsTarget   dataset:Fictive-Persons ;
	void:objectsTarget    dataset:Superheroes ;
	void:feature          format:Turtle ;
	void:linkPredicate    owl:sameAs ;
	void:triples           9 ;
	void:entities         12 ;
	void:distinctSubjects  3 ;
	void:distinctObjects   9 ;
	voidPlus:clusters      3 ;
	validation:count       8 ;
	validation:accepted    7 ;
	validation:rejected    1 ;
	validation:remains     1 ;
	
ex:heroesIdentity
{
	<<hero:BlackWidow owl:sameAs person:Nat>>          validation:status "True" .
	<<hero:BlackWidow owl:sameAs person:Romanoff>>     validation:status "True" .
	<<hero:BlackWidow owl:sameAs person:Natalia-Romanova>> 
		validation:status "True" . 
	<<hero:BlackWidow owl:sameAs person:Natasha>>      validation:status "True" .
	<<hero:Spiderman  owl:sameAs person:Peter-parker>> validation:status "True" .
	<<hero:Spiderman  owl:sameAs person:Tom-Holland>>  
		validation:status     "False" .
		validation:Rational   "Tom-Holland does not have Spiderman properties 
		                       which Peter-parker (fictitious) a.k.a Spiderman has." .
	<<hero:Superman   owl:sameAs person:Clark-Kent>>   validation:status "True" .
	<<hero:Superman   owl:sameAs person:Joseph>>       validation:status "True" .
	hero:Superman   owl:sameAs person:Kal-El .
}
```
<br>



# </span> <div id='Export-Restrictions'/>
## <span style="color:purple"> 7.2 Export Restrictions </span>
<!----------------------------------------------------------->
As addressed in the previous section, link annotation provides the user with export options as described below.

```
• All           : Export all links
• Accepted      : Export only accepted links.
• Rejected      : Export only rejected links.
• Validated     : Export rejected or validated links
• Not Validated : Export links with no accepted or rejected annotation.
• Threshold     : Export links that pass a predefined threshold condition. 
                  This feature applies to links annotated with confidence values.
```



# </span> <div id='Export-Formats'/>
## <span style="color:purple"> 7.3 Export Formats </span>
<!------------------------------------------------------>
Indeed, all links residing in the **Lenticular Lens** can be exported. For that, one is provided with three syntax options: **CSV** (Example-4), **JSON-LD** (Example-5), **RDF Turtle** (Example-6), and **RDF* Turtle** (Example-3).

<span style="color:blue"> **CSV OUTPUT.** </span> In our attend to export a linkset/lens with its complete metadata, in a CSV format, the **Lenticular Lens** generates two CSV tables. As available in Example-4, the first table is an illustration of the metadata table while the second table is an illustration of the superheroes identity linkset.

```
---------------
-- Example-4 --
---------------
Linkset in a CSV format. 
Keep in mind that the table below are a visual representation of a CSV table

--------------------
-- METADATA TABLE --
--------------------

---------------------------------------------------------------------------------------------------------  
| Vocabulary                                                  Value                                     |
---------------------------------------------------------------------------------------------------------                                                
  http://www.w3.org/ns/sparql-service-description#namedGraph  http://example.org/#herosIdentity
  http://www.w3.org/1999/02/22-rdf-syntax-ns#type             http://rdfs.org/ns/void#Linkset
  http://purl.org/dc/terms/description                        Identifying Marvel's superheroes
  http://purl.org/dc/terms/license                            law:odc-public-domain-dedication-and-licence
  http://purl.org/dc/terms/subject                            http://example.org/resource/Person
  http://purl.org/dc/terms/subject                            http://example.org/resource/Hero
  http://rdfs.org/ns/void#subjectsTarget                      dataset:Fictive-Persons
  http://rdfs.org/ns/void#objectsTarget                       dataset:Superheroes
  http://rdfs.org/ns/void#feature                             format:Turtle
  http://rdfs.org/ns/void#linkPredicate                       owl:sameAs
  http://rdfs.org/ns/void#triples                             9
  http://rdfs.org/ns/void#entities                            12
  http://rdfs.org/ns/void#distinctSubjects                    3
  http://rdfs.org/ns/void#distinctObjects                     9
  http://vocabulary/voidPlus#clusters                         3
  http://vocabulary/validation#count                          8
  http://vocabulary/validation#accepted                       7
  http://vocabulary/validation#rejected                       1
  http://vocabulary/validation#remains                        1

------------------------
-- LINKSET/LENS TABLE --
------------------------

------------------------------------------------------------------------------------------------------------------------------------------------
| NamedGraph                         Source                              Target                                      ValStatus  ValRational    |
------------------------------------------------------------------------------------------------------------------------------------------------
  http://example.org/#herosIdentity  http://example.org/hero#BlackWidow  http://example.org/person#Nat               True         
  http://example.org/#herosIdentity  http://example.org/hero#BlackWidow  http://example.org/person#Romanoff          True
  http://example.org/#herosIdentity  http://example.org/hero#BlackWidow  http://example.org/person#Natalia-Romanova  True
  http://example.org/#herosIdentity  http://example.org/hero#BlackWidow  http://example.org/person#Natasha           True
  http://example.org/#herosIdentity  http://example.org/hero#Spiderman   http://example.org/person#Peter-parker      True
  http://example.org/#herosIdentity  http://example.org/hero#Spiderman   http://example.org/person#Tom-Holland       False      Tom-Holland does not have Spiderman properties which Peter-parker (fictitious) a.k.a Spiderman has.
  http://example.org/#herosIdentity  http://example.org/hero#Superman    http://example.org/person#Clark-Kent        True
  http://example.org/#herosIdentity  http://example.org/hero#Superman    http://example.org/person#Joseph            True
  http://example.org/#herosIdentity  http://example.org/hero#Superman    http://example.org/person#Kal-El            True


```
<br>

<span style="color:blue"> **JSON-LD  OUTPUT.** </span>TODO....

```json-ld
---------------
-- Example-5 --
---------------
Linkset in a JSON-LD format.

{
  "@context": 
  {
    "name": "http://xmlns.com/foaf/0.1/name",
    "homepage": 
    {
      "@id": "http://xmlns.com/foaf/0.1/workplaceHomepage",
      "@type": "@id"
    },
    "Person": "http://xmlns.com/foaf/0.1/Person"
  },
  
  "@id": "https://me.example.com",
  "@type": "Person",
  "name": "John Smith",
  "homepage": "https://www.example.com/"
}
``` 
<br>


<span style="color:blue"> **RDF TURTLE  OUTPUT.** </span> Our preference goes to an RDF* Turtle Output as illustrated in Example-3. However, because RDF* is not deployed on all triple stores, we provide the singleton representation alternative as well. An example of this representation in available in Example-6.

```
---------------
-- Example-6 --
---------------
Default RDF turtle syntax annotation structure of a linkset in the the Lenticular Lens.
Linkset in an RDF Turtle format using singletons.
	
ex:heroesIdentity
	a                     void:Linkset ;
	dcterms:description   "Identifying Marvel's heros" ;
	dcterms:license       law:odc-public-domain-dedication-and-licence ;
	dcterms:subject       <http://example.org/resource/Person> ;
	dcterms:subject       <http://example.org/resource/Hero> ;
	void:subjectsTarget   dataset:Fictive-Persons ;
	void:objectsTarget    dataset:Superheroes ;
	void:feature          format:Turtle ;
	void:linkPredicate    owl:sameAs ;
	void:triples           9 ;
	void:entities         12 ;
	void:distinctSubjects  3 ;
	void:distinctObjects   9 ;
	voidPlus:clusters      3 ;
	validation:count       8 ;
	validation:accepted    7 ;
	validation:rejected    1 ;
	validation:remains     1 ;
	
ex:heroesIdentity
{
	hero:BlackWidow  singleton:sameAs-1   person:Nat .
	hero:BlackWidow  singleton:sameAs-2	  person:Romanoff .
	hero:BlackWidow  singleton:sameAs-3	  person:Natalia-Romanova .
	hero:BlackWidow  singleton:sameAs-4	  person:Natasha .
	hero:Spiderman   singleton:sameAs-5	  person:Peter-parker  .
	hero:Spiderman   singleton:sameAs-6	  person:Tom-Holland .
	hero:Superman    singleton:sameAs-7	  person:Clark-Kent .
	hero:Superman    singleton:sameAs-8	  person:Joseph .
	hero:Superman    singleton:sameAs-9	  person:Kal-El .
}
```
<br>

# </span> <div id='Default-Export-Table'/>
## <span style="color:purple"> 7.4 Default Export Table </span>
<!--------------------------------------------------------->
Example-7 summarises the various options for exporting a linkset or lens. In each set of selection category, a default selection is checked in. This means that, by default, an exported linkset or lens comes along with **all its links** and **its complete annotation** in a **CSV format**. 


```
---------------
-- Example-7 --
---------------
	----------------------------------------------------------------
	| RESTRICTIONS        STRUCTURE               FORMAT           |
	----------------------------------------------------------------
	  [x] All             [x] Complete            [x] CSV                                  
	  [ ] Accepted        [ ] Partial:Generic     [ ] JSON-LD                    
	  [ ] Rejected        [ ] Partial:Specific    [ ] RDF-TURTLE              
	  [ ] Validated                               [ ] RDF*-TURTLE 
	  [ ] Not Validated                                           
	  [ ] Threshold                                                                                      
```



<!----------------------------------------------------------->
# </span> <div id='Data-Integration'/>
# <br> <span style="color:purple"> 8. DATA INTEGRATION </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!----------------------------------------------------------->
The Lenticular Lens is **a mean** (link creation, manipulation and validation for data integration) to **an end** (data extraction for analysis). Here, we show **how one can extract the right information for analysis** given an integration model that can be achieve using existing linksets and lenses.  




# </span> <div id='Integration-Model'/>
## <span style="color:purple"> 8.1 Integration Model </span>
<!----------------------------------------------------------->



# </span> <div id='Data-Extraction'/>
## <span style="color:purple"> 8.2 Data Extraction </span>
<!----------------------------------------------------------->





<!--------------------------------------------------------->
# </span> <div id='Installation'/>
# <br> <span style="color:purple">  9. INSTALLATION </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!--------------------------------------------------------->

To install a local version of the Lenticular Lens, follow the installation steps described below.
 
1. Make sure `Docker` and `Docker Compose` are installe
 * For `Windows` and `Mac users`: install [Docker Desktop](https://www.docker.com/products/docker-desktop). 
2.  Use the provided `docker-compose.yml` as a baseline.
3.  Run `docker-compose`
4. Visit http://localhost:8000 in your browser

**Note**: <br> This will create a folder pgdata with the database data. 
<br> To clean up the database and start from scratch, simply remove this folder.



# </span> <div id='API'/>
# <br> <span style="color:purple">  10. API </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)
<!--------------------------------------------------------->

Through Github, the **[Lenticular Lens API](https://github.com/knaw-huc/lenticular-lenses#api)** is made available with a set of functions and procedures allowing for the code to be reused and/or extended .




# <br> <span style="color:purple"> REFERENCES </span> (<span style="font-size:1.7vw">[TOC](#CONTENTS)</span>)

* **<span style="color:purple"> [Euzenat] </span>** J. Euzenat and P. Shvaiko. Ontology matching. Springer-Verlag, Heidelberg (DE), 2nd edition, 2013.

* **<span style="color:purple"> [LINKED-DATA] </span>** T. Berners-Lee. Linked Data – Design issues. 27 July 2006. URL: https://www.w3.org/DesignIssues/LinkedData.html <br>

* **<span style="color:purple"> [RDF11-CONCEPTS] </span>**  Richard Cyganiak, David Wood, Markus Lanthaler. RDF 1.1 Concepts and Abstract Syntax. W3C Recommendation, 25 February 2014. URL: http://www.w3.org/TR/2014/REC-rdf11-concepts-20140225/. The latest edition is available at http://www.w3.org/TR/rdf11-concepts/ <br>

* **<span style="color:purple"> [RFC2141] </span>** R. Moats. URN Syntax. May 1997. RFC. URL: http://www.ietf.org/rfc/rfc2141.txt <br>

* **<span style="color:purple"> [RFC3305] </span>** M. Mealling; R. Denenberg. Report from the Joint W3C/IETF URI Planning Interest Group: Uniform Resource Identifiers (URIs), URLs, and Uniform Resource Names (URNs): Clarifications and Recommendations. August 2002. RFC. URL: http://www.ietf.org/rfc/rfc3305.txt

* **<span style="color:purple"> [RFC3986] </span>** T. Berners-Lee; R. Fielding; L. Masinter. Uniform Resource Identifier (URI): Generic Syntax. January 2005. RFC. URL: http://www.ietf.org/rfc/rfc3986.txt

* **<span style="color:purple"> [RFC3987] </span>** M. Dürst; M. Suignard. Internationalized Resource Identifiers (IRIs). January 2005. RFC. URL: http://www.ietf.org/rfc/rfc3987.txt

* **<span style="color:purple"> [VoID] </span>**  K. Alexander, R. Cyganiak, M. Hausenblas, and J. Zhao. Describing LinkedDatasets with the VoID Vocabulary.  Technical report, 2011.  W3C Note. URL:https://www.w3.org/TR/void/. <br>




<!--
Research Select Construct Manipulate Validate Export
<div align="center"> </div>
<sub>![](LL_PlusButton.jpg)</sub> 
<span style="color:blue">•••</span>
-->
