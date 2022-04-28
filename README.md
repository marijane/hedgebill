# Hedgebill
Hedgebill is a tool for collaboratively creating and managing reproducible search hedges.

## Project Goals

**Hedgebill aspires to:**
- Facilitate building search strategies out of multiple hedges
- Automatically generate search strategy strings for abstracts databases
- Launch search strategies against database APIs like NCBI Entrez/PubMed, Scopus, and Dimensions and save the results in a variety of formats, and pull lists of identifers like PMID or DOI.
- Be accessible, from undergraduate students breaking down search questions for the first time to skilled reference librarians and subject matter experts creating and validating hedges for systematic reviews
- Allow database users to easily experiment with different search terms in their hedges
- Make it easy to find and remove duplicate search terms from their hedges
- Allow database users to easily generate sets of searches on the same topic across a range of precisions/sensitivity to find the right search terms
- Allow database users to thoroughly document their search strategy
- Allow database users to easily snapshot hedges and search strategies for validated searches
- Target documentation formats such as the one suggested in (Haddaway et al., 2022)

All that said, I am not a professional software developer so these goals may be a stretch.

## Current Capabilities

At present, Hedgebill can read lists of MeSH terms and keywords from a series of text files organized by single search topic, build a formatted hedge for each, and combine them in a variety of ways to produce search results with a range of recall/precision/sensitivity/specificity, and then retrieves those results from PubMed via the Entrez API. It makes very short work of exploring lots of different ways to build a search.

## Why is this thing called Hedgebill?

Expert literature searchers have used the term "hedge" to refer to search strategies saved for later reuse since at least the late 1970s (Campbell, 2016). When used as a verb, The OED indicates [hedge](https://www.google.com/search?q=define%3Ahedge) can mean 'limit or qualify (something) by conditions or exceptions', such as 'hedging a bet', which seems appropriate to the context of building quality search strategies for literature reviews by carefully selecting the terms to include in the search hedges.

A [hedgebill](https://en.wiktionary.org/wiki/hedgebill) ([photo](https://museum.wales/collections/online/object/fc64749b-944e-3a1a-ad82-812d2702c8b3/Hedge-bill/?field0=string&value0=hedge%20bill&field1=database&value1=mwl&index=1)) is a [long-handled](https://www.thefreedictionary.com/Hedge+bill) [billhook](https://www.merriam-webster.com/dictionary/billhook) used by a [hedger](https://en.wiktionary.org/wiki/hedger) to build and maintain [hedges](https://www.merriam-webster.com/dictionary/hedge) and [hedgerows](https://www.merriam-webster.com/dictionary/hedgerow). "Bill" also brings to mind such things as a [bill of lading](https://www.merriam-webster.com/dictionary/bill%20of%20lading) or a [bill of health](https://www.merriam-webster.com/dictionary/bill%20of%20health).

Given the above history and definitions, **Hedgebill** is a tool used to build, maintain, and document search hedges in order to make them reproducible, which are expressed as bills of lading (i.e. a list of things in a given hedge), and which could perhaps also be thought of as bills of health since systematic literature searching and reviews tend to be focused on biomedical questions.

## Why did I build this thing?

In March 2020, my colleagues and I at the [OHSU Library](https://www.ohsu.edu/library) spent our first month or so of the pandemic intensely focused on conducting literature searches about COVID-19 for the staff of the Oregon Health Authority. While working on these searches, I became extremely frustrated at the lack of good ways to document and save searches in a reproducible way. Before I became a librarian, I spent nearly two decades in the software industry as a tester, technical writer/editor, and semantic modeler, and I yearned for a structured query language like SQL or SPARQL that could be used to build and document literature searches. Lacking that, I thought about ways to make building search hedges easier and collaboratively editable. My first attempt to build this tool was in Google Sheets with Google App Script, but I didn't have the time to dedicate to making it work correctly. Two years later, I find myself working on a complex and expansive search to find as many papers on a particular topic, so I revived the idea in this new, far more flexible form.

## References

Haddaway, N. R., Rethlefsen, M. L., Davies, M., Glanvill, J., McGowan, B., Nyhan, K., & Young, S. (2022). A suggested data structure for transparent and repeatable reporting of bibliographic searching. https://agrirxiv.org/search-details/?pan=20210337806

Campbell, S. (2016). What is the difference between a filter and a hedge?. Journal of EAHIL, 12(1). Retrieved from http://ojs.eahil.eu/ojs/index.php/JEAHIL/article/view/95
