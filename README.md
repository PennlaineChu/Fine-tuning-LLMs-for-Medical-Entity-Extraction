# Fine-tuning-LLMs-for-Medical-Entity-Extraction
[Hugging Face Model!!](https://huggingface.co/Pennlaine/Mistral-7B-v02-Entity-Extraction)

### Project Background
The adoption of electronic medical records (EMR) and electronic health records (EHR) has revolutionized healthcare, enhancing diagnostic efficiency and accuracy. EMRs are digital record systems within hospitals, while EHRs aggregate patient information across providers. EMR implementation in U.S. hospitals increased from 6.6% to 81.2% between January and June 2020. Digital records improve care quality by standardizing data and facilitating better decision-making. They also enhance administrative efficiency by simplifying access to records for departments, billing, insurance, and patients.

However, extracting medical data from free-text information is challenging. Physicians spend nearly half of their clinic time on EHR tasks, leading to reduced patient care time and increased after-hours work, contributing to lower-quality care and higher burnout rates. Improving data extraction efficiency is critical. Manual data entry is time-consuming and error-prone, while traditional NLP methods like NER and SVM struggle with diverse expressions. This work examines the performance of fine-tuned generative AI large language models (LLMs) in extracting medical entities, offering a potential solution.

This work focuses on developing a model to extract medical entities from unstructured free-text medical descriptions. The model is fine-tuned on a pre-trained LLM, combining the power of AI into this field. The model aims to act as a tool that could be utilized within business workflows to help automate and streamline data processing, decreasing human interference in this field. The work discusses the significance of the data and pre-trained model used, and proves its applicability in other fields. The model resulted in high BERT scores for evaluation. Ultimately, the model demonstrates high accuracy and flexibility, exhibiting the advantages of utilizing LLMs. This research was done to improve the fundamental process of technological development—data processing—hoping to contribute to societal benefit.


### Data
The model training uses synthetic data which are recently proven to be feasible for model-training. 
