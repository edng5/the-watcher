# The Watcher: Kaggle x Google Gemini Long Context

> Paige Bailey, Paul Mooney, Ashley Chow, and Addison Howard. Google - Gemini Long Context. https://kaggle.com/competitions/gemini-long-context, 2024. Kaggle.

[![](https://markdown-videos-api.jorgenkh.no/youtube/NY0BU2m-3ZI)](https://youtu.be/NY0BU2m-3ZI)

## Introduction:

The Google Gemini Long Context Competition on Kaggle focuses on recommending the most relevant MCU movies, allowing viewers to save time while staying informed about the main storyline. This approach leverages Gemini's 2-million-token context window and content caching capabilities to create a tool for casual MCU fans, enabling them to skip watching all 34 movies and 11 TV shows while still grasping the core narrative.

## Methods:

The project uses web scraping and a Kaggle dataset of MCU transcripts as input to answer key questions, such as whether a story is essential to the overall MCU narrative, which movies serve as prerequisites, and key plot points to note for future developments. There are two options to inputting to Gemini:

### Option #1
- I webscrape for a transcript of WandaVision EP.9 and transcript of She-Hulk EP.9. [SubsLikeScript](https://subslikescript.com/)

- I input this transcript as context for Gemini, which contains 9065 tokens.
  
- Use the contents of that transcript as the context to send to Gemini 1.5 Pro to answer some questions about the movie and the MCU in general.

### Option #2
- I parsed Marvel Transcripts Kaggle dataset. [18 MCU movie transcripts (by Ethan Barr)](https://www.kaggle.com/datasets/barret07/marvel-transcripts)

- Input these transcript as context for Gemini which results in 313169 tokens.

- Use the contents of that transcript as the context to send to Gemini 1.5 Pro to answer some questions about the movie and the MCU in general.

### Prompt

Once the transcripts are parsed, include instructions, questions and the context in the prompt. The questions include:

- "In the following movies/tv shows, which one are worth watching based on relevance to the MCU timeline?"
  
- "Which other movies and series should I watch before only the relevant movies so that I fully understand the plot?"
  
- "Which key points, from the ones that you picked, do you think are major plot points in the future based on the comics?"

## Conclusion: 

While this experiments on the MCU, it can be applied to many other movies as well. This can help people use their time more effeciently by investing their time watching something they would be interested in.

Gemini is capable of taking in long context and answering questions about it with its knowledge space. It was able to provide a solution to my problem of being selectful in the movies I watch. Gemini also highlighted some prerequisites movies so I can fully understand the plot of these films. Furthermore, it can try and extrapolate and foreshadow what could be possible key plot point and Gemini is able to identify spoilers based on the contex, avoidng them in its response.
