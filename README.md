# Fine-tuning-LLMs-for-Medical-Entity-Extraction
[Hugging Face Model!!](https://huggingface.co/Pennlaine/Mistral-7B-v02-Entity-Extraction)

### Project Background
The adoption of electronic medical records (EMR) and electronic health records (EHR) has revolutionized healthcare, enhancing diagnostic efficiency and accuracy. EMRs are digital record systems within hospitals, while EHRs aggregate patient information across providers. EMR implementation in U.S. hospitals increased from 6.6% to 81.2% between January and June 2020. Digital records improve care quality by standardizing data and facilitating better decision-making. They also enhance administrative efficiency by simplifying access to records for departments, billing, insurance, and patients.

However, extracting medical data from free-text information is challenging. Physicians spend nearly half of their clinic time on EHR tasks, leading to reduced patient care time and increased after-hours work, contributing to lower-quality care and higher burnout rates. Improving data extraction efficiency is critical. Manual data entry is time-consuming and error-prone, while traditional NLP methods like NER and SVM struggle with diverse expressions. This work examines the performance of fine-tuned generative AI large language models (LLMs) in extracting medical entities, offering a potential solution.

This work focuses on developing a model to extract medical entities from unstructured free-text medical descriptions. The model is fine-tuned on a pre-trained LLM, combining the power of AI into this field. The model aims to act as a tool that could be utilized within business workflows to help automate and streamline data processing, decreasing human interference in this field. The work discusses the significance of the data and pre-trained model used, and proves its applicability in other fields. The model resulted in high BERT scores for evaluation. Ultimately, the model demonstrates high accuracy and flexibility, exhibiting the advantages of utilizing LLMs. This research was done to improve the fundamental process of technological development—data processing—hoping to contribute to societal benefit.


### Data
The model training uses synthetic data (OpenAI GPT-3) which are recently proven to be feasible for model-training. 
The training data consists of common knowledge and question considering the easier access and wider application that this training dataset could contribute to. The responses are in JSON format since it is an ideal representing structured data for entity extraction. The following is and example which can also be viewed in the 'train_data.csv' file:

````
<s>[INST]What institute at Notre Dame studies the reasons for violent conflict? Answer the question, extract the organization, field of study and return in Json format.[/INST]```json
{
    ""question"": ""What institute at Notre Dame studies the reasons for violent conflict?"",
    ""answer"": ""The Kroc Institute for International Peace Studies"",
    ""entities"": [
        {
            ""Organization"": ""Notre Dame""
        },
        {
            ""Field of Study"": ""the reasons for violent conflict""
        }
    ]
}
```</s>
````



The evaluation data only consists of medical descriptions and questions also generated by Chat GPT. Here is an example, the evaluation dataset can be viewed in the `eval_data.json` file:

````
[INST]Type 2 Diabetes Mellitus is a chronic metabolic disorder characterized by insulin resistance and relative insulin deficiency. This condition leads to chronic hyperglycemia, which can cause significant damage to various body systems over time. Write a short summary of how to treat patients with diabetes. Answer the question, extract the disorder, type of disorder, causes, effect, ICD Code, and return in Json format.[/INST]```json
{
    "question": "Type 2 Diabetes Mellitus is a chronic metabolic disorder characterized by insulin resistance and relative insulin deficiency. This condition leads to chronic hyperglycemia, which can cause significant damage to various body systems over time. Write a short summary of how to treat patients with diabetes.",
    "answer": "Treatment for diabetes typically involves a combination of lifestyle modifications, medication, and insulin therapy.",
    "entities": [
        {
            "Disorder": "Type 2 Diabetes Mellitus"
        },
        {
            "Type of Disorder": "Chronic Metabolic Disorder"
        },
        {
            "Causes": "Insulin Resistance and Relative Insulin Deficiency"
        },
        {
            "Effect": "Chronic Hyperglycemia"
        },
        {
            "ICD Code": "E11"
        }
    ]
}
```
````

### Methodology

The data processing, fine-tuning process, code to run the model, and evaluation process could be viewed in the jupyter notebook `main.ipynb`.

Since the notebook primarily relies on the Hugging Face library, please note that your token should be granted access to the gated model. 
To be granted access, please go to the Hugging Face page and click on the "Agree and access repository" button, your access would be automatically granted.

### Hardware

The GPU used is "NVIDIA_A100_80GB x 8."
