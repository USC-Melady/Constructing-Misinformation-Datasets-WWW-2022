## output_refined_labels.csv
- contains the output misinformation dataset after label refinement.
- **cascade_tid**: tweetid of cascade source tweet
- **weak_label**: weak news-source credibility labels (binarized)
- **binarized_human_gt_label**: binarized human ground-truth (fact-checked) label
- **init_data_split**: tr/va/te
- **prob_cls_1**: predicted by refined misinformation detection model (CSI-Ruchansky et al'17)
- **action**: QUERY (or REMOVE), RETAIN, FLIP. Each action refers to either remove from dataset (or query a human resource to get correct label), 
RETAIN (weak label), FLIP (flip weak label) as predicted by label refinement procedure using CSI detection model uncertainity and social context.
- **refined_label**: Final refined label for misinformation dataset. (-1 if unknown/query, 0 for True claim, 1 for Misinformation claim).

## Distortion of facts (label definition)
- **Misinformation claims** (mostly_false, false/conspiracy, mixture, unproven): Label = 1 (binarized)
- **True claims** (true, mostly_true, debunk): Label = 0 (binarized)
