# The Gumar Corpus N-grams

> Copyright © 2017-2018 New York University Abu Dhabi
>
> Computational Approaches to Modeling Language (CAMeL) Lab

## About

We present the Gumar Corpus n-grams.
The n-grams are Generated from the
[Gumar Corpus](https://camel.abudhabi.nyu.edu/gumar/), a large-scale corpus of
Gulf Arabic containing more than 100 million words [1,2].
The n-grams are in order of 5, that is 5, 4, 3, 2 and 1 grams with their
respective frequency counts and number of documents they appear in.
The n-grams are counted across the entire corpus and also across each dialect
category individually.
The format of the n-gram files follows a similar format of Google n-grams with
the exception of the year column which we don't produce.

## Preprocessing

* All documents of the corpus are converted into plain text.
* Basic UTF-8 character cleaning.
* Punctuation separation.

## Dialect Categorization

Below are categorizations of the dialects and their respective document counts.
For specific information per document please refer to the spreadsheet attached
with this package.

| Tag      | Dialect                                      | Document Count |
|:--------:|:--------------------------------------------:|:--------------:|
| SA       | Saudi                                        | 770            |
| AE       | Emirati                                      | 115            |
| KW       | Kuwaiti                                      | 87             |
| OM       | Omani                                        | 14             |
| QA       | Qatari                                       | 10             |
| BA       | Bahraini                                     | 8              |
| MSA      | Modern Standard Arabic                       | 82             |
| EGY      | Egyptian                                     | 3              |
| LEV      | Levantine                                    | 5              |
| MOR      | Moroccan                                     | 1              |
| IRQ      | Iraqi                                        | 5              |
| YEM      | Yemeni                                       | 1              |
| UNID_GA  | Unidentified Gulf Arabic                     | 116            |
| MIXED_GA | Mixed Gulf Arabic                            | 11             |
| MIXED    | Gulf Arabic mixed with other Arabic dialects | 4              |

## Download

You can
[download the GUMAR n-grams here](https://github.com/owo/GUMAR_NGRAMS/releases).

The n-grams are split by dialect into seperate compressed folders of the form
`<TAG>.tar.xz` where *\<TAG>* is one of the dialect tags listed above.
There is an additional file `ALL.tar.xz` that contains n-grams of all the
dialects combined.

Once downloaded, you can extract the files by running the following:

```bash
tar -xJf <TAG>.tar.xz
```

This will generate a folder `<TAG>/` in the current working directory.

## Directory Structure

Each folder contains the following n-gram files:

* `1-grams_<TAG>.tsv`
* `2-grams_<TAG>.tsv`
* `3-grams_<TAG>.tsv`
* `4-grams_<TAG>.tsv`
* `5-grams_<TAG>.tsv`

## Format

Each n-gram file consists of three tab separated columns as follows:

    <n-gram> TAB <frequency> TAB <# of documents> NEWLINE

Each \<n-gram> larger than one is single space separated.

Example of a 2-grams row:

<pre dir="rtl">
انتظر منك	85	69
</pre>

*\* Note that the example above is displayed right-to-left but the columns are
in the order described.*

Each n-gram file is sorted by `<frequency>` in descending order.

## Data Sources

If you would like more details on the data used to generate the n-grams,
take a look at the [Gumar_Info.tsv](./Gumar_Info.tsv) file.
It is a Tab Separated Values file containing author and title
information for each document, as well as its dialect and the link it was
downloaded from. Duplicate entries for title-author pairs indicate that a
document was split into multiple files.

## Citation

Please use the following citation when referencing this resource:

> Khalifa, Salam, Nizar Habash, Dana Abdulrahim, and Sara Hassan.
> "A Large Scale Corpus of Gulf Arabic." In Language Resources and Evaluation
> Conference. 2016. Portorož, Slovenia

## License

This compilation is licensed under a
[Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/).

## References

[1] [Khalifa, Salam, Nizar Habash, Dana Abdulrahim, and Sara Hassan. "A Large Scale Corpus of Gulf Arabic." In Language Resources and Evaluation Conference. 2016. Portorož, Slovenia](http://www.lrec-conf.org/proceedings/lrec2016/pdf/823_Paper.pdf)

[2] [Khalifa, Salam, Nizar Habash, Fadhl Eryani, Ossama Obeid, Dana Abdulrahim, and Meera Al Kaabi. "A Morphologically Annotated Corpus of Emirati Arabic". In Language Resources and Evaluation Conference. 2018. Miyazaki, Japan](http://www.lrec-conf.org/proceedings/lrec2018/pdf/529.pdf)
