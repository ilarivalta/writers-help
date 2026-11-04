
# Writer's Help: Smart Keyword & Context Suggester

An AI-assisted topic and vocabulary suggestion tool designed to help non-professional writers discover domain-specific terminology and meaningful ideas for targeted writing tasks.

> **Course:** Building AI ([Elements of AI](https://www.elementsofai.com/))
> **Topic:** Natural Language Processing (NLP), Text Analysis, Keyword Co-occurrence

---

## Summary

Accidental writers—such as employees drafting occasional reports, guides, or blog posts—often struggle to structure their thoughts and select appropriate terminology. **Writer's Help** analyzes domain-specific text corpora to propose relevant clusters of words, helping writers uncover contextual themes and common vocabulary used by experienced authors in similar domains.

---

## Background

In modern workplaces, professionals across various roles are frequently required to write presentations, temporary instruction guides, internal documentation, and public blog posts. Most people are not professional writers, yet their text needs to deliver clear value to readers.

* **Problem:** Identifying the right concepts and domain terminology usually requires manually reading through extensive reference documents—a time-consuming and tedious process.
* **Impact:** Writers spend excessive time staring at blank pages or risk producing vague, unstructured documentation.
* **Goal:** Automate reference analysis to present writers with immediate, relevant word groups and topic suggestions tailored to their target genre or topic.

---

## How It Is Used

The workflow is lightweight and integrated directly into the drafting process:

1. **Input Setup:** The user selects a target text type (e.g., *Technical Documentation*, *Job Presentation*, *Internal Guide*) and inputs a tentative title, primary keywords, or both.
2. **Contextual Retrieval:** The system retrieves topic-adjacent word groups frequently present in high-quality reference texts of that category.
3. **Drafting Support:** The writer uses these vocabulary suggestions as conceptual prompts to structure paragraphs and adopt industry-standard phrasing.

---

## Data Sources & AI Methods

### Data Corpora

* **General Text Corpus:** A broad language dataset (e.g., Wikipedia dump or open language model corpus) containing word frequency distributions across standard language.
* **Domain-Specific Corpora:** Specialized text collections categorized by format or topic (e.g., technical guides, product launch presentations), collected to establish baseline vocabulary for specific writing tasks.

### Technical Pipeline

```
[ Domain Corpus ] ---> [ Lemmatization ] ---> [ TF-IDF / Frequency Scoring ]
                                                       |
[ User Keywords ] -----------------------------> [ Co-occurrence Search ]
                                                       |
                                               [ Output: Word Groups ]

```

1. **Preprocessing & Lemmatization:** Standardize input texts to base forms (lemmas) to group morphological variants.
2. **Specific vs. General Term Extraction:** Apply frequency filtering (such as **TF-IDF** or **log-likelihood ratio**) against the general corpus to eliminate stop words, pronouns, and ubiquitous verbs while isolating domain-specific terms.
3. **Contextual Co-occurrence Analysis:** When the user enters a keyword, the model identifies terms within the specialized corpus that statistically co-occur in the same document segments or sentences, returning structured candidate word clusters.

---

## Challenges & Limitations

* **Data Quality Dependency ("Garbage In, Garbage Out"):** Proposing useful vocabulary requires high-quality, cleanly curated domain corpora.
* **Evaluation Metrics:** Because quality is subjective, evaluating performance relies on soft human feedback and user acceptance rather than hard loss metrics.
* **Human-in-the-Loop:** The tool serves as an ideation assistant rather than an autonomous generator; the actual drafting remains entirely with the human writer.

---

## Future Roadmap

* [ ] Survey open-source NLP libraries (e.g., `spaCy`, `NLTK`, `scikit-learn`) for efficient lemmatization and TF-IDF implementation.
* [ ] Prototype a lightweight vector similarity search (e.g., Word2Vec or mini embeddings) to complement statistical co-occurrence.
* [ ] Develop a minimal web UI or browser extension for real-time word prompting.

---

## Acknowledgments

* **Elements of AI / Building AI Team** for structured guidance on project scoping and practical AI applications.
