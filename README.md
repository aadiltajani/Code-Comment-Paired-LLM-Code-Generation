## The Repo contains the files for Code-Comment Paired Instruction Tuned LLM for Code Generation project by Aadil Tajani for CSC591 Generative AI for Software Engineering

# Resources Needed:
- Storage: ~5GB
- GPU (>= NVIDIA V100 recommended)
- RAM (>= 10GB)

# File Description:
- `DatasetCreation.ipynb`: A python notebook with steps to augment the dataset with comments using gpt3.5 in batches and a multithreaded process with the ability to monitor progress, aborted ids, and tokens used with commenst explaining the usecase.
- `codet5_comment_instruction_tune.ipynb`: A python notebook that does the instruction tuning on models specifically for codet5+ 220M py model here. It starts with cloning repos, downloading/uploading dataset and installing libraries. Then, making changes to the seq2seq file to use the desired dataset(augmented/original), and set the target(output/newcode) and source(instruction + input) variables accordingly and change the epochs, model name, save directory, target and source len to desired values. Then, adding the tokenizer files from original model to saved final checkpoint of the finetuned model, inference is done and the preds are processed to merge the generated humaneval solutions of 164 problems in one file. Humaneval is then used to evaluate the outputs by commenting out the execute line mentioned n the execution.py file and gives out the pass@k values.
