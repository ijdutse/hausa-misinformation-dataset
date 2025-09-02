# Hausa Misinformation Dataset

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

A curated and annotated dataset of fake and genuine online content in the Hausa language. This resource is intended to support research in Natural Language Processing (NLP), misinformation detection, and media studies for low-resource languages.

## 📥 Download Data

The latest version of the dataset can be found in the [`/data/processed/`](/data/processed/) directory.
- **Primary File**: `hausa_misinformation_dataset_v1.0.csv`
- **Format**: CSV (Comma-Separated Values)
- **Encoding**: UTF-8

**Direct Download Link**: [Click here to download v1.0](data/processed/hausa_misinformation_dataset_v1.0.csv)

*(Alternatively, you can use [Git LFS](https://git-lfs.github.com/) if the dataset is very large)*

## 🗂️ Dataset Overview

| Column Name | Description | Data Type |
| :--- | :--- | :--- |
| `id` | Unique identifier for each text sample | Integer |
| `text` | The full text of the news article/social media post | String |
| `label` | Annotation label (`fake` or `genuine`) | Categorical |
| `source` | Type of source (e.g., `facebook`, `online_news`, `twitter`) | Categorical |
| `date_collected` | Date when the sample was collected | Date |
| `annotator_notes` | Optional notes from the annotators | String |

**Statistics:**
- Total samples: ~1000
  - Fake samples: ~500
  - Genuine samples: ~500
- Average text length: 250 words

## 🚀 Quick Start

1.  **Clone the repository**
    ```bash
    git clone https://github.com/ijdutse/hausa-misinformation-dataset.git
    cd hausa-misinformation-dataset
    ```

2.  **Load the data in Python (Pandas)**
    ```python
    import pandas as pd
    df = pd.read_csv('data/processed/hausa_misinformation_dataset_v1.0.csv')
    print(df['label'].value_counts())
    ```

3.  **Explore the data**
    Check out the Jupyter notebooks in the [`/notebooks/`](/notebooks/) directory for examples of data analysis and a baseline model.

## 📚 Documentation

For detailed information, please refer to our documentation:
- **[Data Collection Methodology](docs/data_collection.md)**: How the data was sourced and gathered.
- **[Annotation Guidelines](docs/annotation_guidelines.pdf)**: The criteria and process used by annotators to label content.
- **[Ethical Considerations](docs/ethical_considerations.md)**: Our approach to privacy, ethics, and responsible use.

## 🤝 Contributing

We welcome contributions! Please read our [Contributing Guidelines](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md) before submitting a pull request or issue. You can help by:
- Annotating more data.
- Improving preprocessing scripts.
- Suggesting new features or resources.

## 📜 License

This dataset is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See the [LICENSE](LICENSE) file for details.
**Please note:** This is a common license for datasets to prevent misuse. Choose the license that best fits your goals.

## 🙏 Citation

If you use this dataset in your research, please cite it using the following BibTeX entry:

```bibtex
@dataset{hausa_misinformation_dataset_2025,
  author = {Isa Inuwa-Dutse},
  title = {Hausa Misinformation Dataset},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/ijdutsee/hausa-misinformation-dataset}
}
