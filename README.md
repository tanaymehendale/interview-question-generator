# Interview Question Generator (RAG)

This project is a Retrieval-Augmented Generation (RAG) system that generates high-quality interview questions using only a candidate’s resume as evidence.

The system indexes a resume once, retrieves the most relevant experience, project, and skills context at query time, and generates grounded interview questions with cited evidence.

## Problem Statement

Interview preparation is often generic and unstructured. Candidates struggle to practice questions that are truly aligned with their own experience.

Most AI tools hallucinate details or ask shallow questions that do not reflect real resume content.

This project solves that problem by generating interview questions strictly grounded in the resume itself.

## Solution

 - Resume is ingested once and stored in a vector database.
 - At query time, relevant resume chunks are retrieved.
 - A single LLM prompt generates interview questions using only retrieved evidence.
 - Every question cites the resume chunks it was derived from.
 - If information is missing, the system explicitly calls it out instead of guessing.

## Tech Stack
 - Python
 - Google Gemini API
 - LangChain
 - Pinecone Vector Database
 - Google Colab

## Future Enhancements

 - Job description alignment.
 - UI using Streamlit or React.
 - Confidence scoring per question.
 - Resume gap detection.
 - Multi-resume support.