
 
# SOS AI

## Overview

<h1>SOS AI is a sophisticated emergency response system that leverages cutting-edge technologies to enhance the efficiency and accuracy of handling 911 calls. By integrating AssemblyAI's transcription service, Twilio's voice API, HuggingFace's analysis tools, DigitalOcean's hosting solutions, and Firebase's real-time database, SOS AI ensures a timely and effective response to emergencies, providing critical support when it is needed most.</h1>

## Walkthrough 

- [FrontEnd-video](https://youtu.be/tP7V9_xB8JI) 

- [Backend-Video](https://youtu.be/jCalG0fj0bE)

<h2>## Technologies Used for backend</h2>

<h3>### 🧠 AssemblyAI's [Real-Time Transcription](https://www.assemblyai.com/docs/walkthroughs#realtime-streaming-transcription)</h3>
- Real-Time Transcription service
- Provides highly accurate and reliable transcription of spoken words into text
- Enables quick and accurate understanding of incoming 911 calls
- Facilitates real-time processing and efficient response to emergency calls

<h4>### ☎️ Twilio's [Programmable Voice API](https://www.twilio.com/docs/voice)</h4>
- Programmable Voice API for accepting and handling calls
- Intuitive REST API, webhook, and WebSockets for seamless caller interaction
- Caller ID feature for quick identification of callers
- Simplifies infrastructure management and call handling

<h5>### 🤗 HuggingFace's [Inference API](https://huggingface.co/inference-api)</h5>
- Inference API for comprehensive analysis of transcriptions
- Utilizes three Transformer models:
  - Named Entity Recognition (dbmdz/bert-large-cased-finetuned-conll03-english) for determining caller’s name and location
  - Additional NER model (Jean-Baptiste/roberta-large-ner-english) as a fall-back for improved accuracy
  - Zero Shot Text Classification (facebook/bart-large-mnli) for categorizing the nature of emergencies

<h6>### 🔥 Firebase [Realtime Database](https://firebase.google.com/docs/database)</h6>

- Real-time synchronization of data
- Instant reflection of database changes across connected devices
- Easy setup and use with powerful JS SDK for both frontend and backend
- Flexible data model for structured data management

<p>## Instructions to Run SOS AI</p>

<h7>### Backend Setup</h7>

1. **Navigate to Backend Directory:**
   ```sh
   cd backend
   ```

2. **Install Dependencies:**
   ```sh
   yarn
   ```

3. **Configure Environment Variables:**
   - Create and fill the `.env` file with the following keys:
     ```
     ASSEMBLYAI_API_KEY=your_assemblyai_api_key
     MAPS_API_KEY=your_maps_api_key
     HUGGINGFACE_API_KEY=your_huggingface_api_key
     HUGGINGFACE_API_KEY2=your_secondary_huggingface_api_key
     WALLET_PRIVATE_KEY=your_wallet_private_key
     ```
   - Note: A paid account is required for using AssemblyAI's streaming transcription.

4. **Start the Server:**
   ```sh
   yarn start
   ```

5. **Setup Tunnel Server for Twilio:**
   - We recommend using [localhost.run](https://localhost.run). Run the following command:
     ```sh
     ssh -R 80:localhost:8080 localhost.run
     ```

6. **Configure Twilio:**
   - Log in to the Twilio console.
   - Navigate to **Active Numbers** under **Manage Numbers**.
   - Click on the number you wish to configure.
   - Add the URLs provided by `localhost.run` to the configuration.
   - Call the number to access the service.

### Frontend Setup

1. **Navigate to Client Directory:**
   ```sh
   cd client
   ```

2. **Install Dependencies:**
   ```sh
   yarn
   ```

3. **Run the Development Server:**
   ```sh
   yarn dev
   ```

**Note:** The frontend is not yet connected to the backend, but you can use it by following the above steps.#   S O S - A I - o n - B l o c k c h a i n - 
 
 
