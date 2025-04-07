# TRABALHO DE INTELIGÊNCIA ARTIFICIAL – A2 (PORTUGUÊS)

Alunos participantes:
- EDGAR DE SOUZA DIAS  
- JOÃO EMANUEL MENDONÇA APÓSTOLO  
- JOSÉ MATHEUS RIBEIRO DOS SANTOS  
- MARIA EDUARDA PIRES POSSARI DOS SANTOS  
- ULISSES DE JESUS CAVALCANTE

Projeto desenvolvido como forma de avaliação (A2) para a disciplina de Inteligência Artificial - COMP0427
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

## Estrutura de Pastas

📁 Inteligência Artificial/ 
  ├── 📁 Audios_narrativa/ # Áudios .mp3 com narração descritiva de cada imagem 
  ├── 📁 Imagens_narrativa/ # Conjunto de imagens usadas no experimento 
  ├── 📄 IA_Trabalho_A2.ipynb # Código principal do projeto 
    ├── 📄 modelo/ # Modelo Vosk utilizado para transcrição 
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

## Métricas Avaliadas

| Métrica              | Descrição                                                                 |
|----------------------|---------------------------------------------------------------------------|
| Coerência Textual    | Avaliada manualmente pelos autores do projeto (nota de 1 a 5)             |
| Acurácia Multimodal  | Comparação entre a transcrição real da narrativa e a descrição gerada     |
| Tempo de Resposta    | Tempo medido em segundos para a geração da resposta de cada modelo        |
