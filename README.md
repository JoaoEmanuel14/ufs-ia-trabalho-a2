# TRABALHO DE INTELIGÊNCIA ARTIFICIAL – A2 (PORTUGUÊS)

Alunos participantes:
- EDGAR DE SOUZA DIAS  
- JOÃO EMANUEL MENDONÇA APÓSTOLO  
- JOSÉ MATHEUS RIBEIRO DOS SANTOS  
- MARIA EDUARDA PIRES POSSARI DOS SANTOS  
- ULISSES DE JESUS CAVALCANTE

Trabalho desenvolvido como forma de avaliação (A2) para a disciplina de Inteligência Artificial - COMP0427
Universidade Federal de Sergipe | Departamento de Computação | Prof. Dr. Hendrik Teixeira Macedo

## Objetivo do Projeto

Este trabalho tem como objetivo explorar a capacidade de modelos multimodais de Inteligência Artificial (OpenAI ChatGPT-4o e Google Gemini Pro) em compreender e gerar descrições coerentes com base em imagens, áudios e textos narrativos associados. Tal investigação será feita por meio de três experimentos. Primeiramente, será a capacidade dos modelos de lidarem com uma entrada multimodal. Subsequentemente, a transferência de modalidade será avaliada. Por fim, será aferida a capacidade das arquiteturas de reconhecer o contexto de vários prompts.

## Funcionalidades

- Conversão de descrições de texto em áudio via TTS (text-to-speech) com OpenAI e gTTS (Google Text-to-Speech) com Gemini
- Transcrição de áudios narrativos com Vosk (speech-to-text)
- Análise de imagens com descrição de contexto via:
  - OpenAI GPT-4o
  - Google Gemini 1.5 Pro
- Comparação entre os modelos em termos de:
  - **Coerência textual**
  - **Acurácia multimodal**
  - **Tempo de resposta**
- Avaliação da capacidade dos modelos de lidarem com entrada multimodal
- Avaliação da transferência de modadelidade
- Avaliação da progressão narrativa com base nas descrições geradas

## Tecnologias Utilizadas

- **Python 3.10+**
- **OpenAI API (GPT-4o, TTS)**
- **Google Gemini API (Gemini 1.5 Pro, gTTS)**
- **Vosk (Reconhecimento de fala offline)**
- **gTTS e pydub** para manipulação de áudio
- **Pillow (PIL)** para tratamento de imagens
- **Google Drive** para organização dos dados

> [!IMPORTANT]
> Para a utilização das APIs do OpenAI ChatGPT e do Google Gemini, são necessárias chaves secretas que permitem o acesso a estes recursos.
> 
> A chave do Gemini pode ser obtida gratuitamente pelo Google, porém a chave do ChatGPT-4o só pode ser obtida mediante um investimento financeiro no próprio site da OpenAI.

**Depois que as chaves forem obtidas, elas devem ser postas na aba "Secrets" do Google Colab e importadas para o código utilizando:**
```python
from google.colab import userdata

openai_api_key = userdata.get('OPENAI_API_KEY')  # Chave da OpenAI
google_api_key = userdata.get('GOOGLE_API_KEY')  # Chave do Google
```

## Estrutura de Pastas

📁 Inteligência Artificial/ 

  ├── 📁 Audios_narrativa/ # Áudios .mp3 com narração descritiva de cada imagem 
  
  ├── 📁 Imagens_narrativa/ # Conjunto de imagens usadas no experimento 
  
  ├── 📄 IA_Trabalho_A2.ipynb # Código principal do projeto 
  
  ├── 📄 README.md # Documentação do projeto


## Como Executar

1. **Monte o Google Drive no Colab** e garanta que os caminhos estejam corretos:
```python
from google.colab import drive
drive.mount('/content/drive')
```

2. Execute o notebook passo a passo, garantindo:
- Conversão dos arquivos .mp3 para .wav (PCM 16kHz mono)
- Transcrição dos áudios com Vosk
- Geração de descrições com OpenAI e Gemini
- Avaliação de coerência e tempo

> [!CAUTION]
> Cada áudio presente em "Audios_narrativa" se relaciona diretamente com uma imagem em "Imagens_narrativas". A sequência é a seguinte:
> 
> audio_1.mp3: Tobias explorando o bairro.jpg
> 
> audio_2.mp3: Tobias achou o guarda-chuva azul.jpg
> 
> audio_3.mp3: Guarda-chuva se fecha e portal aparece.jpg
> 
> audio_4.mp3: Tobias é sugado pelo portal.jpg
> 
> audio_5.mp3: Tobias chega em Umbrelópolis e é recebido pelo coelho estiloso.jpg

> [!NOTE]
> As imagens utilizadas no terceiro experimento foram geradas pelo ChatGPT-4o a partir da seguinte narrativa:
> 
> Num dia em que o sol brilhava com força, um gato cinza chamado Tobias decidiu sair para explorar o bairro. Ele andava como se tivesse um compromisso sério — cauda erguida, passos firmes. No meio do caminho, encontrou algo incomum: um guarda-chuva azul, aberto, no meio da calçada. Tobias parou. Olhou para o guarda-chuva. Depois para o céu sem nuvens. “Humano distraído”, pensou ele. Mas ao tocar no guarda-chuva com a pata, ele se fechou de repente... e um portal se abriu! Tobias foi sugado para dentro com um miau! surpreso. Quando abriu os olhos, estava numa cidade onde todos os animais usavam roupas e andavam de patinete. Um coelho de óculos escuros o olhou e disse: — Seja bem-vindo a Umbrellópolis. Aqui, só entra quem encontra o Guarda-Chuva Azul. Tobias deu um miado resignado. Aparentemente, a aventura do dia estava só começando.

## Métricas Avaliadas

| Métrica              | Descrição                                                                 |
|----------------------|---------------------------------------------------------------------------|
| Coerência Textual    | Avaliada manualmente pelos autores do projeto (nota de 1 a 5)             |
| Acurácia Multimodal  | Comparação entre a transcrição real da narrativa e a descrição gerada     |
| Tempo de Resposta    | Tempo medido em segundos para a geração da resposta de cada modelo        |


# ARTIFICIAL INTELLIGENCE PROJECT – A2 (ENGLISH)

Participating Students:
- EDGAR DE SOUZA DIAS  
- JOÃO EMANUEL MENDONÇA APÓSTOLO  
- JOSÉ MATHEUS RIBEIRO DOS SANTOS  
- MARIA EDUARDA PIRES POSSARI DOS SANTOS  
- ULISSES DE JESUS CAVALCANTE

Work developed as part of the A2 evaluation for the Artificial Intelligence course - COMP0427  
Federal University of Sergipe | Department of Computing | Prof. Dr. Hendrik Teixeira Macedo

## Project Objective

This project aims to explore the capabilities of multimodal Artificial Intelligence models (OpenAI ChatGPT-4o and Google Gemini Pro) in understanding and generating coherent descriptions based on images, audio, and associated narrative texts. This investigation will be conducted through three experiments. First, we will evaluate the models' ability to handle multimodal input. Then, modality transfer will be assessed. Finally, we will evaluate the architectures' capability to recognize the context of multiple prompts.

## Features

- Conversion of text descriptions to audio using TTS (text-to-speech) with OpenAI and gTTS (Google Text-to-Speech) with Gemini
- Transcription of narrative audios using Vosk (speech-to-text)
- Image analysis with contextual description via:
  - OpenAI GPT-4o
  - Google Gemini 1.5 Pro
- Comparison between the models in terms of:
  - **Textual coherence**
  - **Multimodal accuracy**
  - **Response time**
- Evaluation of the models' ability to handle multimodal input
- Evaluation of modality transfer
- Assessment of narrative progression based on generated descriptions

## Technologies Used

- **Python 3.10+**
- **OpenAI API (GPT-4o, TTS)**
- **Google Gemini API (Gemini 1.5 Pro, gTTS)**
- **Vosk (Offline speech recognition)**
- **gTTS and pydub** for audio manipulation
- **Pillow (PIL)** for image processing
- **Google Drive** for data organization

> [!IMPORTANT]
> To use the OpenAI ChatGPT and Google Gemini APIs, secret keys are required to access these resources.
> 
> The Gemini key can be obtained for free from Google, but the ChatGPT-4o key can only be acquired through a financial investment on OpenAI's official website.

**After obtaining the keys, they must be placed in the "Secrets" tab of Google Colab and imported into the code using:**
```python
from google.colab import userdata

openai_api_key = userdata.get('OPENAI_API_KEY')  # OpenAI's Key
google_api_key = userdata.get('GOOGLE_API_KEY')  # Google's Key
```

## Folder Structure

📁 Artificial Intelligence/  

  ├── 📁 Audios_narrativa/ # .mp3 audio files with descriptive narration for each image  
  
  ├── 📁 Imagens_narrativa/ # Set of images used in the experiment  
  
  ├── 📄 IA_Trabalho_A2.ipynb # Main project code  
  
  ├── 📄 README.md # Project documentation

## How to Run

1. **Mount Google Drive in Colab** and ensure the paths are correct:
```python
from google.colab import drive
drive.mount('/content/drive')
```

2. Run the notebook step by step, ensuring:
- Conversion of .mp3 files to .wav (PCM 16kHz mono)
- Audio transcription with Vosk
- Generation of descriptions with OpenAI and Gemini
- Evaluation of coherence and response time

> [!CAUTION]
> Each audio file in "Audios_narrativa" is directly related to an image in "Imagens_narrativas". The sequence is as follows:
> 
> audio_1.mp3: Tobias explorando o bairro.jpg
> 
> audio_2.mp3: Tobias achou o guarda-chuva azul.jpg
> 
> audio_3.mp3: Guarda-chuva se fecha e portal aparece.jpg
> 
> audio_4.mp3: Tobias é sugado pelo portal.jpg
> 
> audio_5.mp3: Tobias chega em Umbrelópolis e é recebido pelo coelho estiloso.jpg

> [!NOTE]
> The images used in the third experiment were generated by ChatGPT-4o, using the following narrative as a source:
> 
> On a day when the sun was shining brightly, a gray cat named Tobias decided to explore the neighborhood. He walked as if he had an important appointment — tail up, steps confident. Along the way, he found something unusual: a blue umbrella, open, in the middle of the sidewalk. Tobias stopped. He looked at the umbrella. Then up at the cloudless sky. “Careless human,” he thought. But when he touched the umbrella with his paw, it suddenly closed... and a portal opened! Tobias was sucked inside with a surprised meow! When he opened his eyes, he was in a city where all the animals wore clothes and rode scooters. A rabbit with sunglasses looked at him and said: — Welcome to Umbrellopolis. Here, only those who find the Blue Umbrella may enter. Tobias let out a resigned meow. Apparently, the day's adventure was just beginning.

## Evaluated Metrics

| Métrica              | Descrição                                                                           |
|----------------------|-------------------------------------------------------------------------------------|
| Textual Coherence    | Manually evaluated by the project authors (score from 1 to 5)                       |
| Multimodal Accuracy  | Comparison between the actual narrative transcription and generated description     |
| Response Time        | Time measured in seconds for each model's response generation                       |
