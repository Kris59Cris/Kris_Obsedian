---
Core: AI
Focus: NLP
Type: Metric Table
---
a.k.a **Bilingual Evaluation Understudy**
_______________________________________________________
Candidate text: NLP generated translation
Reference text: Reference translation answer
_______________________________________________________
Methods:

1. **N-Gram Precision:** It calculates how many word sequences (n-grams, typically from 1 to 4) in the candidate text match the reference text
2. **Modified Precision (Clipping):** To prevent systems from inflating scores by repeating a common word endlessly, word counts are clipped to the maximum frequency found in the reference


Modified n-gram precision
1. Take 2-gram as example, let say the first 2-gram chunk
2. Count matching frequency of 2-gram across all  Reference texts
3. Select Max matching frequency across all reference texts (Max-ref)
4. Clipping ==> select Min of the 2-gram matching frequency between Candidate text & Max-ref
5. Repeat steps 1-4 for the remaining 2-gram chunks
6. 2-gram precision = sum of all 2-gram chunks clipped / number of 2-gram chunks in Candidate text
_______________________________________________________

Advantages:
1. Fast + simple to calculate
2. Widely acknowledge

Disadvantages:
1. Does not consider meaning
2. Does not incorporate sentence structure (Sub + Verb + Obj)
3. Hard to compare between different tokenizers
	- Sub-word that can be split into `"cat"` → `["ca", "t"]`



_______________________________________________________
Base:
[[AI.base]]

Relevant Topics:
[[AI & Creative Writing]]