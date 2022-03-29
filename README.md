# BookGenerator
Generate realistic book titles for an author using the GPT-2 generative model.

## Abstract

Artists can have a particular way of naming their creations (movies, books, music albums, or song titles...) 
and it is common to sometimes feel that some of those titles remind you of
a particular author, maybe because they follow a similar style, or because the topics are already familiar. 
Hence, we present a system capable of generating non-existing book titles for a given
author, following a similar style and topics that feel like books that the author could have written.


## How it works

By fine-tuning a GPT-2 model using the publicly available [GoodReads dataset](https://www.kaggle.com/datasets/b2dde9353c9d10c36e4d6b593a74c109dbaca6393a1ca0f2c7abafeba7633641),
we create a model with the ability to generate realistic sounding book titles. 
Our pre-trained model can be downloaded [here](https://drive.google.com/file/d/1CEVqW_-dGhuRDFqwHwGEp_ISzrIqQHub/view?usp=sharing).
Then, by feeding a list of already published book titles of an author, the model is used to generate new entries in that list, thus
generating similar titles to those fed. The same GTP-2 model is used to calculate similarity to already existing titles of that 
author by averaging word embeddings of the existing/generated titles.

A list ordered by similarity is returned as the output.


## Examples

Book titles for **George Orwell**

- **Simil.	Generated title**
- 0.68	The Life And Times Of Aldous Huxley
- 0.67	The Postal Service's Official Tales
- 0.67	Journey to the Bottom
- 0.63	Truth, Liberty, and Equality
- 0.62	Audacity, Simplicity, and Greatness
- 0.59	A Christmas Carol
- 0.56	Uncle Tom's Cabin
- 0.54	Analysis of Comparative Literature
- 0.47	Royal Wedding
- 0.46	Black Knights

Book titles for **Noam Chomsky**

- **Simil.	Generated title**
- 0.73	The American Dream: From The Harlem Renaissance to the Vietnam War
- 0.71	We the People: Ten Underclass Struggle to Reclaim Our Democracy
- 0.70	About the Leader: The Politics of a Genuine Nation
- 0.69	A Short History of Psychology
- 0.67	A Colorful and Revolutionary Story
- 0.63	Estatehood: Federalism, Labor and Labor History
- 0.60	Socialism: Political and Economic Interpretation
- 0.57	The Shadowlands
- 0.43	Crossing Souls
    
    
## Extra
An unpublished paper is included [here](https://github.com/AgiBla/BookGenerator/blob/main/Report.pdf) explaining the technical capabilities of our system.
