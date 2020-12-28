## Power-Level-Scouter
# Automatic extraction of a character's power level from book/manga text/summaries.

A fun little winter break project inspired by SethTheProgrammer's [power scaling videos](https://www.youtube.com/watch?v=48haDEHpJEA&t=349s).

The goal is to create the __Dragon Ball Z Scouter__ that can measure the opponent's power level. Instead of using Ki readings as proxy, we will follow the most generalizable methodology used in the Power Scaling community: **Calcs**, or the Joules (energy) required to accomplish specific feats. Examples range from punching out a human, splitting rocks, vaporizing cities, exploding planets, and destroying universes. 

Given a select text, either plot summaries or raw dialogue, the pipeline will run as follows:

1. Use Spacy/BookNLP to identify entites and extract all entity-action pairs.
2. Create action-Joules cross walk using physics calculations (available database?)
3. Find top feat for each entity, compare within/between series. 

We will start with creating a fully working pipeline from DBZ plot summaries found on Fandom.org. 

12-28-20

TO DO:

- [ ] Scrape DBZ Fandom for chapter summaries
- [ ] Run NLP pipeline to identify entities
- [ ] Create preliminary heuristics to find entity-action pairs
- [ ] Validate an action-Joules dataset to use for Calcs
