# Medical Image Captioning

Image Captioning is a multi-modal task that requires visual reasoning and semantic/syntactic knowledge to succinctly summarize an image. In medical image captioning, the goal is to generate a report or a brief
summary describing a radiology scan such as an X- Ray or an MRI.

Deep learning models designed to handle this require a visual feature extractor and a text generator which forms the basis of an encoder- decoder architecture. Because the task resembles both summarization and translation, metrics such as ROUGE and BLEU are generally used to gauge the performance of a model.

Generating captions for radiology reports is a challenging task for two reasons. First is the presence of high entropic words in the report. The presence or absence of word can greatly alter the meaning of a sentence in a medical report for example Malignant Tumor and Benign Tumor have vastly different meanings or words such as Mediastinum which is next to non-existent in day-to-day human language is frequently used in medical reports to describe the chest cavity. The presence of high entropic words requires that the generative model to learn its meaning and correlation with certain traits in radiology scans. This means that the model has to implicitly develop visual reasoning capabilities. The second reason follows suite from the first, that because the task is to generate medical reports, there is an inherent requirement for high precision and recall, because as mentioned before, the presence or absence of a word can greatly alter the meaning of a sentence.

> **Warning**
> Fine-tuning the underlying language model heads is extremely computing resource intensive.

# Datasets

## ROCO

Radiology Objects in COntext (ROCO) is a multimodal dataset with various scans such as X-Rays, CT (Computer Tomograph),Ultrasound, Fluroscopy, MRI (Magnetic Resonance Imaging), etc. In total there are over 81,000 images and with each image there is an associated report or descriptive text.

[ROCO](https://github.com/razorx89/roco-dataset)

## Open-I Chest X-Rays

The Open-I Chest X-Rays dataset is a part of a much larger
repository of biomedical datasets sponsored by the NIH. In
this dataset there are a total of 7,470 images and for each image
there is an associated report tagged to it.

[Open-I CheXRays](https://openi.nlm.nih.gov/)
