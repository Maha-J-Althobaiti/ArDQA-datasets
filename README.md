## ArDQA datasets

ArDQA is a cross-dialect Arabic QA benchmark spanning three domains. Each domain provides parallel QA triples {context, question, answer} across five Arabic varieties: MSA, Egyptian, Gulf, Levantine, Maghrebi. The benchmark contains 8,150 QA triples overall and is designed for evaluation of cross-dialectal transfer in Arabic QA.

**Composition**

- **ArDQA-SQuAD**: Curated from Arabic-SQuADv2.0, then translated by native speakers into four dialects with manual span annotation to preserve one-to-one alignment.
- **ArDQA-Vlogs**: Colloquial lifestyle vlog transcripts --> QA construction --> dialect translations --> manual span annotation.
- **ArDQA-Narratives**: Cultural narratives and folklore from online videos, following the same pipeline as Vlogs, with longer, descriptive answers.

**Quality control**

Native speakers translated independently in every domain, cross-checked each other, and an expert adjudicated disagreements. Span consistency was validated (using answer-to-context length ratios) to maintain strict alignment across dialects.


## ArDQA format (SQuAD v2.0 JSON)

ArDQA follows the SQuAD v2.0 structure:

```text
root
├── data: [
│   ├── {
│   │   ├── title: string
│   │   └── paragraphs: [
│   │       ├── {
│   │       │   ├── context: string
│   │       │   └── qas: [
│   │       │       ├── {
│   │       │       │   id: string
│   │       │       │   question: string
│   │       │       │   is_impossible: boolean
│   │       │       │   answers: [
│   │       │       │       ├── { text: string, answer_start: int }
│   │       │       │       └── ...
│   │       │       └── ...
│   │       └── ...
│   └── ...
└── (optional) version: string
```










