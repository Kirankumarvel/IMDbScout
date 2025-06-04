
# 🎬 IMDbScout

**IMDbScout** is a lightweight and efficient Python-based command-line utility that fetches the IMDb rating of any movie using the [`IMDbPY`](https://pypi.org/project/IMDbPY/) library. This tool is ideal for movie lovers, developers, bloggers, or anyone curious to quickly check a film's popularity and reception.

---

## 📌 Features

✅ Simple command-line interface
✅ Fast movie search and rating fetch
✅ Gracefully handles missing or incorrect movie names
✅ Easy to read and extend Python code
✅ Beginner-friendly
✅ Built with pure Python

---

## 🧰 Technologies & Libraries Used

| Library      | Purpose                                 |
| ------------ | --------------------------------------- |
| `IMDbPY`     | Access IMDb's movie database via Python |
| `Python 3.x` | Programming language                    |

### 📦 Installation

Install `IMDbPY` via pip:

```bash
pip install IMDbPY
```

---

## 💻 How to Run

Save the following code in a file named `IMDbScout.py`:

```python
from imdb import IMDb

def get_movie_rating():
    movie_name = input("Enter the name of the movie: ")
    ia = IMDb()
    movies = ia.search_movie(movie_name)

    if movies:
        movie = movies[0]
        ia.update(movie)
        rating = movie.get('rating', 'N/A')
        print(f"The IMDb rating of '{movie_name}' is: {rating}")
    else:
        print(f"Movie '{movie_name}' not found!")

get_movie_rating()
```

Run it using:

```bash
python IMDbScout.py
```

---

## 🧪 Example Output

```
Enter the name of the movie: Titanic
The IMDb rating of 'Titanic' is: 7.9
```

---

## 📂 Project Structure

```bash
IMDbScout/
├── IMDbScout.py         # Main Python script
├── README.md            # Project documentation (this file)
└── requirements.txt     # (Optional) For dependency management
```

You can create a `requirements.txt` with:

```txt
IMDbPY
```

---

## 🌱 Future Improvements (Optional)

* [ ] List top 5 matching results with release year
* [ ] Add TV show support
* [ ] Include genres, plot summary, and cast
* [ ] Build a GUI version using `tkinter` or `PyQt5`
* [ ] Export results to CSV or JSON
* [ ] Web-based version (Flask)

---

## 📃 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

## 👨‍💻 Author

Made with ❤️ by **Kiran Kumar**

> “Sometimes all you need is a good movie… and a great tool to pick it.”



