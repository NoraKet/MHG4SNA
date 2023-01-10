# MHG4SNA
>Annotations on middle high german texts for social network analysis

This corpus contains multiple middle high german texts with annotations for social network analysis. 
It contains annotations of: named entities and entity mentions (including partial coreference resolution), direct speech, narrator's comments. See below for further description.
The annotated texts are: 'Parzival' by Wolfram von Eschenbach, 'Erec' by Hartmann von Aue, 'Iwein' by Hartmann von Aue, 'Willehalm' by Wolfram von Eschenbach, and 'Rolandslied' by Pfaffe Konrad.

The annotated texts are part of my dissertation on social network analysis of arthurian romances. The research was developed in the context of the DH center CRETA at the university of Stuttgart.

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

The annotations follow the guidelines created for multiple categories and disciplines in the context of CRETA. They are published here: LINK 

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

tbc

# Data downloads

The annotated texts can be downloaded in multiple formats: conll, csv, and gexf.

>Conll contains seven columns:

(1) token

(2) POS-tag, tagged using a middle high german pos tagger [LINK]

(3) number of segment

(4) Entity reference annotation indicating the intance that the entity reference refers to. '-' if there is no entity reference.

(5) EK: '1' in case there is an annotation of 'EK', '0' if not.

(6) EK2: '1' in case there is an annotation of 'EK2', '0' if not.

(7) DS: '1' if the token is tagged as direct speech, '0' if not.

>Csv

>Gexf

tbc
