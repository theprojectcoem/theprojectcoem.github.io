# Coem visualizer
This is part of the Coem project (The union of Poems and Cuentos) and in this part I'm trying to visualize all classical short stories and poems less than 8 minutes long into an embeddings map of 3092 classical short stories and 22540 poems and Also listen to the stories through Carl Sagan Voice in spanish and english too.
The english version of all the poems cannot be hosted in GitHub with this one so it is hosted here: https://theprojectcoem.github.io with the oems in spanish for now. The links Visualization was done thanks to the help of @AgustinVallejo!

The landing page is here [Coem](https://theprojectcoem.github.io/), Visualize the embeddings here [Coem embeddings](https://theprojectcoem.github.io/embeddings.html). the links here [Coem Links](https://theprojectcoem.github.io/authorToAuthor3DSmall.html) and the poems here [Coem Poems](https://theprojectcoem.github.io/poems-info.html) and the stories here [Coem Stories](https://theprojectcoem.github.io/stories-info.html)


# Limits
The color are only for 50 categories at maximum in the embeddings, so segment it if you want to see grouping of Colors by authors. Github pages supports only 5 GB maximum so I cannot add al the stories audios in english nor the poems. The embeddings hosted in Github can only project files of 100 MB mat max so the poems embeddings had to be separated into 4 files.


# Models used:
- Translation: NLLB
- Sentence transformer: jina-embeddings-v2-base-es
- LLM: Phi-3
- TTS: Openvoice and Metavoice to generate the audios
- Midjourney: to generate some of the images. (The principals were done by artist Isabela Hernández)

# Coming soon
The spanish Audios will be reproceced fixing the weird noises. These audios and images will be uploaded to youtube and added as a column to the embeddings and also have a separate website where one can explore, comment, rate and subscribe to listen to this stories in a customized way with users and states that will create requests for the audios and data instead of having a monolith which Github Cannot support.
I have without the audio for now, the poems and suggestions of the most similar poems after the ones that you are reading. After that, the customization would be like adding their own voice or how they want the story to be like or how hard it is to read. Missing adding the english poems and The voice for poems, I would like a woman and I'm trying Idea Vilariño and Wislawa Szymborska.

# Contribute
If anyone want to contribute please Push a PR, or send me an email mostly the tsv and [json](static/authorLinksSmallerAllStories.json)
containing the metadata file of [stories_metadata.tsv](tensor_generator/stories_metadata.tsv) inside tensor_generator 
needs more attention. Need to turn them into csv, json or parquet to be eassily monitored. Finetuning 
the translation to make them really available for the stories and Poems would be really great. Also putting more effort to the front or the UX would be appretiated, it's my first time coding front end!

[![Donate with PayPal button](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/donate?hosted_button_id=F43U7EFMW5N2A)

## Explanation
I wanted to be able to see the stories that I liked, which authors I had read and hearing them from Carl's voice to explore everything the classical literature that I love has and also to Help people that can no longer read but still want to explore like in my family!! so I did this for me and for anyone else who also wants to explore Classical Literature. Also, to eassily get to know new authors or stories similar to what they already like or know, which in my case, took some time to read the recommendation from the prologues or by reading wikipedia, so I hope this helps but keep exploring and reading wikipedia and the books directly nonetheless!
These are 3092 short stories and 22450 short poems all under 8 minutes long approximately. They are scraped and annotated by me, wikipedia and the 
help of some LLMs. I embedded these stories using one of the best open source models for Spanish classification and 
extraction with high enough input tokens so that the entire story would fit that I could find at that moment.
All stories are in spanish originally. I used full open source models and computers (including GPUS) that were all free 
as a self limitation (Thank you Colab). I used Pinecone as a VectorDB. The Author Links was created using the Wikipedia API and seeing 
which other authors were mentioned, some of the authors couldn't get scraped by a wikipedia page so there is still work 
to be done.
Thank you open source people, literature databases in spanish that are too old like amediavoz.com
 and free trials or amounts per month for making this possible!! 


# To eassily start the server and test you can run:
```bash
python -m http.server 8000
```
and enter:

http://localhost:8000/

