# ElmTA_project

This repository contains code for the ElmTA app. This app uses ChatGPT to respond to elementary school student questions in an easy to interpret manner. In response to the challenges faced by educators in providing individualized support to students in elementary education, there is a growing interest in exploring the implementation of chatbot assistants as a means to alleviate the burden on teachers and enhance the quality of education. This project aims to explore the design considerations, development processes, and functionality requirements necessary for creating a chatbot assistant optimized for young students.

## Problem Statement - what the problem is from the customer's perspective

Elementary School teachers need additional support to ease the stress of teaching and reduce the burden each individual student may take, in order to provide higher quality education.

## Solution - what your tool/product/model does to solve the customer's problem

ElmTA is a python implementation I designed that utilizes speech to text as well as text to speech to interact with young students. It utilizes OpenAI's gpt-4, whisper-1, and tts-1 to interpret what a student says and speak back to them. This extra assistance by ElmTA aims to reduce the burden on teachers by giving easy to understand explanations when the teacher is unavailable.

## Demo 

<video src="ElmTa-v1-demo3.mp4" width="720" height="480" controls></video>

~ 8 min demo video showing a few sample runs of the code

### Assumptions, Constraints & Implications - what assumptions you're making, any constraints that you're dependent on, and what implications your solution results in

I assume that the student can ask their question in the provided time. This code also requires an openAI API access key to be able to use. It assumes that we are working in English. It assumes that the recorded audio and generated audio do not be saved for future use. This version of the application is not product ready yet, just proves functionality. This all assumes we can access OpenAI and have a key to use their more advanced models. 

### How your solution was built - what data you used, feature learning you applied, and model you trained

By utilizing gpt-4, the model is already pretty smart and able to answer well. This means that precise prompt engineering is utilized to make the model conform to our desired answer. The whisper-1 model is speech to text and allows for our student's questions to be translated into a string and passed into gpt-4. The tts-1 model then selects a voice model to then speak back the generated response to the question from gpt-4. By combining these models, the program is able to emulate a real teacher student interaction. I used some sample questions from a 3rd grade teacher to ensure that it was answering on level.

## Summary - Summarize the problem, solution, and issues

This project aimed to tackle the problem of over-burdened teachers by providing them assistance by answering students' questions effectively. This project was inspired by my mom as she is a 3rd grade teacher and I think something like this could truly help her and others alike.

This chat bot should behave as a 'TA' for these students and guide them to the solution without directly giving up the answer. My solution does accomplish what I set out to do and can fully comprehend the audio and speak back to the student, ensuring ease of use for young students.

My solution would be better with a frontend to make it more visually appealing and accessible. There's also more features I could add such as visual generation or expanding the bot to be more specialized in other ways. I ran into issues trying to get whisper-1 to read the captured audio file properly. Had to look up documentation and see which functions will accomplish the task the way I needed. It took me some time to decide which modules to use as google also had a good text to speech agent, but I opted with openAI's as it had better voices. Overall OpenAI provides lots of documentation and allows for me to gain a deeper understanding of how the model works and different ways it can be utilized. 