# Photo-Album-In-Python-Using-Tkinter-

Program Details:

The program first change your current directory with that path which you give to the program.if you want user enter the location directory you need to take an input the directory path from user then change current directory with the user given directory by using OS module.OS module allows to access the operating system files and allow to working with operating system files like change the file/folder name,directory,access a specific directory etc.  

After changing the directory select all the pictures from current directory and place all pictures on Tkinter GUI window.if the pictures are in PNG format then you don't need to import any extra library because tkinter supports PNG format images and if the pictures are in JPG format then you need to install "pillow" using cmd or windows power shell or python terminal in windows.and after install the pillow you need to import ImageTK and Image from PIL(python imaging library) library which are mention in code.



Used Module:

Tkinter Module (built-in package/library of python you don't need to install it).

From PIL Module Image and ImageTK (We need to install the pillow package into python because it is not built-in module).

To install Pillow you need to write "pip install pillow" in your any terminal.

OS Module(built-in package/library of python you don't need to install it).



Websites:

https://docs.python.org/3/library/tkinter.html  (Tkinter Module).

https://pillow.readthedocs.io/en/3.0.x/handbook/tutorial.html (Pillow Module ).

https://docs.python.org/3/library/os.html (OS Module).



Program Code:



from tkinter import *

from PIL import Image, ImageTk  #import this library to work/upload/open JPG images in python

import os  # Working with system files we need to import this library

root = Tk()

root.geometry("800x600")

# change the current directory with given directory give your folder path like this(G:/folder name1/foldername2)

dir = os.chdir("Give your folder path here") 

currentDir = os.listdir(dir) #show the list of directory

#print(currentDir)

root.title("Picture Album ")

textLabel = Label(root, text=" Wellcome to your Album", bg="white", font="arial 20 bold underline")

textLabel.pack(anchor="nw", fill=BOTH)

for pic in currentDir:

    image = ImageTk.PhotoImage(Image.open(pic))  # open  all the images of the current directory

    img = Label(root, image=image)

    img.image = image

    img.pack(side=LEFT,anchor="nw",pady=20,padx=3)



root.mainloop()

If you want to see program with out then visit the link: https://codingwithburhan.blogspot.com/
