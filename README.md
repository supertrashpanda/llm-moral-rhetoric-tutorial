To classify United States congressional floor speeches based on if they contain **moral rhetoric** (yes = 1, no = 0)

Moral rhetoric, which frames the subject in terms of fundamental beliefs about right and wrong (Simonsen & Widmann, 2025), is a powerful tool for politicians to mobilize their co-partisans (Jung, 2020). Yet when politicians moralize their public speech, on which issues, and in what political contexts remain open questions.

An example:
> 🗣️ *“You have perverted the right of asylum, turned it into a system of mass immigration.”*
>
> — Alternative for Germany (AfD), 2018

Most extant studies measure moral rhetoric with dictionaries or word embeddings that score a text based on vocabulary, or with supervised classifiers that requires laborious human coding. LLMs, given their strong in-context learning capabilities, offer a promising alternative approach that can annotate texts with no or few labeled examples (i.e., **zero-shot** or **few-shot** learning). Empirically, we want to examine whether LLMs can reliably detect moral rhetoric in congressional speeches in this tutorial.

**We will walk through a minimal LLM annotation workflow:**

1. **Get the data**: download the Congressional Record and add each speaker's party ✅
2. **Prepare the text**: clean the texts and split them into paragraphs ✅
3. **Draw a validation set**: prepare a small validation set with hand-coded labels
4. **Write codebook and prompt**: as instructions to the LLM
5. **Zero-shot annotation**: ask the LLM using only the minimal prompt
6. **Few-shot annotation**: add a few labeled examples to the prompt
7. **Validation**: compare the LLM labels with human labels
