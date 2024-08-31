import tkinter
from tkinter import *
import string
import random

def generator():
    small_alphabets=string.ascii_lowercase
    capital_alphabets=string.ascii_uppercase
    numbers=string.digits
    characters=string.punctuation

    all=small_alphabets+capital_alphabets+numbers+characters
    password_length=int(length_box.get())

    if choice.get()==1:
        passwordField.insert(0,random.sample(small_alphabets,password_length))
    if choice.get()==2:
        passwordField.insert(0,random.sample(small_alphabets+capital_alphabets,password_length))
    if choice.get()==3:
        passwordField.insert(0,random.sample(all,password_length))


root=Tk()
root.config(bg="black")
choice=IntVar()
Font=("arial",15,"bold")

passwordLabel=Label(root,text='Password Generator',font=("times new roman",20,"bold"),bg="black",fg="white")
passwordLabel.grid(pady=10)

weakradiobutton=Radiobutton(root,text="Weak",value=1,variable=choice,font=Font)
weakradiobutton.grid(pady=5)

mediumradiobutton=Radiobutton(root,text="Medium",value=2,variable=choice,font=Font)
mediumradiobutton.grid(pady=5)

strongradiobutton=Radiobutton(root,text="Strong",value=3,variable=choice,font=Font)
strongradiobutton.grid(pady=5)

lengthLabel=Label(root,text='Password length',font=("times new roman",20,"bold"),bg="black",fg="white")
lengthLabel.grid(pady=5)

length_box=Spinbox(root,from_=5,to_=18,width=5,font=Font)
length_box.grid(pady=5)

generateButton=Button(root,text="generate",font=Font,command=generator)
generateButton.grid(pady=5)

passwordField=Entry(root,width=25,bd=2,font=Font)
passwordField.grid()

root.title("Password Generator")
root.mainloop()
