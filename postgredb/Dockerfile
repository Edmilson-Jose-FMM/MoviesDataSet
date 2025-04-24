FROM postgres:16

RUN apt-get update && \
apt-get install unzip -y && \
apt-get install curl -y

RUN mkdir -p /TMDB_movie_dataset_v11/

RUN curl -L -o /TMDB_movie_dataset_v11/tmdb-movies-dataset-2023-930k-movies.zip \
https://www.kaggle.com/api/v1/datasets/download/asaniczka/tmdb-movies-dataset-2023-930k-movies

RUN unzip /TMDB_movie_dataset_v11/tmdb-movies-dataset-2023-930k-movies.zip -d /TMDB_movie_dataset_v11