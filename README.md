# Automated CI/CD Testing for LLMOps (gpt-3.5-turbo) : 
This repository contains code is a guide for automating testing using Continuous Integration/Continuous Deployment (CI/CD) pipelines for Language Learning Models (LLM). The primary goal is to evaluate the performance of the LLM-based quiz assistant by assessing its ability to generate accurate quizzes based on a given question bank.
where we can operationalize and manage large language models (LLMs) using `circleci`. In this guide, we’ll explore how to streamline the deployment and management of LLMs for real-world applications. Specifically, we’ll focus on gpt, one of the most powerful LLMs out there. 

## Overview
The code in this repository includes functionalities to automate the evaluation process of the quiz assistant. It utilizes a combination of Python modules and language models to generate quizzes and evaluate them against a predefined question bank. Overall, this script automates the evaluation of the quiz assistant application using predefined datasets, evaluation prompts, and language models. It generates evaluation reports to assess the performance and effectiveness of the quiz assistant in creating quizzes based on a given question bank.

## Methods for evaluating Large Language Models (LLMs)
When evaluating Large Language Models (LLMs), we need robust testing methods to ensure their reliability, safety, and performance. Let’s delve into two essential approaches:
- 1. Rule-based testing.
- 2. model-graded testing.

1. Rule-Based Testing
Rule-based testing relies on predefined rules or criteria to assess LLM behavior. Here’s how it works:
**Designing Rules**: Testers create a set of rules that define expected behavior. These rules can cover various aspects, such as grammar correctness, factual accuracy, or avoiding harmful content.  There are some methods established to check the model performance on Rule based testing.

2. Model-Graded Testing
Model-graded testing assesses LLM performance by comparing it to other models or human-generated responses. Here’s how it works:
**Evaluation Models**: Use an evaluation LLM (different from the LLM being tested) to generate reference responses. This code also contain another same `model` to measure the performance of the first model.
However, we can use both methods to Both rule-based and model-graded testing to ensure LLM reliability. Combining these approaches provides a comprehensive evaluation, addressing safety, accuracy, and creativity. As LLMs continue to evolve, refining testing methods remains an ongoing quest for the AI community.

## Dependencies
The following dependencies are required to run the code:

- `pandas`: Used for data manipulation and analysis.
- `python-dotenv`: Used for loading environment variables from a .env file.
Components
- `langchain`: for using LLM

The main components of the code include:
- `app.py`: The main script that orchestrates the automated testing process.
- `save_eval_artifacts.py`:  this script automates the evaluation of the quiz assistant application using predefined datasets, evaluation prompts, and language models. 
- `test_assistant.py`:  this script automates the testing process for the chatbot assistant application by defining evaluation functions and corresponding test cases. It helps ensure the reliability and effectiveness of the chatbot assistant's functionalities under various scenarios..
- `test_release_evals.py`:  this script facilitates automated testing of the quiz assistant's ability to generate valid quizzes. It evaluates the assistant's responses and ensures they meet the expected format and content requirements. The use of fixtures and test cases helps streamline the testing process and ensure the reliability of the quiz assistant.
- `quiz_bank.txt`: Contains the data set in the quiz format.



## Risks of LLMs in Real-World Applications
While LLMs are impressive, they come with risks:
- **Bias Amplification**: LLMs may produce biased or discriminatory outputs.
- **Hallucination**: They might inadvertently generate incorrect or misleading information. There could be Inaccurate Information, Accurate but Irrelevant or misleading or nonsensing reply. In this guide, we use the some `Prompt Engineering` to analyse all these inaccuracies.
- **Prompt Injection**: Bad actors could exploit LLMs to create harmful content.
- **Ethical Concerns**: Using LLMs raises questions about accountability and responsibility for their output.

## Customized Quiz Generation Guide
Welcome to the Customized Quiz Generation Guide! In this README, we’ll walk you through the process of creating personalized quizzes based on user-defined categories. Whether you’re an educator, a student, or just someone curious about trivia, follow these steps to generate engaging quizzes.

## Overview
- **User Input**: The user provides a category (e.g., Geography, Science, Art) for which they want to create a quiz.
- **Subject Selection**: Based on the chosen category, select up to two subjects from the provided quiz bank.
- **Question Generation**: Generate three quiz questions related to the selected subjects using facts from the quiz bank.

## Steps
### Step 1: Identify the Category
First, identify the category the user is interested in. The available categories are:
 - Geography
 - Science
 - Art

### Step 2: Choose Subjects
Next, determine the subjects within the chosen category. Refer to the quiz bank below for a list of available topics:
- Quiz Bank
{quiz_bank}

- End Quiz Bank
Select up to two subjects that align with the user’s category.

### Step 3: Generate Quiz Questions
Using the selected subjects, create three quiz questions. Remember the following guidelines:

Only include questions related to subjects in the quiz bank.
Use explicit string matches for category names. If the category doesn’t exactly match Geography, Science, or Art, indicate that you don’t have information on that subject.
### Quiz Format:

- Question 1: <question 1>
- Question 2: <question 2>
- Question 3: <question 3>

**Additional Notes**: Students only know answers from the quiz bank, so focus on those topics.
Be creative and informative while crafting questions.




## Quiz Evaluation Guide

As an evaluator, your task is to assess the quality of quizzes generated by the quiz assistant. You'll focus on ensuring that the quizzes adhere to the available facts in the question bank. Let's dive into the evaluation process:

## Quiz Data

Here's the data you'll be evaluating:

- **Question Bank**: The set of available facts that the quiz assistant can reference.
- **Quiz**: The generated quiz based on user input.

## Example Quiz Questions

Subject: <subject>
Categories: <category1>, <category2>
Facts:
- <fact 1>
- <fact 2>

## Evaluation Steps

1. **Review the Question Bank**: Familiarize yourself with the available facts. These are the only valid references for the quiz.
2. **Compare Quiz Content**: Analyze the quiz questions and compare them to the question bank.
3. **Ignore Grammar and Punctuation Differences**: Focus on content alignment.

## Decision and Explanation

Make a clear decision and provide a brief explanation:

- **Decision**: Yes or No (Does the quiz only reference information from the context?)
- **Explanation**: Summarize your reasoning for the decision, referencing facts from the question bank if applicable.

For instance:

************
Decision: Yes
************
Explanation: The quiz accurately reflects information from the question bank, ensuring alignment.

Remember, factual accuracy is crucial. Let's maintain high-quality quizzes! 🚀


