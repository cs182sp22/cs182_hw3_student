# CS182/282 Assignment 3

In this assignment you will implement a neural network to generate news headlines, by training an LSTM-based language model.
You will also train a Transformer to summarize news articles.

## Setup
Make sure your machine is set up with the assignment dependencies.

### [Option 1] Install Anaconda and Required Packages
The preferred approach for installing all the assignment dependencies is to use
[Anaconda](https://www.anaconda.com/products/individual), which is a Python distribution
that includes many of the most popular Python packages for science, math,
engineering and data analysis. Once you install Anaconda you can run the following
command inside the homework directory to install the required packages for this homework:

```bash
conda env create -f cs182_hw3.yaml
```

Once you have all the packages installed, run the following command **every time**
to activate the environment when you work on the homework.
```bash
conda activate cs182_hw3
```

### [Option 2] Working on a Virtual Machine
This assignment is provided pre-setup with a VirtualBox image. Installation Instructions:
1. Follow [the instructions here](https://www.virtualbox.org/manual/ch02.html) to install VirtualBox if it is not already installed.
2. [Download the VirtualBox image here](https://drive.google.com/file/d/1Upo6wDUR0QiQLwyzh4pWwdnoG01VFBnv/view?usp=sharing)
3. Load the VirtualBox image using [the instructions here](https://docs.oracle.com/cd/E26217_01/E26796/html/qs-import-vm.html)
4. Start the VM. The username and password are both cs182. Required packages are pre-installed and the cs182_hw3 environment activated by default.
5. Download the assignment code onto the VM yourself.

**FAQ**

**I get an error "AMD-V is disabled in the BIOS" or "Intel-VT is disabled in the BIOS" or similar**

Solution: See [this link](https://docs.fedoraproject.org/en-US/Fedora/13/html/Virtualization_Guide/sect-Virtualization-Troubleshooting-Enabling_Intel_VT_and_AMD_V_virtualization_hardware_extensions_in_BIOS.html)


**The virtual machine won't boot**

Solutions:

- Try increasing the number of allocated CPUs: Under Settings→System→Processor
- Try [increasing the amount of allocated memory:](https://superuser.com/questions/926339/how-to-change-the-ram-allocated-to-an-os-in-virtualbox)

### Download data:
To download the data, run the following command from the assignment root directory:
```bash
bash download_data.sh
```
If you get the error "bash: ./download_data.sh: Permission denied" run `chmod +x download_data.sh` and try again.

### Start Jupyter Notebook
After you download data, you should start the IPython notebook server
from the homework 1 directory with the following command:

```bash
jupyter notebook
```

## Submitting your work:
Once you are done working run the `collect_submission.sh` script;
this will produce a file called `assignment3.zip`.

If you encounter "zip not found" error on macos, run the following command.
```bash
brew install zip
```

Check that your submission contains:
- "1 Language Modeling.ipynb" and "2 Summarization.ipynb"
- "transformer.py", "transformer_attention.py", "language_model.py"
- Your folder for best models for each notebook, `best_models`
- Your folder for submission logs, `submission_logs`

Upload this file to Gradescope.
The Gradescope will run an autograder on the files you submit. It is very unlikely but still possible that your implementation might fail to pass some test cases due to randomness.
If you think your code is correct, you can simply rerun the autograder to check check whether it is really due to randomness.


## Q1: LSTM for Language Modeling (40 points)
The IPython notebook `Language Modeling.ipynb` will introduce you to the implementation
of preprocessing raw text and training an LSTM. Follow the instructions in the notebook to complete this part.

## Q2: Transformer Network for Summarization (60 points)
The IPython notebook `Summarization.ipynb` will introduce you to the implementation
of Transformer to summarize news articles. Follow the instructions in the notebook to complete this part.
