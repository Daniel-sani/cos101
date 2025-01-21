import tkinter as tk
from tkinter import messagebox

# Dictionary with 20 words in Spanish and their English translations
dictionary = {
    "hola": "hello",
    "adiós": "goodbye",
    "gracias": "thank you",
    "amigo": "friend",
    "familia": "family",
    "casa": "house",
    "coche": "car",
    "perro": "dog",
    "gato": "cat",
    "escuela": "school",
    "trabajo": "work",
    "comida": "food",
    "bebida": "drink",
    "música": "music",
    "película": "movie",
    "libro": "book",
    "deporte": "sport",
    "viaje": "trip"
}


def translate():
    word = entry.get()
    if word in dictionary:
        result = dictionary[word]
        messagebox.showinfo("Translation", f"{word} means {result} in English")
    else:
        messagebox.showerror("Error", "Word not found in dictionary")


root = tk.Tk()
root.title("Spanish-English Dictionary")

label = tk.Label(root, text="Enter a Spanish word:")
label.pack()

entry = tk.Entry(root)
entry.pack()

button = tk.Button(root, text="Translate", command=translate)
button.pack()

root.mainloop()
