# Modal Dependency Dataset

This repository contains the English modal dependency dataset described in the ACL 2021 [paper](https://aclanthology.org/2021.acl-long.122/) named Factuality Assessment as Modal Dependency Parsing.


## Data
(1) The annotated modal dependency trees are in the `data` directory.

(2) Each edge has 4 fields, separated by tabs:
```
child    child_type    parent  relation
```
- child: the child node
- child_type: the child is a conceiver node or an event node
- parent: the parent node of this child
- relation: the relation between the child and the parent. pos, pp, pn, neg are Positive, Partial Positive, Neutral Positive and Negative respectively.

The child node and parent node are represented by their `sentence id, start token id in the sentence and end token id in the sentence`. For example, `0_0_3` means this node is in the first sentence in this document, its start token position in this sentence is 0, and its end token position in this sentence is 3. We use `-1_-1_-1` to represent the `ROOT` node, `-3_-3_-3` to represent the `Author` node, `-5_-5_-5` to represent the `Null-Conceiver` node.

(3) Please note: we downloaded the coronavirus news data set using [AYLIEN API](https://aylien.com/blog/free-coronavirus-news-dataset). We did some preprocessing before the annotation. Before we post the instructions about how to map the annotations to the articles and do the preprocessing, please email the first author of the paper to get the articles.


## Annotation Guidelines
You can find our annotation guidelines in the `guidelines` directory.
