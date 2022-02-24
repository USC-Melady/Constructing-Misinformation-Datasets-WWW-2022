# Construction of Large-Scale Misinformation Labeled Datasets from Social Media Discourse using Label Refinement on COVID-19 Vaccines

## 1) **WWW'22 Dataset: Construction of Large-Scale Misinformation Labeled Datasets from Social Media Discourse using Label Refinement**

### init_data_split_and_label.csv

- **cascade_source_tweetid**: tweetid of source tweet of the cascade.
- **init_label**: In the case of va/test cascades these are binarized ground-truth labels, in the case of train cascades these are binarized weak labels.
- **init_data_split**: tr/va/test split.
- **human_gt_label**: for va/test cascades.

### pruned_cascades_feats_fake_true_minlen5.csv

- Contains features of the cascade source tweets (cascade_tid == tweetid, is the same as cascade_source_tweetid).
- **ns_label (ns_url)** is for the extracted weak label from tweet text.

### weakly_labeled_cascade_features_minlen5.pkl
- Contains features of the cascades (i.e., source tweet and its engagements)
- **Features used in CSI** (text, user, relative timestamp of engagements in the cascade)
- **label field** here is the *weak label* of each cascade's source tweet.


### features.csv
- Contains raw tweet features for the 370K tweets in the weakly labeled cascades (source tweet and its engagement tweets)


## 2) **COVID-19 Vaccines: Characterizing Misinformation Campaigns and Vaccine Hesitancy on Twitter**

### covid_vaccine_Dec_9_2020_Apr_24_2021.csv
- Contains **tweetid** and **ns_label (unreliable/conspiracy/reliable/NaN for unlabeled)** for tweets from Dec, 9, 2020 to Apr 24, 2021.
- User Twitter API (tweepy) to obtain tweet features.


## **Please cite the following works:**

```
@inproceedings{sharma2022constructing,
author = {Sharma, Karishma and Ferrara, Emilio and Liu, Yan},
title = {Construction of Large-Scale Misinformation Labeled Datasets from Social Media Discourse using Label Refinement},
year = {2022},
isbn = {9781450390965},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3485447.3512271},
doi = {10.1145/3485447.3512271},
booktitle = {Proceedings of the Web Conference 2022},
numpages = {10},
keywords = {misinformation, datasets, labeling, social media, covid-19, vaccines},
location = {Virtual Event, Lyon, France},
series = {WWW '22}
}
```

```
@article{sharma2021covid,
  title={COVID-19 vaccines: characterizing misinformation campaigns and vaccine hesitancy on twitter},
  author={Sharma, Karishma and Zhang, Yizhou and Liu, Yan},
  journal={arXiv preprint arXiv:2106.08423},
  year={2021}
}
```

