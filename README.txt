"topicextractor" extracts topic keywords from documents based on 'TF-IDF' algorithm.

"pip install topicextractor"

Example for usage
=======================================================================
import topicextractor as te

sample_docs = [["doc1_str"], ["doc2_str"], ["doc3_str"] ....]

#preprocessing data
count_container = te.extract_noun_counts(sample_docs)
print(count_container)
>>[{"a": 3, "b": 2}, {"c": 5, "d":3}, {"e": 7, "f": 12} ....]

#extract keywords for 'count_container[0]'
keywords = te.tfidf(count_container[0], count_container)
print(keywords)
>>[("keyword1", 2.1104),("keyword2" 2.0012),("keyword3", 1.8892) ....]

=======================================================================

The number next to the keyword is 'tfidf' value and the greater the value, the stronger the keyword reflects the topic.
Thanks, and please contact the author via e-mail for any comment.