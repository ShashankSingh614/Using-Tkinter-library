#Creating a Menu and performing operations using tkinter library
from tkinter import *

#Intial Values
main_window = Tk()
d={}
l=[]

#Labels
menul = Label(main_window,text='MENU').grid(row=0,column=0,columnspan=3)
print()
emp_nol = Label(main_window,text='Employee Number:').grid(row=1,column=0)
namel = Label(main_window,text='Name:').grid(row=2,column=0)
agel = Label(main_window,text='Age:').grid(row=3,column=0)
occupationl = Label(main_window,text='Occupation:').grid(row=4,column=0)
contact_numberl = Label(main_window,text='Contact Number:').grid(row=5,column=0)

#Entries
emp_no=Entry(main_window,width=60,borderwidth=5).grid(row=1,column=1,columnspan=2)
name=Entry(main_window,width=60,borderwidth=5).grid(row=2,column=1,columnspan=2)
age=Entry(main_window,width=60,borderwidth=5).grid(row=3,column=1,columnspan=2)
occupation=Entry(main_window,width=60,borderwidth=5).grid(row=4,column=1,columnspan=2)
contact_number=Entry(main_window,width=60,borderwidth=5).grid(row=5,column=1,columnspan=2)

#Functions
def save():
    while True:
        l=[name,age,occupation,contact_number]
        d[emp_no]=l
        print('Saved Successfully')
        break

def clear():
    while True:
        emp_no = None
        name = None
        age = None
        occupation = None
        contact_number = None
        print('Cleared Successfully')
        break

def exitf():
    while True:
        print('Thank You!')
        break
    
#Buttons
saveb = Button(main_window,text='Save',command=save()).grid(row=6,column=0)
clearb = Button(main_window,text='Clear',command=clear()).grid(row=6,column=1)
exitb = Button(main_window,text='Exit',command=exitf()).grid(row=6,column=2)

#Main
main_window.mainloop()
