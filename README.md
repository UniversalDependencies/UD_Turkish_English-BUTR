# Summary

UD_Turkish_English-BUTR is a treebank of Turkish-English code-switched sentences collected from Boğaziçi University students, annotated in the Universal Dependencies framework to provide a standardized resource for analyzing syntactic patterns in Turkish-English code-switching.

# Introduction

The UD_Turkish_English-BUTR treebank contains annotated Turkish-English code-switched sentences collected from Boğaziçi University students. The term "Boğaziçi Turkish" refers to the variety of Turkish influenced by English commonly spoken by Boğaziçi University students and characterized by frequent code-switching. This linguistic phenomenon, sometimes referred to as "Boğaziçi Tarzancası" (Boğaziçi Tarzan-speak) in informal settings, represents a distinct sociolinguistic practice that has remained largely unexamined in the linguistic literature.

The treebank was developed using a semi-automated annotation pipeline within the Universal Dependencies framework. The process began with preliminary annotation using the language model Claude 3.5 Sonnet, followed by manual verification and correction by four annotators using ArboratorGrew. The annotation scheme aligns with existing Turkish UD treebanks while incorporating necessary adjustments for code-switching phenomena, particularly in head assignment within mixed-language constructions.

Qualitative analysis of the treebank reveals distinctive code-switching patterns, including English verbs with Turkish auxiliaries, academic terminology, and pragmatic expressions. A notable pattern is the morphological integration of English verbs into Turkish syntax, exemplified by constructions like "drop-bylayacağım" ("I will drop by"), where English phrasal verbs receive Turkish morphological markers.

The Universal Dependencies analysis demonstrates three key syntactic patterns in Boğaziçi Turkish: preservation of Turkish syntactic structure with English lexical insertions, morphological adaptation of English verbs, and code-switching at specific syntactic boundaries.

The treebank captures three main contact phenomena:

* **Code-switching (CS):** Full English phrases or clauses embedded in Turkish discourse, both intrasentential and intersentential.
* **Lexical adaptation (LA):** English words integrated with Turkish morphology, such as "drop-bylayacağım" ("I will drop by") or "overthinkledim" ("I overthought").
* **Loan translation (LT):** Calques of English expressions using Turkish lexemes, such as "toplantı almak" (loan translation of "to get a meeting").

Each sentence is annotated with the following comment-level metadata:

* `# type` — Primary contact phenomenon (CS, LA, or LT)
* `# text_en` — English translation
* `# medium` — Communication medium (Written or Spoken), where known

Token-level language identification is provided via `Lang=tr` / `Lang=en` in the MISC column. Morpheme-level code-switching boundaries are marked with `CSID=MIXED` and `CSPoint` features.

This treebank provides a standardized resource for analyzing syntactic patterns in Turkish-English code-switching, facilitating further research in computational linguistics.

# Acknowledgments

We would like to express our gratitude to all the Boğaziçi University students who participated in our survey and provided examples of code-switched sentences for this treebank. Their contributions were essential for capturing authentic instances of Turkish-English code-switching patterns.

We thank the Universal Dependencies community for their guidelines and support during the annotation process. Special thanks to the ArboratorGrew team for providing the annotation platform that facilitated our collaborative work.

We also acknowledge the contributions of Claude 3.5 Sonnet in the preliminary annotation phase, which helped streamline our workflow and allowed the annotation team to focus on refining and validating the dependency structures.

This work was conducted as part of a research project at Boğaziçi University, with support from the Departments of Linguistics and Computer Engineering. We appreciate the academic environment that encouraged this interdisciplinary collaboration between computational and sociolinguistic approaches to the study of code-switching.

## References

* Nivre, J., et al. (2020). Universal Dependencies v2: An evergrowing multilingual treebank collection. In Proceedings of the 12th Language Resources and Evaluation Conference. European Language Resources Association.
* Guillaume, B., et al. (2021). Grew-match: An online tool for comparative corpus queries and quantitative analyses of UD treebanks. In Proceedings of the Fourth Workshop on Universal Dependencies.
* Anthropic (2024). Claude 3.5 Sonnet [Large Language Model]. https://www.anthropic.com/claude

# Changelog

* 2026-05-15 v2.18
  * Added 7 new sentences (52–58), expanding the treebank to 58 sentences.
  * Added English translations (`# text_en`) to all sentences.
  * Added missing PronType features to all PRON and DET tokens.
  * Added Polarity=Neg/Pos to existential predicates (yok/var), aligning with UD_Turkish-GB and UD_Turkish-TueCL conventions.
  * Fixed punct head attachment errors (sents 1, 35).
  * Fixed Case=Nom → Case=Equ for equative pronouns (sent 9).
  * Fixed deprel errors: nmod → amod for participial adjectives (sent 45), obj → conj for coordinated objects (sent 50).
  * Added Mood=Ind to finite English verbs (sents 50, 51).
  * Fixed ADP deprel: compound → case for "on" in PP constructions (sent 6).
* 2025-05-15 v2.16
  * Initial release in Universal Dependencies.

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.16
License: CC BY-SA 4.0
Includes text: yes
Parallel: no
Genre: spoken social
Lemmas: manual native
UPOS: manual native
XPOS: not available
Features: manual native
Relations: manual native
Contributors: Akkurt, Furkan; Teker, Nursena; Binici, Helin; Demir, Ahmet; Sampanis, Konstantinos
Contributing: here
Contact: furkan.akkurt@bogazici.edu.tr
===============================================================================
</pre>
