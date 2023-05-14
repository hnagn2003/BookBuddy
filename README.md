### Group 17
Nguyễn Hoài Ngân - 21020363
Nguyễn Thị Quỳnh Mai - 21020125
Lê Phương Linh - 21020544
Vũ Phượng Hồng - 21020764

### Introduction

This is a Book Recommendation System built for all you Book Lovers📖.

### Setting Up the Project

1. The Project works seamlessly on Python version `3.8.6`

2. Clone Your Forked copy/the original repo - `git clone https://github.com/hnagn2003/BookBuddy`

3.  Navigate to the directory of project -  `cd BookBuddy/`

4. Install requirements from [poetry](https://python-poetry.org/docs/#installation) - `poetry install`
    - If you prefer the vanilla route `poetry export -f requirements.txt --output requirements.txt --without-hashes` skip to step (6)

5. Activate the environment -  `poetry shell`

6. Open `BookRecSystem/settings.py`

7. Make Migrations - `python manage.py migrate`

8. `python manage.py runserver` - You're good to Go!!

### Dataset 🧾
The Dataset that we used for this task is the [goodbooks-10k](https://github.com/zygmuntz/goodbooks-10k) dataset. It consists of 10k books with a total of 6 million ratings. 

**Dataset Structure**
```
GoodBooks10k
    ├── books.csv         # Contains book info with book-id
    ├── ratings.csv       # Maps user-id to book-id and rating
    ├── book_tags.csv     # Contains tag-id associated with book-ids
    ├── tags.csv          # Contains tag-name associated with tag-id
    ├── to_read.csv       # Contains book-ids marked as to-read by user
```

### PreProcessing 🛠
Since this is a recommendation problem, we have to make sure that the `books.csv` is as clean as possible and only consider those ratings whose book-id is present, same goes for vice versa.

More Cleaning for `books.csv`
- Missing Book Image URLs
- Book & Rating Duplicates

### Model Exploration 🤯
For Recommendation Problems there are multiple approaches that are possible:
- Embedding Matrix
- Term Frequency

### Project Structure 💁‍♀️
```
BookBuddy
│
├───BookRecSystem               # Main Project Directory
│
├───forms                       # Form Class
│
├───mainapp                     # Project Main App Directory
│   │
│   └───migrations              # Migrations
│
├───static
|   |                           # Static Directory
│   └───mainapp
│       ├───css                 # CSS Files
|       |
│       ├───dataset             # Dataset Files
│       │
│       ├───gif                 # GIF Media
│       │
│       ├───model_files         # Model Files
|       |   |
│       │   ├───surprise        # FunkSVD Files
│       │   │
│       │   └───cv              # CV Files
│       │
│       └───png                 # PNG Media FIles
|
└───templates                   # Root Template DIrectory
    |
    ├───account                 # Account App Templates
    │
    └───mainapp                 # Project Main App Templates

```

### References 😇

- [Dataset](https://github.com/zygmuntz/goodbooks-10k)
- [Count Vectorizer](https://www.kaggle.com/sasha18/recommend-books-using-count-tfidf-on-titles)
- [Books2Rec](https://github.com/dorukkilitcioglu/books2rec)

