# Summary

Publicly available subset of the IAHLT UD Hebrew Treebank's Wikipedia section (https://www.iahlt.org/)

# Introduction

The UD Hebrew-IAHLTWiki treebank consists of 5,000 contemporary Hebrew sentences representing a variety of texts originating from Wikipedia entries, compiled by the [Israeli Association of Human Language Technology](https://www.iahlt.org/). It includes various text domains, such as: biography, law, finance, health, places, events and miscellaneous. The schema for the UD Hebrew-IAHLT treebank, from which the publicly available UD Hebrew-IAHLTWiki subset is derived, is based on the conversion of the Hebrew Treebank (HTB) into the latest UD V2 and is checked against the Universal Dependencies validator as of UD release V2.10, in addition to a range of additional validations using the grewv tool.

## Compatible datasets

The HTB version used in the project was initially converted automatically, then a subset of the converted data was manually validated and adopted as a gold standard for training the model for UD parsing used in Hebrew-IAHLT. The entire parsed data has been manually edited to correct parsing errors, and was automatically QA'ed to apply corrections following updates in the schema. For a fork of UD_Hebrew-HTB (Ha'aretz newswire data) using the same annotation scheme, see:

https://github.com/IAHLT/UD_Hebrew

For an additional UD_Hebrew corpus with the same annotation scheme (spoken parliament proceedings), see:

https://github.com/UniversalDependencies/UD_Hebrew-IAHLTknesset

## NER annotations

The data additionally contains *nested* Named Entity annotations in the IAHLT scheme in the MISC annotation `Entity=`, illustrated in the following excerpt:

```CoNLL-U
# sent_id = iahltwiki_piskat-hitgabrut-27
# text = ההצעה תאמה את עמדתו של נשיא בית המשפט העליון אהרן ברק, היא נדונה בוועדת חוקה חוק ומשפט של הכנסת אך לא קודמה.
1-2	ההצעה	_	_	_	_	_	_	_	_
1	ה	ה	DET	DET	Definite=Def|PronType=Art	2	det	_	_
2	הצעה	הצעה	NOUN	NOUN	Gender=Fem|Number=Sing	3	nsubj	_	_
3	תאמה	תאם	VERB	VERB	Gender=Fem|HebBinyan=PAAL|Number=Sing|Person=3|Tense=Past|Voice=Act	0	root	_	_
4	את	את	ADP	ADP	_	5	case	_	_
5-6	עמדתו	_	_	_	_	_	_	_	_
5	עמדת	עמדה	NOUN	NOUN	Gender=Fem|Number=Sing	3	obj	_	_
6	ו	הוא	PRON	PRON	Case=Gen|Definite=Def|Gender=Masc|Number=Sing|Person=3|Poss=Yes|PronType=Prs	5	nmod:poss	_	_
7	של	של	ADP	ADP	Case=Gen	8	case	_	_
8	נשיא	נשיא	NOUN	NOUN	Definite=Cons|Gender=Masc|Number=Sing	5	nmod:poss	_	Entity=(TTL
9	בית	בית	NOUN	NOUN	Definite=Cons|Gender=Masc|Number=Sing	8	compound	_	Entity=(ORG
10-11	המשפט	_	_	_	_	_	_	_	_
10	ה	ה	DET	DET	Definite=Def|PronType=Art	11	det	_	_
11	משפט	משפט	NOUN	NOUN	Gender=Masc|Number=Sing	9	compound	_	_
12-13	העליון	_	_	_	_	_	_	_	_
12	ה	ה	DET	DET	Definite=Def|PronType=Art	13	det	_	_
13	עליון	עליון	ADJ	ADJ	Gender=Masc|Number=Sing	9	amod	_	Entity=ORG)TTL)
14	אהרן	אהרן	PROPN	PROPN	_	8	appos	_	Entity=(PER
15	ברק	ברק	PROPN	PROPN	_	14	flat	_	Entity=PER)|SpaceAfter=No
```

Entity types cover the following categories:

  * ANG - language 
  * DUC - product 
  * EVE - event 
  * FAC - facility 
  * GPE - geo-political entity 
  * LOC - location 
  * ORG - organization 
  * PER - person 
  * TIMEX - time expression 
  * TTL - title
  * WOA - work of art 
  * MISC - miscellaneous 

# Acknowledgments

We would like to thank all the people who contributed to this corpus: Amir Zeldes, Hilla Merhav, Israel Landau, Netanel Dahan, Nick Howell, Noam Ordan, Omer Strass, Shira Wigderson, Yael Minerbi, Yifat Ben Moshe

## References

To cite this dataset please refer to the following paper:

Zeldes, Amir, Nick Howell, Noam Ordan and Yifat Ben Moshe (2022) [A Second Wave of UD Hebrew Treebanking and Cross-Domain Parsing](https://arxiv.org/abs/2210.07873). In: *Proceedings of EMNLP 2022*. Abu Dhabi, UAE, 4331-4344.

```bibtex
@InProceedings{ZeldesHowellOrdanBenMoshe2022,
  author    = {Amir Zeldes and Nick Howell and Noam Ordan and Yifat Ben Moshe},
  booktitle = {Proceedings of {EMNLP} 2022},
  title     = {A Second Wave of {UD} {H}ebrew Treebanking and Cross-Domain Parsing},
  year      = {2022},
  pages     = {4331--4344},
  address   = {Abu Dhabi, UAE},
  url       = {https://aclanthology.org/2022.emnlp-main.292/},
}
```


# Changelog

* 2024-11-15 v2.15
  * Construction annotations in the [UCxn](https://github.com/LeonieWeissweiler/UCxn) framework added to MISC
     * This release adds rule-based annotations of Interrogatives, Conditionals, Existentials, and NPN (noun-preposition-noun) constructions on the head of the respective phrase, plus construction elements.
     * The UCxn v1 notation and categories are documented [here](https://github.com/LeonieWeissweiler/UCxn/blob/main/docs/UCxn-v1.pdf).

* 2024-11-15 v2.15
  * Added nested NER
  * FEATS consistency changes with other Hebrew treebanks
  * Changed :tmod and :npmod subtypes to :unmarked with TemporalNPAdjunct=Yes in misc to preserve tmod info

* 2022-05-15 v2.10
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.10
License: CC BY-SA 4.0
Includes text: yes
Parallel: no
Genre: wiki
Lemmas: manual native
UPOS: manual native
XPOS: not available
Features: manual native
Relations: manual native
Contributors: Zeldes, Amir; Algom, Avner; Ordan, Noam; Ben Moshe, Yifat; Wigderson, Shira
Contributing: here
Contact: amir.zeldes@georgetown.edu
===============================================================================
</pre>
