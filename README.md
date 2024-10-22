# nurse-town


The primary purpose of this project is to develop a nursing student training game named “Nurse Town” that leverages Large Language Models (LLMs) and generative graphics and texts to create an immersive virtual training game for nursing students. This game aims to simulate a wide range of clinical scenarios with high fidelity, allowing students to practice and hone their skills in a controlled yet realistic setting. By doing so, the project seeks to enhance the quality and accessibility of nursing education, ensure a more uniform training experience, and better prepare students for the complexities of real-world medical care

How to run the project:

1. Clone the repository to your local machine.
2. Open the project in Unity.
3. In Unity, go to Assets/Doctor's office/Scene, click on "Demo", and then click on "Play".
4. Go to Assets/Doctor's office/Scripts/PatientSpeech.cs, and replace the placeholder API key with our secret OpenAI API key.
5. Import Newtonsoft.Json: In Unity, go to Window > Package Manager, click on "Add package from git URL", and enter "com.unity.nuget.newtonsoft-json", then click on "Add" to install it.
6. Go to Hierarchy, click on "Patient", in the Inspector, click on "Add Component", search for "PatientSpeech", and add it.
7. The game should start. You can see the conversation from Patient NPC from the console.

