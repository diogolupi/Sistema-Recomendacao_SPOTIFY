# Sistema de Recomendação Spotify 🎧

Este projeto é um **sistema de recomendação musical** que utiliza um dataset com informações detalhadas de músicas do Spotify, Apple Music, Deezer e Shazam. O sistema recomenda músicas com base em características sonoras, como dançabilidade, energia e valência, utilizando **técnicas de aprendizado de máquina**.

## 📁 Dataset Utilizado

O dataset contém os seguintes atributos:

- **track_name**: Nome da música
- **artist_name**: Nome do(s) artista(s)
- **artist_count**: Número de artistas na música
- **released_year**: Ano de lançamento
- **bpm**: Batidas por minuto
- **key**: Tom da música
- **danceability_%**: Porcentagem de dançabilidade
- **valence_%**: Porcentagem de positividade
- **energy_%**: Nível de energia
- **acousticness_%**: Porcentagem de elementos acústicos
- **instrumentalness_%**: Porcentagem de conteúdo instrumental
- **liveness_%**: Presença de elementos ao vivo
- **speechiness_%**: Quantidade de palavras faladas

## 🚀 Funcionalidades

- **Recomendação baseada em similaridade de conteúdo**: O sistema recomenda músicas semelhantes a uma música alvo, analisando atributos sonoros (como bpm, energia, valência) e aplicando a métrica de **similaridade de cosseno** para encontrar faixas com características similares.
- **Escalabilidade**: O modelo é eficiente e escalável, capaz de recomendar músicas com precisão a partir de grandes conjuntos de dados.
- **Personalização**: As recomendações são altamente personalizadas, levando em conta a similaridade entre os atributos musicais.

## 🔧 Tecnologias

- **Python**: Linguagem principal utilizada
- **Jupyter Notebook**: Ambiente de desenvolvimento
- **Bibliotecas**: pandas, numpy, scikit-learn

## 📊 Como Funciona

O sistema utiliza um modelo de **similaridade de cosseno** para encontrar músicas com atributos semelhantes à música escolhida pelo usuário. Ao fornecer o nome da música, o modelo retorna uma lista de faixas recomendadas, baseadas na proximidade dos atributos sonoros.

### Exemplo de Uso:

```python
# Exemplo de recomendação de músicas baseadas em uma música alvo
song_name = "vampire"
recommended_songs = recommend_songs_by_name(song_name, 5)

for song, artist, score in recommended_songs:
    print(f"Artista: {artist}, Track: {song}, Similaridade: {score}")
