# ATLANTIS - ArTificiaL And Natural waTer-bodIes dataSet
## A Benchmark for Semantic Segmentation of Waterbody Images

This is the respository for the ATLANTIS. All waterbody labels are comprehensively described in [ATLANTIS Wiki](https://github.com/smhassanerfani/atlantis/wiki).
![](https://github.com/smhassanerfani/atlantis/blob/master/wiki/dataset.png)

For the first time, this dataset covers a wide range of natural waterbodies such as sea, lake, river and man-made (artificial) water-related sturcures such as dam, reservoir, canal, and pier. ATLANTIS includes 5,195 pixel-wise annotated images split to 3,364 training, 535 validation, and 1,296 testing images. In addition to 35 waterbodies, this dataset covers 21 general labels such as person, car, road and building.

## AQUANet
In addition to waterbodies dataset, and in order to tackle the inherent challenges in the segmentation of waterbodies, we also developed, CNN-based semantic segmentation network, which takes advantage of two different paths to process the aquatic and non-aquatic regions, separately. Each path includes low-level feature and cross-path modulation, to adjust features for better representation. The results show that AQUANet outperforms other state-of-the-art semantic-segmentation networks on ATLANTIS, and the ablation studies justify the effectiveness of the proposed components.
![](https://github.com/smhassanerfani/atlantis/blob/master/wiki/frequency_distribution.svg)

The ATLANTIS dataset is designed and developed with the goal of capturing a wide-range of water-related objects, either those exist in natural environment or the infrastructure and man-made (artificial) water systems. In this dataset, labels were first selected based on the most frequent objects, used in water-related studies or can be found in real-world scenes. Aside from the background objects, total of 56 labels, including 17 artificial, 18 natural water-bodies, and 21 general labels, are selected. These general labels are considered for providing contextual information that most likely can be found in water-related scenes. After finalizing the selection of waterbody labels, a comprehensive investigation on each individual label was performed by annotators to make sure all the labels are vivid examples of those objects in real-world. Moreover, sometimes some of the water-related labels, e.g., levee, embankment, and floodbank, have been used interchangeably in water resources field; thus, those labels are either merged into a unique group or are removed from the dataset to prevent an individual object receives different labels.

In order to gather a corpus of images, we have used Flickr API to query and collect 800 "medium-sized" unique images for each label based on seven commonly used "Creative Commons" and "United States Government Work" licenses. Downloaded images were then filtered by a two-stage hierarchical procedure. In the first stage, each annotator was assigned to review a specific list of labels and remove irrelevant images based on that specific list of labels. In the second stage, several meetings were held between the entire annotation team and the project coordinator to finalize the images which appropriately represent each of 56 labels. Finally, images were annotated by annotators who have solid water resources engineering background as well as experience working with the [CVAT](https://github.com/openvinotoolkit/cvat), which is a free, open source, and web-based image/video annotation tool.

Figure~\ref{fig:freq-imgs-pixels} shows the frequency distribution of the number of images and pixels for waterbody labels. Labels are ranked based on pixel frequencies. Such a long-tailed distribution is common for semantic segmentation datasets \cite{lin2014microsoft, zhou2019semantic} even if the number of images that contain specific label are pre-controlled. Such frequency distribution for pixels would be inevitable for objects existing in real-world. Taking ``water tower'' as an example, despite having 219 images, the number of pixels are less than many other labels in the dataset. In total, only $4.96\%$ of pixels are unlabeled, and $34.07\%$ and $60.97\%$ of pixels belong to waterbodies (natural and man-made) and general labels, respectively. 
