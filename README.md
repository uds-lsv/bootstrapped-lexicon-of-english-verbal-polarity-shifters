# Towards Bootstrapping a Polarity Shifter Lexicon using Linguistic Features
This repository contains the data created as part of:

[Schulder, Marc](http://marc.schulder.info) and [Wiegand, Michael](http://www.coli.uni-saarland.de/~miwieg/) and [Ruppenhofer, Josef](http://ruppenhofer.de/) and [Roth, Benjamin](https://sites.google.com/site/rothbenj/) (2017). **"Towards Bootstrapping a Polarity Shifter Lexicon using Linguistic Features"**. Proceedings of the 8th International Joint Conference on Natural Language Processing (IJCNLP). Taipei, Taiwan, November 27 - December 30, 2017.

[PDF](http://aclweb.org/anthology/I17-1063)

## Content
The supplementary data of this paper consists of:
1. Two lists of WordNet verbs (Miller et al., 1990), annotated for whether they cause shifting.
    1. The initial gold standard (§2) of 2000 randomly chosen verbs.
    2. The bootstrapped 1043 verbs (§5.3) that were labelled as shifters by our best classifier and then manually annotated.
2. Data set of verb phrases from the Amazon Product Review Data corpus (Jindal & Liu, 2008), annotated for polarity of phrase and polar noun.


## Verbal Shifters
### Files
  - The initial gold standard: `verbal_shifters.gold_standard.txt`
  - The bootstrapped verbs: `verbal_shifters.bootstrapping.txt`

### Format
- Each line contains a verb and its label, separate by a whitespace.
- Multiword expressions are separated by an underscore (WORD_WORD).
- All labels were assigned by an expert annotator.

## Sentiment Verb Phrases
### Files
- All annotated verb phrases: `sentiment_phrases.txt`

### Content
The file starts with 400 phrases containing shifter verbs, followed by 2231 phrases containing non-shifter verbs.
### Format
Every item consists of:
- The sentence from which the VP and the polar noun were extracted.
- The VP, polar noun and the verb heading the VP.
- Constituency parse for the VP.
- Gold labels for VP and polar noun by a human annotator.
- Predicted labels for VP and polar noun by RNTN tagger (Socher et al., 2013) and `LEX_gold` approach.
- Items are separated by a line of asterisks (*)

## BibTex
```
@inproceedings{schulder2017shifter,
  title={Towards Bootstrapping a Polarity Shifter Lexicon using Linguistic Features},
  author={Schulder, Marc and Wiegand, Michael and Ruppenhofer, Josef and Roth, Benjamin},
  booktitle={Proceedings of the Eighth International Joint Conference on Natural Language Processing},
  year={2017},
  publisher={Asian Federation of Natural Language Processing},
  volume={1},
  pages={624--633},
  location={Taipei, Taiwan},
  url={http://aclweb.org/anthology/I17-1063}
}
```

## References
G. Miller, R. Beckwith, C. Fellbaum, D. Gross, K. Miller: "Introduction to WordNet: An On-Line Lexical Database". International Journal of Lexicography, 3:235-244, 1990.

N. Jindal and B. Liu: "Opinion Spam and Analysis", in Proceedings of ACM-WSDM, 2008.

R. Socher, A. Perelygin, J. Wu, J. Chuang, C. Manning, A. Ng, C. Potts: "Recursive Deep Models for Semantic Compositionality Over a Sentiment Treebank", in EMNLP, 2013.
