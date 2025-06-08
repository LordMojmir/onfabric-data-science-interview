## Fabric's user understanding challenge

Congratulations on being selected for this take home interview! The goal of this challenge is to see how you approach problem solving, especially when the “best practice” approach isn’t clear. We don’t want to constrain your thinking, so feel free to solve this challenge with any tools you deem appropriate.

### Few guidelines

1. Don’t spend more than a couple hours on this, we really just want to see how you **approach problem solving**. Not all experiment's work out, so if the output of your work isn’t great, you can find comfort in the fact we just want to **see the process**! Don’t start again from scratch, you’ll be wasting your time.
2. We value **clean code** and **clear explanations** as much as the actual solution to the challenge. Include the cell outputs of the Jupyter notebook in the final commit. We will not execute your solution so make sure the notebook clearly shows the **output of your work**.
3. We value **creativity**. If undecided between two approaches, go with the most surprising one.
4. Provide **any additional context** you think we may need to understand your approach on the notebook itself.

Apart from that, go for it! We’re excited to see what you build.

### Getting started

To get started, please clone this repo and check out the `challenge.ipynb` file. The file includes the challenge and a high level description of what we consider a **dummy** approach. Make sure your solution is **significantly** better that the dummy one.

### Submit your solution

When you’re happy with your solution, send us a link to your repo. If you don’t feel like making your repo public, make a private one and invite us:

- @jskerman
- @massimoalbarello

# My solution
## Solution overview (added by Mojmír Horváth)

We embed **both** user search queries and catalog items with the
`all-MiniLM-L6-v2` Sentence-Transformer and recommend the products whose
**maximum** cosine similarity across *any* of the customer’s searches is
highest.  This one-to-many scoring lets a single highly relevant query
surface niche items even if the rest of the history is noisy.

The notebook:
1. Cleans and embeds searches & descriptions.
2. Computes a full query×product similarity matrix.
3. Surfaces the top-12 items and a bar-chart of their scores.

All outputs are baked into the notebook so the reviewer can read it
without re-running heavy models.
## Installation
```bash
pip install -r requirements.txt
```