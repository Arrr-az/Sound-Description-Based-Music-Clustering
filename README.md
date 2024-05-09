# Sound-Description-Based-Music-Clustering
In this project, we aim to cluster different music albums based on their sound-description, as described by users of online music community RateYourMusic. For this purpose were built both a music descriptor dataset and an unsupervised classification model with the "k-Means Clustering" algorithm.

# What is "Sound Description"
In the online music forum "Rate Your Music", users can vote on pre-determined descriptors for any musical release they want. Descriptors are simply words or short terms that capture a certain characteristic of that musical release. As an example here are the most voted descriptors for the album "Take Me to Your Leader", by King Geedorah: "science fiction, sampling, humorous, concept album, quirky, abstract, lush, playful, male vocalist, rhythmic, surreal, boastful, bittersweet, violence, melodic, conscious, fantasy, protest, mellow, urban, mysterious, futuristic, dense, lo-fi, apocalyptic, hypnotic, rebellious, atmospheric, martial, energetic, eclectic, technical, complex, ethereal, cryptic"

As can be noted, not all descriptors refer to sound aspects of a certain release. In this example, "concept album", "boastful", "conscious", "protest" and some others refer more to lyrical themes or how the album was structured around a certain concept. However, our goal is to cluster albums based on their sound/musical aspects similarities, so we're not interested in these types of descriptors mentioned, but yes in "sound-based" descriptors.

# Repository components

### HTML_pages
Contains 706 album/EP pages from the RYM forum. From them we scrap the descriptors from each release.

### Notebooks
Contains the Jupyter Notebooks written for both scrapping the HTML, building the dataset, and training our k-Means Clustering model. I've also put in these notebooks some relevant theoretical concepts aiming to help navigate through why we are modeling things that way, and how k-Means Clustering works.

### Discarded_Notebooks
Mostly modeling ideas that were crafted, tested and discarded. The main idea where everything else revolved around was to clump similar enough descriptors into the positive side of an axis, while descriptors that meant the opposite went on the negative side of the same axis. From this idea, a few different axes were formed and became the new features. It didn't turn out as well as the plain, simpler approach with PCA done in the main notebooks, but it was in these discarded notebooks where I learned the most, and most of that learning is written in them.

### csv
.csv files from different datasets, each one used in different phases of the process. Most of them only in Discarded_Notebooks.

### Outputs
.txt files containing the outputs of k-Means Clustering on differently modeled datasets. The most successfull one, created from "04_PCA_and_Clustering.ipynb", is "final_output.txt"
