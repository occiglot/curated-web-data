# Curated Web Data for Multilingual Pretraining

Welcome to the `curated-web-data` repository! This repository contains a collection of "good and bad" web domains for large language model (LLM) pretraining. The domains are categorized into "useful" and "unwanted" based on their quality and relevance for multilingual pretraining. 

## Repository Structure

The repository is organized as follows:

```
curated-web-data/
│
├── useful/
│   ├── english/
│   ├── french/
│   ├── german/
│   ├── spanish/
│   ├── .../
│   └── multilingual/
│
├── unwanted/
│   ├── english/
│   ├── french/
│   ├── german/
│   ├── spanish/
│   ├── .../
│   └── multilingual/
│ 
└── duplicated/

```

### Useful Folder

The `useful` folder contains subfolders for each European language and a `multilingual` subfolder for domains that contain multiple languages. The domains in these folders are considered "good" for LLM pretraining. Here's what "useful" means in this context:

- **High Quality Content**: The domains contain well-written, grammatically correct, and informative content.
- **Diverse Topics**: The domains cover a wide range of topics, providing a rich and varied dataset for pretraining.
- **Accurate Information**: The content is factually accurate and comes from reputable sources.
- **Original Content**: The content is original and not plagiarized from other sources.
- **Proper Attribution**: When content is sourced from other works, proper attribution is given.
- **Cultural Relevance**: The content reflects the cultural and linguistic nuances of the respective language, providing a more authentic training dataset. Especially in the context of European languages.

### Unwanted Folder

The `unwanted` folder also contains subfolders for each European language and a `multilingual` subfolder. The domains in these folders are considered "bad" for LLM pretraining. Here's what "unwanted" means in this context:

- **Low Quality / Noisy Content**: The domains contain poorly written, grammatically incorrect, or nonsensical content.
- **Spammy Content**: The domains are filled with spam, advertisements, or irrelevant content that does not contribute to meaningful pretraining.
- **Misinformation**: The content is factually incorrect, misleading, or comes from unreliable sources.
- **Hate Speech**: The content includes hate speech, offensive language, or discriminatory remarks.
- **Violence**: The content includes physical and non-physical violence. 
- **Adult**: The content includes the abbreviation for not safe for work (NSFW) or non-educational sexual content. 
- **Irrelevance**: The content is irrelevant to the language or cultural context, making it unsuitable for pretraining purposes.
- **Ethical Bias**: The content contains an ethical bias that does not align with the values of Occiglot, or the values of any of the European countries. 
- **Controversial**: If the content is controversial or in public discussion in regards to the previously stated reasons. 

### Duplicated Folder

The `duplicated` folder contains domains where dedicated and clean datasets already exist. These domains should have their own structured datasets available for use, making web crawls unnecessary.

Examples of domains in this category include:
- **Wikipedia**: A multilingual, crowd-sourced encyclopedia with comprehensive datasets available through various APIs and data dumps.
- **Reddit**: A platform with extensive and regularly updated datasets covering a wide range of discussions and communities.
- **Stack Overflow**: A Q&A site for programmers with high-quality datasets available for research purposes.

By categorizing these domains under `duplicated`, we ensure that our web crawling efforts are focused on sources where such structured datasets do not exist, optimizing the efficiency and effectiveness of our data collection process.

## Contribution

We welcome contributions to this repository. If you have suggestions for additional domains that should be included in either the `useful` or `unwanted` folders, please submit a pull request or open an issue.

### How to Submit a Pull Request

1. **Fork the Repository**: Start by forking this repository to your own GitHub account.
2. **Clone Your Fork**: Clone your forked repository to your local machine.
   ```bash
   git clone https://github.com/your-username/curated-web-data.git
   cd curated-web-data
   ```
3. **Create a Branch**: Create a new branch for your changes.
   ```bash
   git checkout -b add-new-domains
   ```
4. **Add Your URLs**: Use the provided [`web_domain.csv`](./docs/template/web_domain.csv) file to add your URLs. Each URL should be accompanied by a comment explaining why the domain is important or not. You can also optionally add any number of tags in the third row to enhance the domain with meta-information. A list of all existing tags can be found in the `docs` folder.
   - **Domain**: The web domain name, use wildcard `*` to include subdomains (e.g., `*.wikipedia.org` for all language versions of Wikipedia).
   - **Comment**: A short comment on why this domain is important or unwanted. Please ensure that you add a link to the dataset if you add duplicated domain.
   - **Tags**: Optional tags for additional meta-information.
   
   Example:
   ```
   Domain,Comment,Tags
   *.wikipedia.org,High-quality and reliable multilingual resource,encyclopedia;education
   example.com,Poorly written and unreliable source,spam
   ```
5. **Commit Your Changes**: Commit your changes to your branch.
   ```bash
   git add .
   git commit -m "Added new useful and unwanted domains"
   ```
6. **Push Your Changes**: Push your changes to your forked repository.
   ```bash
   git push origin add-new-domains
   ```
7. **Create a Pull Request**: Open a pull request from your branch to the main branch of this repository. Provide a brief description of your changes and why they should be merged.

### How to Raise an Issue

If you encounter any problems or have suggestions for domains that should be added or removed, you can raise an issue:

1. **Open a New Issue**: Go to the [Issues](https://github.com/your-repository/issues) tab in this repository and click on "New Issue".
2. **Provide Details**: Include the domains you want to discuss and provide a short comment explaining why this domain is important or unwanted (why, what, who). Please ensure that you add a link to the dataset if you add duplicated domain.
3. **Submit the Issue**: Submit your issue and wait for feedback from the maintainers.

## Tags

As an *optional* extension, we use tags for enhancing the domains with metadata. You can find a list of the already existing tags [here](). If you want to add more unique tags then either generate a pull request or raise an issue. 

## License

This repository is licensed under the Apache-2.0 license. See the `LICENSE` file for more details.

## Contact

For any questions or concerns, please contact the repository maintainers on [discord]() or raise an [Issues](https://github.com/your-repository/issues).

---

Thank you for contributing to the improvement of multilingual language models!
