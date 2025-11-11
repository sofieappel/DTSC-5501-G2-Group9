# Data Structures and Algorithms - Group Project 2
Group 9 - Sofie Appel, Isra Marcu, Abhirama Karthikeya Mullapudi, Erin Noonan

## Setup Instructions
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/DTSC-5501-G2-Group9.git
   cd DTSC-5501-G2-Group9
   ```
2. Explore results in Jupyter:
   ```bash
   jupyter notebook Group9_Final_Report_Notebook.ipynb
   ```

## Description of the Project and Summary of Results
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
* Returns height of the tree (maximum depth)
* Deletes node given its path.
* Prints summary of book.
* Searches for key word given input.

**Insights:**
This project demonstrates a practical use of the general tree structure. To be able to print the TOC in order, preorder traversal was the best method. Upon reflection, we decided to create a dictionary that would assign the sub-chapters to their chapter rather than the indexing method that was originally used.

### Q2:
We used the novel, The Adventures of Sherlock Holmes by Sir Arthur Conan Doyle. We obtained this text from Project Gutenberg and downloaded it directly in plain .txt format. There were many steps taken during the data preprocessing to ensure the rest of the code would run smoothly. All text was converted into lower case and all carriage returns, new lines, roman numerals, punctuation, special characters, digits, and multiple spaces were removed. Additionally we implemented stopwords as permitted and our text changed in length from 105,811 to 47,104 after stopword removal. 

**Findings:**
- Letter frequency is a multimodal distribution with ‘e’ being the most frequent and ‘z’ being the least frequent.
- Word frequency is unimodal with ‘said’ being the most frequent and the distribution flattened out towards the right with many words having similar low frequency rates, ‘never’, ‘nothing’, and ‘found’ are examples of this. 
- Bigram's distribution is unimodal with the top three bigrams including the word, ‘holmes’. 
- Trigram’s distribution is unimodal and showed more variety in words, however all top three phrases are referring to a character's name. 
- When comparing the bigrams and trigrams, the frequency of the least common bigram is just under 20 whereas the most common trigram is barely over 25. 
- Sentence length distribution is unimodal and right-skewed, with most sentences being shorter in length and there being few sentences with a lot of words. 

**Insights:**
Our analysis pipeline primarily runs in linear time with respect to the size of the text. The preprocessing and cleaning functions scan the text character by character, giving a time and space complexity of O(T) where T is the length of the text. Tokenization and stopword removal each operate once per word with constant-time lookups, resulting in O(n) time and space complexity, where n is the number of tokens.

Frequency counting for letters, words, and n-grams uses hash-based structures (Counter), maintaining O(n) time and O(u) space complexity, where u is the number of unique tokens. Sentence analysis, including splitting and length computation, also scales linearly with text length (O(T)).

Overall, our approach is efficient, performing single linear passes through the data and avoiding nested or quadratic loops. This ensures the entire pipeline runs in O(T) time, making it scalable for large texts like full novels while maintaining practical runtime and memory usage.

## Roles
As a group we focused on open communication, leading to great collaboration and a focus on each of our individual strengths. Using an iMessage group chat as our form of communication allowed us to stay in contact with one another, schedule Zoom meetings, and plan when to meet in person. We were intentional with each other's time and present when we met to work together.

For both questions, we met as a group to decide on the technical book and novel to be used in our project and allocated parts of the project within our group. Question 1 was Sofie and Isra’s focus, while Question 2 was Erin and Abhirama’s focus.  

**Roles and Contributions:**

- **Sofie Appel:**  
  - Worked on the insert function for Question 1.  
  - Developed the `print_toc` and depth functions for Question 1.  
  - Took the lead on the write-up for Question 1.  

- **Isra Marcu:**  
  - Worked on the insert function for Question 1.  
  - Developed the traversal and height functions for Question 1.  
  - Took the lead on the write-up for Question 2.  

- **Abhirama Karthikeya Mullapudi:**  
  - Created the technical book in the notebook by iterating through chapters, sub-chapters, and sub-sub-chapters.  
  - Worked on showcasing the different methods implemented inside the TOC tree in Question 1
  - Worked on letter analysis and bonus sentence analysis for Question 2.  

- **Erin Noonan:**  
  - Focused on preprocessing functions, word analysis, bigram, and trigram analysis for Question 2.  
  - Assisted with testing and validation of various code components for both questions.
  - Assisted with time complexity explanations in write-ups.

All the group members have worked together to build the additional search, delete and summary functions in Question 1. 

Together we all focused on making sure everyone was comfortable with their workload and felt like they were contributing fairly, being able to give their best work.

