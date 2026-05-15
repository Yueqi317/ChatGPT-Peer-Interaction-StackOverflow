# The Impact of ChatGPT on Peer Interaction in Stack Overflow Question Threads

**Author:** Yueqi Sun

## Research Question

Does the release of ChatGPT reduce observable peer interaction (commenting activity) on Stack Overflow, and is this reduction stronger for questions that are highly substitutable by AI?

## Data Description

This project extracts and structures data from two Stack Exchange communities – **AI Stack Exchange** (`ai.stackexchange.com`) and **Russian Stack Exchange** (`rus.stackexchange.com`) – covering the period from January 1, 2021 to December 31, 2023. The dataset includes:

- **Questions** (post type 1) with metadata: creation date, body text, tags, owner user ID, score, and accepted answer ID.
- **Answers** (post type 2) linked to their parent questions, including acceptance status.
- **Comments** attached to questions or answers, with inferred question-level linkage.
- **Users** (only those appearing in the filtered posts/comments) with their reputation scores.

The data enables analysis of commenting activity before and after the release of ChatGPT (November 2022), allowing tests of whether AI‑substitutable questions experience a greater decline in peer interaction.

## Data Source

**Source:** [Stack Exchange Data Dump](https://archive.org/details/stackexchange) – a free, anonymized snapshot of all Stack Exchange public content.

The raw XML files used are:

- `Posts.xml`
- `Comments.xml`
- `Users.xml`

For this project, two specific communities were selected:
- `ai.stackexchange.com` (the AI‑focused community)
- `rus.stackexchange.com` (a non‑AI, general‑purpose Russian language community, serving as a control)

## How to Run the Code

### Prerequisites

- Python 3.8+
- Required packages: `pandas`

Install dependencies:

```bash
pip install pandas
