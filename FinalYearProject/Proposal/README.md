---
title: "Campus Companion - University chatbot"
seoTitle: "Developing a ChatBot using LangChain and GPT-3.5 Turbo"
seoDescription: "Developing a chatbot using LangChain, OpenAI GPT-3.5 Turbo LLM, Pinecone and a website to reply the chatbot to"
datePublished: Fri Oct 13 2023 14:52:22 GMT+0000 (Coordinated Universal Time)
cuid: clnoq9j0j000u08l6az8fd8vc
slug: campus-companion-university-chatbot
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697195752276/93313f5e-d048-4e05-a4bc-3ce19ac14f8b.png
tags: chatbot-development, finalyearproject, llm, pinecone, langchain

---

# Introduction

Hi everyone! Today I will be embarking on my journey of developing a chatbot for my Final Year Project. It will be predominantly targeted to students enrolled on a course at the University of Birmingham, however, this is only the beginning so it may change as I dive deeper. In this blog series, I will take you through my journey in developing this chatbot and I invite you to join me on this adventure.

# Project Aim

I have not completely finalised my project idea yet but it will be capable of responding to inquiries regarding the University's rules and regulations as well as details about the School of Computer Science.

I was also thinking of integrating other Schools as well but I am not sure how feasible this may be as I am still in early stages.

After conducting a questionnaire I gathered information from many students at the University studying a broad range of courses that a chatbot would be beneficial to them not only academically but also administratively.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697043741036/301dff0a-8598-4e59-9cb1-42709b606521.png align="center")

# Project Objectives

1. User Interface - simple website to deploy chatbot to with clear UI so those with limited technology experience can navigate it effortlessly
    
2. Return an appropriate response - an answer from the chatbot should be accurate whilst also not being too long
    
3. Data fetching mechanism - Users will be able to store their past conversations and go back to them at a later date at their convenience
    
4. Future Recommendations - Create a separate space for students to leave any comments or improvements they wish to see
    

# Architectural & Model Selection

There are many frameworks and LLM to choose from for developing a chatbot in Python.

## Choice of Framework

After weighing out several different frameworks including Haystack, LlamaIndex, I settled on using LangChain.

LangChain facilitates NLP applications like question answering systems which would be ideal for a chatbot. There are also many modules within LangChain, some of which I have mentioned below:

1. Memory - this gives the LLM access to the conversation history so each response will be tailored based on the previous question asked
    
2. Indexes - contains utility functions enabling integration of vector databases which is useful for allowing document retrieval and real-time updates
    
3. Chains - the idea of composing components together in a chain simplifying and making the implementation of the chatbot modular, so easier to debug and maintain (probably the most important point)
    

There are also further useful features such as *ConversationChain* and *ConversationSumaryMemroy* but I will talk more about these during the development stage when I am coding.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697043683146/01899b4f-aa84-41ab-af4c-23e88e9bbba3.png align="center")

## Choice of Large Language Model

There are also numerous LLMs available some being free, and others being paid so it is important to choose the appropriate one for developing a chatbot. Some examples are PaLm2 by Google, Llama2 by Meta and GPT-3.5 Turbo & GPT-4 by OpenAI.

An experiment was conducted between PaLm2 vs Llama2 vs GPT-4 to see which model performs the best. I will save you the time without diving into the specific details and the tests conducted, the end result was that GPT-4 was the most impressive. Each model had a strong suit in a particular set of areas but GPT-4 consistently provided a good answer even when the other models' output was close to useless.

### GPT-3.5 Turbo

The GPT-4 model is very capable and advanced, however, it comes at a price. The GPT-3.5 Turbo model has similar capabilities as that of GPT-4, is also the flagship model and is much more cost-effective. After reading many reviews online, the GPT-3.5 model appears to be highly efficient and would be well suited to my chatbot. GPT-3.5 Turbo is a slightly older model and has demonstrated strong performance in numerous NLP tasks making it reliable and well established.

Furthermore, GPT-3.5 Turbo has greater community support than other models simply because it has been around for longer which would help me as I am bound to face challenges during the development stage. Although GPT-4 is a more advanced model than GPT-3.5, it is not far behind and will, therefore, perform well as the LLM for my chatbot.

# Pinecone - Vector Database

An LLM can have many issues such as:

1. Hallucinations - provides false information to the user
    
2. Context Limit - amount of text that can be fed into LLM
    
3. Slow Response Time - more text fed into LLM means higher latency so slow response time
    
4. Knowledge Updates - LLM is not going to be able to keep up with a database that is regularly updated
    

I aim to use Pinecone vector database to address these issues.

In order to keep the LLM up to date, we need vectors. A vector is the numerical data that retains the semantic meaning. This means that when the chatbot is queried it will be able to find relevant chunks of information based on these vectors.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697151088960/2005d539-0fd3-4ce8-aa77-ee6e686188ba.png align="center")

## Summary

LangChain is the best suited framework for my use case as it contains many useful modules and functions which are likely to lead to an increased traction for the chatbot. OpenAI’s GPT-3.5 Turbo is the LLM I have selected to use as it is not only the most cost effective, but it is also OpenAI’s flagship model. It will operate seamlessly with LangChain, alongside Pinecone as the vector database to ensure the chatbot does not return false information by keeping the data up to date.

# Methodologies

I will not outline my methodology in detail here otherwise it might get boring very quickly.

Below is a vague list of steps I aim to carry out for the entire project.

1. Project Definition
    
2. Data Collection
    
3. Designing the chatbot's UI
    
4. Designing the website's UI
    
5. Developing the chatbot
    
6. Developing the website to host the chatbot
    
7. Enhancing the UI
    
8. Testing and Validation
    
9. Deployment
    
10. Maintenance
    

This is only the beginning of my journey in developing this chatbot and I hope you can follow along as I continue to share the steps I take.

If anyone has any questions or comments, please do not hesitate to reach out to me on any platform. Your feedback and support mean a lot as I embark on this adventure.

Thank you 🙂