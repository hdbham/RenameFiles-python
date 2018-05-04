## this is supposed to remove selected characters from files in a chosen directory
## but whitespace = (ノಠ益ಠ)ノ彡┻━┻

import os
import Tkinter as tk
from tkFileDialog import askopenfilename

def browse_button():
        # Allow to select a directory and store it in global variable
        # called folder_path
        global folder_path
        filename = TKfiledialog.askdirectory()
        folder_path.set(filename)
        print(filename)

       
        root = Tk()
        folder_path = StringVar()
        lbl1 = Label(master=root,textvariable=folder_path)
        lbl1.grid(row=0, column=1)
        button2 = Button(text="Browse", command=browse_button)
        button2.grid(row=0, column=3)

  
def rename_files():
        #  get file names from given folder selected via tkinter

        file_list = os.listdir(folder_path)
        print "Old Names"
        print(file_list)
        saved_path = os.getcwd()

        os.chdir(folder_path)
        for file_name in file_list: os.rename(file_name, file_name.translate(None, "0123456789"))
        os.chdir(saved_path) # (3) brings path back to original path


browse_button() # to declare global folder_path
rename_files() # run with global path declared

file_list = os.listdir(folder_path)
print "New Names"
print(file_list)

