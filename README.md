# The similar movie searcher

This program searches for the movies by name, shows its rating and helps you find similar ones.

It's founded on [The Movies Data Base](https://www.themoviedb.org/).
The program receives top 1000 movies from TMBD and save them to a local database.
The similar searching finds eight most similar to the one you specified.
The selection is based on parameters such as belongs to collection, original language, budget and genres.


## How to install
### Get an api key
Before using, you should get your own api key.
- Log in at [themoviedb.org](https://www.themoviedb.org/login).
- Follow instructions to get an api key.

### Install requirements
Python3 should be already installed. Then use `pip` (or `pip3`, if there is a conflict with Python2) to install dependencies:

```
pip install -r requirements.txt
```

### Create local database
Create your own local database of the top 1000 movies by requesting from TMDB using api.
```
python make_own_db
```
You will be asked for an api key that you are created.
```
Enter your api key v3:

```
*The local database will be saved to the file `MyFilmDB.json` at the service root directory.*

## How to use
### Search for the movie by title
Use `python` (or `python3`).
Start searching the film by title:
```
python search_in_db
```
- It will ask you for path to local database file.
```
Enter path to DataBase:
```
*Type `MyFilmDB.json` if you didn't change the name or the location of the local database file.*
- Enter the name of the movie.
```
Enter film to search for:
```
You will see the movie info.
### Find similar movies
Start searching of similar ones:
```
python find_similar
```
- It will also ask you for the path to a local database file (do the same as in "search by title" step).
```
Enter path to DataBase:
```
- Then you will be asked to type the name of the movie, which will be used to searching for similar ones.
```
Enter film to search for:
```
You will see a list of eight of the most similar movies.

## Project Goals
The code is written for educational purposes on online-course for web-developers [dvmn.org](https://dvmn.org/).
