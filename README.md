# STS.news.sr - The Serbian Semantic Textual Similarity News Corpus
The Serbian STS News Corpus consists of 1192 pairs of sentences in Serbian gathered from news sources on the web.
Each sentence pair was manually annotated with fine-grained semantic similarity scores on the 0-5 scale.
The final scores were obtained by averaging the scores of five annotators.

## Corpus creation
The sentence pairs in this dataset were taken from the [Serbian Paraphrase Corpus](https://vukbatanovic.github.io/paraphrase.sr/) (*paraphrase.sr*).
Details on the construction of that corpus can be found on the *paraphrase.sr* repository and in the papers listed in its reference section.

Typographical errors within the 1194 sentence pairs of the Serbian Paraphrase Corpus were manually corrected.
Any missing diacritical marks were restored as well.
Two of the 1194 pairs were removed from the corpus - one was was found to be a duplicate and the other included a text longer than one sentence.
The remaining 1192 pairs were annotated with fine-grained semantic similarity scores.

## Corpus annotation
The annotation methodology followed the one established in the [*SemEval* STS shared tasks](http://ixa2.si.ehu.es/stswiki/index.php/Main_Page) (2012-2017).
One major difference is that the example pairs for each score that were used in the *SemEval* STS annotation instructions were replaced by new ones.
Instead of one example per score value, three examples were included in the annotation instructions for each score value.
This was found to improve task comprehension and annotation quality.
The new examples were taken from the 2012 *MSRPar* and the 2013-2016 *Headlines* portions of the annotated *SemEval* STS corpora in English, and were then professionally translated into Serbian.
The final annotation instructions (with examples) are available in [Serbian](./Annotation instructions - Serbian.md) and [English](./Annotation instructions - English.md).

Five annotators separately assigned semantic similarity scores in the 0-5 range to each pair in the corpus.
They first scored a subset of 60 randomly selected pairs (~5% of the total), after which they proceeded to annotate the entire dataset.
This subset was used to calculate the annotator self-agreement scores.

The [STSAnno](https://vukbatanovic.github.io/STSAnno/) tool was used in the annotation process.

The final semantic similarity scores for each sentence pair were obtained by averaging the scores of individual annotators.

## Corpus format
The Serbian STS News Corpus is available as a tab-separated .txt file - [STS.news.sr.txt](http://github.com/vukbatanovic/STS.news.sr/blob/master/STS.news.sr.txt).
The file contains 8 tab-separated columns:
* Column 1 - the final semantic similarity score, obtained as the average of individual annotator scores.
* Columns 2-6 - the individual scores of all five annotators.
* Column 7 - the text of the first sentence in a pair.
* Column 8 - the text of the second sentence in a pair.

Sentences are written in the Serbian Latin script.
The file is encoded in UTF-8.

## Corpus statistics
The average annotator self-agreement score, expressed in terms of the Pearson correlation coefficient *r*, is 0.93.
The average inter-rater correlation between an annotator and the averaged scores of all other annotators is 0.92, which is effectively the upper bound for STS model performance on this dataset.
STS.news.sr contains around 64 thousand tokens, making the average sentence length around 27 tokens.
The average semantic similarity score value is 2.51.
When scores are rounded to their nearest integer value, their distribution in the corpus is as follows:

|  0  |   1  |   2  |   3  |   4  |  5  |
|-----|------|------|------|------|-----|
|9.06%|14.93%|16.11%|39.43%|16.53%|3.94%|

## References
TBA

## License
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

If you wish to use this dataset in a commercial product, please contact me at: vuk.batanovic / at / student.etf.bg.ac.rs
