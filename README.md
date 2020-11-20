# Writer's Help

Building AI course project

## Summary

An accidental writer needs often help to create a meaningful text. AI could offer a relevant proposal for the substance, in the form of word-groups, which other writers have favored in similar situations.

## Background

Nowadays people have to be an ability to write presentations, blogs, temporary instruction guides, and so on, but occasionally. We are not professional writers. Anyhow, to give some value to the readers, it would be nice if our texts incorporated relevant thoughts about the subject. Meaningful thoughts became with right words. Of course, it is possible to go through with earlier-written text masses oneself, make notes, and so on. However, this good old way is time-consuming and burdensome. It would be very nice to get some help at this point.

## How is it used?

When a user needs to write a job-oriented text, she or he can pick the text-type, and give a title, some key words, or both. Then the solution will offer some groups of words, which it presumes to find in that kind of text. In the ideal case, selected suggestions are picking up valid topics, and furthermore common terms to describe these clearly.

## Data sources and AI methods

The solution will do clearly the text analysis. For that, it will need data corpora. One is a general text corpus of the used language, with the occurrence information of words. Hopefully this would be available from some source, either free or for money. The other is the corpus of the specific text type, the one where to a user want to add her or his contribution. If many kinds of text types is to be supported, each one needs its own corpus, or the corpus has to be classified for that. Anyhow, this is a corpus (or corpora), which you need to collect yourself. Better suitability means better accuracy.

First task is some sort of lemmatization of your own corpus. The trial and error will tell what the most promising level to do that is.

Next, the solution should find the popular words of your corpus that are not so widespread universally by comparison with a more general text corpus. This is for to cast out pronouns and the most common verbs etc. The method for that is still in search.

It is enough to do two first steps once. It creates the basic for the actual analysis. Of course, they can and should be repeated, if there is a place for a bettering.

Now it is a time to use key words of the current text to be written. With them, the solution is to find which words in your corpus are close ones. Quite literally, it will pick up texts including given key words, and try to find out typical words just for them. The phase is very similar to the one that earlier hunted meaningful terms of your whole corpus. Therefore, same type a method is a candidate also for that.

Results will be given as lists of words. Each one of key words are united with the own list of proposed relative terms.

## Challenges

The goodness of result is very dependent from data. If used corpus is a collection of garbage as a form of texts, the solution will recommend waste.

Weak points of the solution might be hard to fathom, if it does give something that may be reasonable. Evaluation and evolution is a challenge, because hoped results have been defined so softly.

Anyhow, the main job is still for a human to do. She or he is to write. AI won't do it awhile.

## What next?

There are many blank spots in the project. It requires a closer look to the techniques that someone has already invented, and specific methods to use. The check for the approach to the issue would be good. Is the idea how sound after all? Collecting answers to these questions will help the general understanding of the problem, and probably cause minor and major modifications.

## Acknowledgments

The [Elements of AI](https://www.elementsofai.com/) Team for giving a push to think about the subject.
