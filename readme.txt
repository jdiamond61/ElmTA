Jackson Diamond
ElmTA openAI chatGPT powered Python project

Code breakdown:
One must have access to the internet and an OpenAI api key in order to run this code. As well as the ability to run python.

Program utilizes OpenAI's suite of model's to make ElmTA. My main method references other functions once to do each of the required tasks,
to produce the audio output. These functions follow an easy to follow order of first recording audio by utilizing the sound device package.
Then the recorded audio is passed into whisper-1 to transcribe the audio, then gpt-4 takes the transcription and comes up with a response.
That response is then passed to OpenAI's tts-1 model to speak out the generated text.


How to run:

Need to update the OpenAI api key to your personal key to use.
client = OpenAI(
    api_key= 'your_OpenAI_api_key'
)

Run all of the initial code blocks before running main. 
Takes about a minute to run.
