# gui-calculator
In this I have user tkinter to make a calculater














from tkinter import *



root = Tk()

root.minsize(550, 530)
root.maxsize(550, 530)
root.title("CALCULATOR")
root.wm_iconbitmap("icon.jpg")

try:

    def click(event):
        text = event.widget.cget("text")
        print(text)
        if text == "=":
            if scvalue.get().isdigit():
                value = int(scvalue.get())
            else:
                try:
                    value = eval(screen.get())

                except Exception as e:
                    print(e)
                    value = "Error"
            scvalue.set(value)
            screen.update()

        elif text == "C":
            scvalue.set("")
            screen.update()
        else:
            scvalue.set(scvalue.get() + text)
            screen.update()

except Exception as e:
    print(e)




scvalue = StringVar()

scvalue.set("")
screen = Entry(root, textvar=scvalue, font="lucida  40  bold ")
screen.pack(fill=X, ipadx=4, ipady=4, padx=10, pady=10)

frame1 = Frame(root, bg="blue", relief=FLAT)
frame2 = Frame(root, bg="blue", relief=FLAT)
frame3 = Frame(root, bg="blue", relief=FLAT)
frame4 = Frame(root, bg="blue", relief=FLAT)

b1 = Button(frame1, fg="red", text="AC", font="40", padx=40, pady=25)
b1.pack(side=TOP, fill=BOTH)
b1.bind("<Button-1>", click)

b2 = Button(frame1, fg="black", text="7", font=" +", padx=40, pady=25)
b2.pack(side=TOP, fill=BOTH)
b2.bind("<Button-1>", click)

b3 = Button(frame1, fg="black", text="4", font="40", padx=40, pady=25)
b3.pack(side=TOP, fill=BOTH)
b3.bind("<Button-1>", click)

b4 = Button(frame1, fg="black", text="1", font="40", padx=40, pady=25)
b4.pack(side=TOP, fill=BOTH)
b4.bind("<Button-1>", click)

b5 = Button(frame1, fg="black", text="0", font="40", padx=40, pady=25)
b5.pack(side=BOTTOM, fill=BOTH)
b5.bind("<Button-1>", click)

b6 = Button(frame2, fg="black", text="()", font="40", padx=40, pady=25)
b6.pack(side=TOP, fill=BOTH)
b6.bind("<Button-1>", click)

b7 = Button(frame2, fg="black", text="8", font="40", padx=40, pady=25)
b7.pack(side=TOP, fill=BOTH)
b7.bind("<Button-1>", click)

b8 = Button(frame2, fg="black", text="5 ", font="40", padx=40, pady=25)
b8.pack(side=TOP, fill=BOTH)
b8.bind("<Button-1>", click)

b9 = Button(frame2, fg="black", text="2 ", font="40", padx=40, pady=25)
b9.pack(side=TOP, fill=BOTH)
b9.bind("<Button-1>", click)

b10 = Button(frame2, fg="black", text=".", font="40", padx=40, pady=25)
b10.pack(side=BOTTOM, fill=BOTH)
b10.bind("<Button-1>", click)

b11 = Button(frame3, fg="black", text="%", font="40", padx=40, pady=25)
b11.pack(side=TOP, fill=BOTH)
b11.bind("<Button-1>", click)

b12 = Button(frame3, fg="black", text="9", font="40", padx=40, pady=25)
b12.pack(side=TOP, fill=BOTH)
b12.bind("<Button-1>", click)

b13 = Button(frame3, fg="black", text="6", font="40", padx=40, pady=25)
b13.pack(side=TOP, fill=BOTH)
b13.bind("<Button-1>", click)

b14 = Button(frame3, fg="black", text="3", font="40", padx=40, pady=25)
b14.pack(side=TOP, fill=BOTH)
b14.bind("<Button-1>", click)

b15 = Button(frame3, fg="black", text="C", font="40", padx=40, pady=25)
b15.pack(side=BOTTOM, fill=BOTH)
b15.bind("<Button-1>", click)

b16 = Button(frame4, fg="black", text="/", font="40", padx=40, pady=25)
b16.pack(side=TOP, fill=BOTH)
b16.bind("<Button-1>", click)

b17 = Button(frame4, fg="black", text="* ", font="40", padx=40, pady=25)
b17.pack(side=TOP, fill=BOTH)
b17.bind("<Button-1>", click)

b18 = Button(frame4, fg="black", text="-", font="40", padx=40, pady=25)
b18.pack(side=TOP, fill=BOTH)
b18.bind("<Button-1>", click)

b19 = Button(frame4, fg="black", text="+", font="40", padx=40, pady=25)
b19.pack(side=TOP, fill=BOTH)
b19.bind("<Button-1>", click)

b20 = Button(frame4, fg="black", text="=", font="40", padx=40, pady=25)
b20.pack(side=BOTTOM, fill=BOTH)
b20.bind("<Button-1>", click)

frame1.pack(fill=BOTH, padx=10, side="left")

frame2.pack(fill=BOTH, padx=10, side="left")

frame3.pack(fill=BOTH, padx=10, side="left")

frame4.pack(fill=BOTH, padx=10, side="left")

root.mainloop()



