# GeminiScan: Similarity Classification of HTML with Large Language Models

GeminiScan is a novel approach leveraging Large Language Models (LLMs) for near-duplicate detection in web testing. This project combines a small-scale LLM for efficient inference with a large-scale LLM for prompt optimization.

## Features

- Efficient classification of near-duplicate and distinct web pages
- Combination of small and large LLMs for balanced performance and resource usage
- Evaluation on the Yandrapally et al. 2020 dataset
- High F1 scores for Addressbook and PetClinic applications
- Low false positive rate in near-duplicate detection

## Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/H3nkl3r/GeminiScan.git
    cd GeminiScan
    ```

2. **Create and activate a virtual environment:**
    ```bash
    python3 -m venv env
    source env/bin/activate
    ```

3. **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```
## Usage

1. **Preprocess the HTML files:**
    Use the provided scripts to preprocess your HTML files, focusing on the body tag and excluding scripts.

    ```bash
    2_0_tnk_data_pre_processing.ipynb
    ```

2. **Run the inference:**
    Use the small-scale LLM to classify the preprocessed HTML files.

    ```bash
    3_1_tnk_predict_LLM.ipynb
    ```

4. **Visualize the results:**
    Compare the performance of the classifications against the ground truth.

    ```bash
    4_0_tnk_visualize_results.ipynb
    ```

## Dataset

The dataset used for evaluation is the Yandrapally et al. 2020 dataset, which includes labeled state pairs from nine open-source web applications. This dataset is a benchmark for evaluating near-duplicate detection methods.

## Results

The evaluation of GeminiScan on the Addressbook and PetClinic applications from the dataset demonstrated competitive performance, with F1 scores of 0.87 and 0.78, respectively. The method shows particular strength in avoiding false positives, rarely misclassifying near-duplicates as distinct.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Authors

- Timo Kühne
- Advisor: Dr. Andrea Stocco
