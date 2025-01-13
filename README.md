from tkinter import Tk, Entry, Button,  Label, StringVar


igbo_dict = {
    "house": "ulo",
    "peace": "udo",
    "life": "ndu",
    "medicine": "ugwu",
    "dream": "nro",
    "market": "ahia",
    "work": "oru",
    "wealth": "aku",
    "farming": "oru ugbo",
    "learn": "muo",
    "love": "ihunanya",
    "sand": "aja",
    "brain": "uburu",
    "food": "nri",
    "water": "mmiri",
    "family": "ezi na ulo",
    "friend": "enyi",
    "play": "egwu",
    "tree": "osisi",
    "book": "akwukwọ"
}


window =  Tk()
window.geometry('600x250')
window.title("igbo Dictionary")

entry_text = Entry(window, width=40)
entry_text.pack(pady=10)

result = StringVar()
result_label = Label(window, textvariable=result, font=("arial", 14))
result_label.pack(pady=10)

def search(word):
    if word in igbo_dict:
        result.set(igbo_dict[word])
    else:
        result.set("Not Found")

search_btn = Button(window, text="search", command=lambda:search(entry_text.get()))
search_btn.pack(pady=10)

window.mainloop()

