# TIC_TAC_TOE
#import tkinter library function
#create a frame and put button function of row and column
#create a loop where button actually work(when "X" next turn "O")

from tkinter import *

root =tk. Tk()
root.geometry("500x500")
root.title("TIC TAC TOE")

frame= Frame(root)
frame.pack()

turn = "X"

def play(event):
    global turn
    button=event.widget
    if turn == "X":
        button["text"]="X"
        turn= "O"
    else:
        button["text"]= "O"
        turn="X"

#First row
button1= Button(frame, text=" ", width= 4, height= 2, font=("Arial",40))
button1.grid(row= 0, column= 0)
button1.bind("<Button>", play)

button2= Button(frame, text=" " , width= 4, height= 2, font=("Arial",40))
button2.grid(row= 0, column= 1)
button2.bind("<Button>", play)

button3= Button(frame, text=" " , width= 4, height= 2, font=("Arial",40))
button3.grid(row= 0, column= 2)
button3.bind("<Button>", play)

#Second row
button1= Button(frame, text=" ",  width= 4, height= 2, font=("Arial",40))
button1.grid(row= 1, column= 0)
button1.bind("<Button>", play)

button2= Button(frame, text=" " , width= 4, height= 2, font=("Arial",40))
button2.grid(row= 1, column= 1)
button2.bind("<Button>", play)

button3= Button(frame, text=" " ,  width= 4, height= 2, font=("Arial",40))
button3.grid(row= 1, column= 2)
button3.bind("<Button>", play)

#Third row
button1= Button(frame, text=" ",  width= 4, height= 2, font=("Arial",40))
button1.grid(row= 2, column= 0)
button1.bind("<Button>", play)

button2= Button(frame, text=" " ,  width= 4, height= 2, font=("Arial",40))
button2.grid(row= 2, column= 1)
button2.bind("<Button>", play)

button3= Button(frame, text=" " ,  width= 4, height= 2, font=("Arial",40))
button3.grid(row= 2, column= 2)
button3.bind("<Button>", play)


root.mainloop()
