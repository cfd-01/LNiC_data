# LNiC_data
Datasets for Label Noise in Context

These are the indices and post ids that identify the subset of data used in the paper Label Noise in Context.

## Jeopardy
The paper experiments used a subset of approximately 5k question-answer pairs
from www.j-archive.com labeled by their categories. `identifiers_for_jeopardy.csv`
lists tuples of (<show_number>, <round>, <value>, <category>) for each example
in the dataset.

For instance, "('4931', 'Double Jeopardy!', '$400', 'SCIENCE')"
means "show number 4931, in the Double Jeopardy round, the $400 question in the
SCIENCE category." This example can be viewed here: http://www.j-archive.com/showgame.php?game_id=765


## Stack Exchange
The precision and F_0.5 experiments in the paper use 5k question-topic pairs from
Stack Exchange, and the demo explores noise in 30k pairs. These were sampled
from the Stack Exchange Data Dump, available here: https://archive.org/details/stackexchange

Specific examples for are identified in `post_ids_for_stack_exchange5k.csv` and
`post_ids_for_stack_exchange30k.csv`. Each row is a <forum_topic>, <post_id>
pair. The forum topic identifies the name of the Stack Exchange forum, and the
post_id identifies the specific post that the question came from. For instance,
"cooking,65802" means the question came from the row in
`cooking.stackexchange.com/Posts.xml` where the Id field is 65802. We use the
text from the "Title" field as the utterance. Attribution for each utterance
can be found in its corresponding post.

## Stack Overflow
The paper experiments used a subset of approximately 5k examples from the
Stack Overflow dataset described in
```
@inproceedings{xu-etal-2015-short,
    title = "Short Text Clustering via Convolutional Neural Networks",
    author = "Xu, Jiaming  and
      Wang, Peng  and
      Tian, Guanhua  and
      Xu, Bo  and
      Zhao, Jun  and
      Wang, Fangyuan  and
      Hao, Hongwei",
    booktitle = "Proceedings of the 1st Workshop on Vector Space Modeling for Natural Language Processing",
    month = jun,
    year = "2015",
    address = "Denver, Colorado",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/W15-1509",
    doi = "10.3115/v1/W15-1509",
    pages = "62--69",
}
```
and available from https://github.com/jacoxu/StackOverflow

The `indices_for_stack_overflow.csv` identifies the subset we used; the numbers
refer to the line numbers in
https://github.com/jacoxu/StackOverflow/blob/master/rawText/title_StackOverflow.txt
