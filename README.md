# curated-web-data
A collection of "good and bad" Web domains for LLM pretraining data

## Types of Web domains

- **good**: Domains that can be used as seed for crawling and upsample for training
- **bad**: Unwanted content (noisy, spam, ads, adult, violence, pirate)
- **duplicated**: Dedicated and clean datasets exist (like Wikipedia, reddit, stackoverflow) - no need to use web crawls for these sources

## Data format

The domain types are collected in separate folders. Domains are stored in two column CSV files. The columns are as follows:

- **domain**: The Web domain name, use wildcard * to include subdomains, e.g. "*.wikipedia.org" for all language versions of Wikipedia.
- **comment** (optional): a human readible explanation why the domain is included.

The file name of the CSV files should reflect the language of the content and/or the original source if there is any. Use "multilingual" for multilingual content and "code" for programming languages. 
