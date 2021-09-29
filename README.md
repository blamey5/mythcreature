# mythcreature
GUI to generate a classic mythical creature "sidekick" for user

import tkinter as tk
import tkinter.ttk as ttk
import tkinter.messagebox as messagebox


root = tk.Tk()
root.title("Mythical Creature Generator")
root.geometry("620x300")
root.resizable(0, 0)
root.config(bg="white")

temp_label = tk.Label(root, text="Enter Name: ", bg="white")
temp_label.grid(row=0, column=0, pady=20, padx=50)
temperature = tk.StringVar()
temp_ent = ttk.Entry(root, width = 25, textvariable=temperature)
temp_ent.grid(row=0, column=1)
temp_ent.focus()

unit_label = tk.Label(root, text="Select Unit:" ,bg="white")
unit_label.grid(row=1, column=0)
unit = tk.StringVar()
unit_box = ttk.Combobox(root, width=25, textvariable=unit, state="readonly")
unit_box[" "] = (" ", " ")
unit_box.current(0)
unit_box.grid(row=1, column=1)

unit1 = tk.StringVar()
unit_box1 = ttk.Combobox(root, width=25, textvariable=unit, state="readonly")
unit_box1[" "] = (" ", " ")
unit_box1.current(1)
unit_box1.grid(row=2, column=1, pady=20, padx=50)

ans_label = tk.Label(root, text="The answer is: " ,bg='white')
ans_label.grid(row=3, column=0)

def clear():
ans_frame.destroy()

def exit():
root.destroy()

convert_btn = ttk.Button(root,text="Convert", command=convert)
convert_btn.grid(row=3, column=2, pady=10)

clear_btn = ttk.Button(root,text="Clear", command=clear)
clear_btn.grid(row=4, column=2, pady=10)

exit_btn = ttk.Button(root,text="Exit", command=exit)
exit_btn.grid(row=5, column=2, pady=10)


root.mainloop()
