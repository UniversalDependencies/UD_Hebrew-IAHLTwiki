# Summary

Publicly available subset of the IAHLT UD Hebrew Treebank's Wikipedia section (https://www.iahlt.org/)

# Introduction

The UD Hebrew-IAHLTWiki treebank consists of 5,000 contemporary Hebrew sentences representing a variety of texts originating from Wikipedia entries. It includes various text domains, such as: biography, law, finance, health, places, events and miscellaneous. The schema for the UD Hebrew-IAHLT treebank, from which the publicly available UD Hebrew-IAHLTWiki subset is derived, is based on the conversion of the Hebrew Treebank (HTB) into the latest UD V2 and is checked against the Universal Dependencies validator as of UD release V2.10, inaddition to a range of additional validations using the grewv tool.

The HTB version used in the project was initially converted automatically, then a subset of the converted data was manually validated and adopted as a gold standard for training the model for UD parsing used in Hebrew-IAHLT. The entire parsed data has been manually edited to correct parsing errors, and was automatically QA'ed to apply corrections following updates in the schema. 

# Acknowledgments

We would like to thank all the people who contributed to this corpus: Amir Zeldes, Hilla Merhav, Israel Landau, Netnael Dahan, Nick Howell, Noam Ordan, Omer Strass, Shira Wigderson, Yael Minerbi, Yifat Ben Moshe

## References

An academic paper describing this resource is pending, for the time being please use the repository URL to cite this dataset.


# Changelog

* 2022-05-15 v2.10
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.10
License: CC BY-SA 4.0
Includes text: yes
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
