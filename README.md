# Nurse-town


The primary purpose of this project is to develop a nursing student training game named “Nurse Town” that leverages Large Language Models (LLMs) and generative graphics and texts to create an immersive virtual training game for nursing students. This game aims to simulate a wide range of clinical scenarios with high fidelity, allowing students to practice and hone their skills in a controlled yet realistic setting. By doing so, the project seeks to enhance the quality and accessibility of nursing education, ensure a more uniform training experience, and better prepare students for the complexities of real-world medical care

## Set up
### Clone the repo:

To enable big file uploading, you need to use Git Large File Storage (Git LFS).

1. git lfs install
2. git clone <repository-url>

### Set up .env
1. Ask admin for api keys
2. Put .env to the root:

2.1 open your terminal, make sure you are in the nurse-town file

2.2 create a new .env file: `touch .env`

2.3 `nano .env` 

2.4 add the apikey in the .env file: `OPENAI_API_KEY=your_actual_api_key_here` (normally we don't need to use quote mark with the apikey)

2.5 ctrl+o then ctrl+x to save the change and exit nano

2.6 check whether .env file exist: `ls -a`


#### Note:
\Assets\Scripts\EnvironmentLoader.cs is attached to the main camera

## Run the project:

1. Clone the repository to your local machine.
2. Open the project in Unity.
3. In Unity, go to Assets/Doctor's office/Scene, click on "Demo", and then click on "Play".
5. Import Newtonsoft.Json: In Unity, go to Window > Package Manager, click on "Add package from git URL", and enter "com.unity.nuget.newtonsoft-json", then click on "Add" to install it.
6. Go to Hierarchy, click on "Patient", in the Inspector, click on "Add Component", search for "PatientSpeech", and add it.
7. The game should start. You can see the conversation from Patient NPC from the console.

Testing the Text-to-Speech System:

1. Go to Assets/Scripts/TTS/TTSManager.cs, and change the value of openAIApiKey to our secret OpenAI API key.
2. Open the TTS-Test Scene in the same folder.
3. Click Play and enter any text in the input field. Hit enter and the speech should play. With lip sync, The character should have matching mouth movement.

Lip Sync:

Tool: uLipSync - open source Unity plugin for lip sync. Github link: https://github.com/hecomi/uLipSync

Tutorial: https://www.youtube.com/watch?v=k5CtTsIKwE4

Testing the Speech Recognition System:

1. Go to Assets/Scripts/STT/SpeechToTextController.cs, and change the value of openAIApiKey to our secret OpenAI API key.
2. Open the STT-Test Scene in the same folder.
3. Click Play and enter any text in the input field. Press and hold space bar to start recording and release to end. Transcribed text will appear below.


### Debug reminder:
1. You may see bugs like:
`NullReferenceException: Object reference not set to an instance of an objectInputManger.LateUpdate () (at Assets/Scripts/InputManger.cs:34)`
If you encounter this bug, it might be because you pressed “Play” and then “Pause.” The correct approach is to press “Play,” and if you want to stop, click “Play” again to cancel. Avoid using the “Pause” button.
