# Quora Duplicate Question

This is NLP project which aims to solve the problem of duplicate questions detection in Quora. Quora is famous website where users asks questions and other users tries to answer them. But many times similar question is being asked more then one times (and even 160 times! Yes there is question in dataset which is asked 160 times). 

![image](https://github.com/user-attachments/assets/99feb145-4ee1-494d-b5f8-f969a2b7c7c8)


These duplicate questions affects the user experience in negative way. Our goal is to detect the duplicate questions so that all the related answers can be found at one single place. 

![image](https://github.com/user-attachments/assets/447704fc-55ee-4985-b957-1fedf18e869f)


Two similar questions are merged together.

## Dataset

The dataset contains around 4 Lac plus questions, which are labelled as ‘duplicate’ and ‘not duplicate’. You can access the dataset from [here](https://www.kaggle.com/competitions/quora-question-pairs/data). Here is an overview of test dataset. 

| id | qid1 | qid2 | question1 | question2 | is_duplicate |
| --- | --- | --- | --- | --- | --- |
| 0 | 1 | 2 | What is the step by step guide to invest in share market in india? | What is the step by step guide to invest in share market? | 0 |
| 1 | 3 | 4 | What is the story of Kohinoor (Koh-i-Noor) Diamond? | What would happen if the Indian government stole the Kohinoor (Koh-i-Noor) diamond back? | 0 |
| 2 | 5 | 6 | How can I increase the speed of my internet connection while using a VPN? | How can Internet speed be increased by hacking through DNS? | 0 |
| 3 | 7 | 8 | Why am I mentally very lonely? How can I solve it? | Find the remainder when [math]23^{24}[/math] is divided by 24,23? | 0 |
| 4 | 9 | 10 | Which one dissolve in water quikly sugar, salt, methane and carbon di oxide? | Which fish would survive in salt water? | 0 |
| 5 | 11 | 12 | Astrology: I am a Capricorn Sun Cap moon and cap rising...what does that say about me? | I'm a triple Capricorn (Sun, Moon and ascendant in Capricorn) What does this say about me? | 1 |
| 6 | 13 | 14 | Should I buy tiago? | What keeps childern active and far from phone and video games? | 0 |
| 7 | 15 | 16 | How can I be a good geologist? | What should I do to be a great geologist? | 1 |
| 8 | 17 | 18 | When do you use ã‚· instead of ã—? | When do you use "&" instead of "and"? | 0 |

## Solution

This problem can be solved either by using Machine Learning solutions or by Deep Learning. But as this dataset is very huge and it takes significant amount of time and power to train a model, i have to train this model on my local machine so i used Machine Learning approach.

I have utilized `Xgboost` classifier and `RandomForestClassifier` models as main algorithms.
