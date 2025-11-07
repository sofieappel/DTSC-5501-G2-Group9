# Data Structures and Algorithms - Group Project 2
Group 9 - Sofie Appel, Isra Marcu, Abhirama Karthikeya Mullapudi, Erin Noonan

## Setup Instructions
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/DTSC-5501-G2-Group9.git
   cd DTSC-5501-G2-Group9
   ```

2. Run the main script or notebooks:
   ```bash
   python src/Core_Code.py
   ```

3. Explore results in Jupyter:
   ```bash
   jupyter notebook Final_Report_Notebook.ipynb
   ```

## Summary of Results
### Q1: 
We implemented a hierarchical Table of Contents (TOC) tree that mirrors the structure of the book, Pattern Recognition and Machine Learning by Christopher M. Bishop. Each node in the tree represents a chapter, subchapter, or sub-subchapter. 

**Features:**
* Implements Node and Book classes
* Inserts new nodes based on the path [chapter, subchapter, sub-subchapter]
* Performs Preorder Depth-First Search to print and search the structure. 
* Prints TOC using three modes:
  * Titles only
  * Indented
  * Numbered 
* Returns depth of node given node title
* Returns height of the tree (maximum depth

**Insights:**
This project demonstrates a practical use of the general tree structure. To be able to print the TOC in order, preorder traversal was the best method. Upon reflection, we believe we could improve the insert tests by creating a dictionary that would assign the sub-chapters to their chapter rather than the indexing method that was used.

### Q2:
We used the novel, The Adventures of Sherlock Holmes by Sir Arthur Conan Doyle. We obtained this text from Project Gutenberg and downloaded it directly in plain .txt format. There were many steps taken during the data preprocessing to ensure the rest of the code would run smoothly. All text was converted into lower case and all carriage returns, new lines, roman numerals, punctuation, special characters, digits, and multiple spaces were removed. Additionally we implemented stopwords as permitted and our text changed in length from 105,811 to 47,104 after stopword removal. 

**Findings:**
Letter frequency is a multimodal distribution with ‘e’ being the most frequent and ‘z’ being the least frequent.
Word frequency is unimodal with ‘said’ being the most frequent and the distribution flattened out towards the right with many words having similar low frequency rates, ‘never’, ‘nothing’, and ‘found’ are examples of this. 
Bigram's distribution is unimodal with the top three bigrams including the word, ‘holmes’. 
Trigram’s distribution is unimodal and showed more variety in words, however all top three phrases are referring to a character's name. 
When comparing the bigrams and trigrams, the frequency of the least common bigram is just under 20 whereas the most common trigram is barely over 25. 
Sentence length distribution is unimodal and right-skewed, with most sentences being shorter in length and there being few sentences with a lot of words. 

**Insights:**
All preprocessing steps required going through each character in the text thus having a time complexity of O(n) for each of these steps respectively. In contrast when counting this has a time complexity of O(n^2) because each item must be checked against the entire document. 
The preprocessing was very important to the success of this project as having clean data allowed counting to be more simple and accurate. 

## Roles
As a group we focused on open communication leading to great collaboration and a focus on each of our individual strengths. Using an iMessage group chat as our form of communication allowed us to stay in contact with one another, schedule zoom meetings, and plan when to meet in person. We all were intentional with each other's time and present when we met to work together. 

For both questions, we met as a group to decide on the technical book and novel to be used in our project and allocated parts of the project within our group. Question 1 was Sophie and Isra’s focus while question 2 was Erin and Abhirama’s focus. However Abhirama was able to create the technical book in our notebook by iterating through chapters, sub chapters, and sub-sub chapters. For question 1, both Isra and Sophie worked on the insert function. Further for question 1, Sophie worked on the print_toc and the depth functions while Isra worked on the transversal and the height functions. For question 2, Abrihama worked on the letter analysis and bonus sentence analysis. Erin focused on the other aspects of question 2, working on the preprocessing and bigrams/trigrams. Once we realized question 2 seemed to be more intensive we allocated some more “soft-skills” work to Isra and Sophie. Sophie took the lead on the write-up for question 1 and Isra took the lead on the write-up for question 2 getting help from Abrihama and Erin regarding the time complexity. We all worked on testing as a group, testing various parts of the code.

Together we all focused on making sure everyone was comfortable with their workload and felt like they were contributing fairly, being able to give their best work.  

