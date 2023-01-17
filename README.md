# MHG4SNA
>Annotations on middle high german texts for social network analysis

This corpus contains multiple middle high german texts with annotations for social network analysis. 
It contains annotations of: named entities and entity mentions (including partial coreference resolution), direct speech, narrator's comments. See below for further description.
The annotated texts are: 'Parzival' by Wolfram von Eschenbach, 'Erec' by Hartmann von Aue, 'Iwein' by Hartmann von Aue, 'Willehalm' by Wolfram von Eschenbach, and 'Rolandslied' by Pfaffe Konrad.

The annotated texts are part of my dissertation on social network analysis of arthurian romances. The research was developed in the context of the DH center CRETA at the university of Stuttgart. [1]

# Texts
Wolfram von Eschenbach: 'Parzival', in: Wolfram von Eschenbach: Werke, ed. by Karl Lachmann, 5th edition, Berlin 1891, pp. 11–388.

Hartmann von Aue: 'Erec', ed. by Albert Leitzmann continued by Ludwig Wolff, 7th edition by Kurt Gärtner, Tübingen 2006 (Altdeutsche Textbibliothek 39).

Hartmann von Aue: 'Iwein', ed. by G. F. Benecke and K. Lachmann, revised by Ludwig Wolff, 7th edition, part 1: Text, Berlin 1968.

Wolfram von Eschenbach: 'Willehalm', in: Wolfram von Eschenbach: Werke, ed. by Karl Lachmann, 5th edition, Berlin 1891, pp. 421–640.

'Das Rolandslied des Pfaffen Konrad', ed. by Carl Wesle, 3rd edition by Peter Wapnewski, Tübingen 1985 (Altdeutsche Textbibliothek 69).

All texts are digitally available in the MHDBDB (Mittelhochdeutsche Begriffsdatenbank), http://mhdbdb.sbg.ac.at/.

# Annotations

The texts contain annotations of different categories, as described in the following sections.

>Named Entities and Entity Mentions

I annotated all namend entities and entity mentions that belong to the categories PER and LOC.
PER stands for 'person' and refers to real persons as well as fictional characters. 
LOC stands for 'location' and includes real and fictional places.

I annotated named entities (e.g. 'Parzival' as PER or 'Nantes' as LOC) as well as entity mentions referring to an instance of PER or LOC (e.g. 'the knight' for Parzival, or 'the city' for Nantes). I did not annotate pronouns.
Entity references can contain multiple words, e.g. 'the lovely queen Ginover', and they can be nested, e.g. '[the son of [the king Gahmuret]]'.

The annotations follow the guidelines created for multiple categories and disciplines in the context of CRETA. They are published here: LINK. [2]

>Entity Grounding

All annotated entity references are mapped to the entity instance that they refer to. 
E.g. the refences 'Parzival', 'Herzeloyde's son', 'the young man', 'the red knight' etc. all refer to the character instance 'Parzival'.
The entity grounding takes into consideration the context of the entity mentions since one and the same expression can refer to different instances (in one context 'the king' refers to Arthur, in another context to Gahmuret).

>Direct Speech (DS)

Passages of direct speech have been annotated by detecting quotation marks. They are tagged as 'DS'.
There are a few cases of embedded direct speech (passages of direct speech containing another passage of direct speech); these cases are annotated as well.

>Narrator's comments (EK)

As additional category I annotated passages that contain statements of the narrator, narrator's comments, extensive descriptions or digressions (e.g. an excursus to a specific topic). These passages are not part of the fictional world or lead to a pause in the timeline of events. The are annotated as 'EK' ('EK': passages that aren't part of the diegesis, 'EK2': passages that lead to a pause, e.g. comments or descriptions).

>Segmentation

The texts are subdivided in passages of 30 verses. Since some text's editions ('Parzival', 'Willehalm') contain a formal segmentation in passages of 30 verses each, the same kind of segmentation has been transfered to the other texts. This means 'segment 1' contains the first 30 verses, 'segment 2' contains verses 31-60 and so on.

According to the editions by Lachmann, 'Parzival' and 'Willehalm' are also subdivided in chapter-like books (Parzival: book 1 to 16, Willehalm: book 1 to 9). The other texts are similarly subdivided in chapter-like sections following common content-based divisions.

# Social Network Analysis

The data can be used to explore and analyse the social network of the texts. SNA can be performed via gephi [4] using the gefx files.

The social network is based on co-occurrences using a) the annotated and grounded entities, and b) the text segmentation in segments of 30 verses each. A relation between two or more entities is extracted whenever they co-occur in a segment. 

# Data downloads

The annotated texts can be downloaded in multiple formats: conll, csv, and gexf.

>Conll contains seven columns:

(1) token

(2) POS-tag, tagged using a middle high german pos tagger [3]

(3) number of segment

(4) Entity reference annotation indicating the intance that the entity reference refers to. '-' if there is no entity reference.

(5) EK: '1' in case there is an annotation of 'EK', '0' if not.

(6) EK2: '1' in case there is an annotation of 'EK2', '0' if not.

(7) DS: '1' if the token is tagged as direct speech, '0' if not.

>Csv 

The csv file contains all annotations of the category PER including entity grounding. 

The file contains the following columns: begin and end (start and end of the entity reference expression, character offset), doc_id (document id), buch (book number), quote (entity reference expression), coref (the entity instance that the expression refers to), overlap (indicates if there is an overlap, relevant for embedded entities), ek and ek2 (narrator's comment), ds (direct speech), space (annotations of the space where the story takes action, can be ignored here), segnr (number of segment), em (embedded), klasse (entity class), xrange (technical, relevant for annotation view).

>Gexf

This file can be used to import the data to gephi. It is based on the annotation and grounding of entities (categorie PER). A relation between entities is based on co-occurrence (whenever two or more entities co-occur in a segment, they have a relation; with more relations, the intensitiy of their relation grows). The text segmentation is described above.

Embedded entities are excluded. Entities mentioned in direct speech (DS) or in comments (EK) can optionally be selected or deselected.
These optional filters are indicated in the name of the files.

To visualize the graph dynamically, one can use the text segmentation as timeline. 

# References

[1] https://www.creta.uni-stuttgart.de/, the project was funded by BMBF.

[2] for more information cf. Nora Ketschik, Maximilian Overbeck, Sandra Murr, Axel Pichler, André Blessing (2020). "Interdisziplinäre Annotation von Entitätenreferenzen." Reflektierte algorithmische Textanalyse. Interdisziplinäre(s) Arbeiten in der CRETA-Werkstatt, ed. by Nils Reiter, Axel Pichler and Jonas Kuhn, pp. 203-263.

[3] Nora Echelmeyer, Nils Reiter, Sarah Schulz (2017). "Ein PoS-Tagger für 'das' Mittelhochdeutsche." Dhd 2017 Konferenzabstracts, pp. 141-147. An online version can be used here: http://clarin05.ims.uni-stuttgart.de/mhdtt/index.html; the mhg model can be downloaded here: https://www.ims.uni-stuttgart.de/forschung/ressourcen/werkzeuge/pos-tag-mhg/.

[4] https://gephi.org/, M. Bastian, S. Heymann, M. Jacomy (2009). "Gephi: an open source software for exploring and manipulating networks." International AAAI Conference on Weblogs and Social Media.

# How to cite?

Please cite the zenodo publication linked to this github repository: https://doi.org/10.5281/zenodo.7544005
