# Calculator
This is a IOS themed Calculator.

Code:
import tkinter as tk
from tkinter import *
calculation = ''

def  get_symbol(symbol):
    global calculation
    calculation +=str(symbol)
    result_label.delete(1.0,'end')
    result_label.insert(1.0, calculation)

def evaluate():
    global calculation
    try:
        calculation = str(eval(calculation))
        result_label.delete(1.0,'end')
        result_label.insert(1.0, calculation)
    except:
        clear()
        result_label.insert(1.0,'Error')


def clear():
    global calculation
    calculation = ''
    result_label.delete(1.0,'end')



root = tk.Tk()
root.title('Calculator')
root.geometry('330x430')
root.resizable(0,0)
root.configure(background='black')

result_label = tk.Text(root,bg='black',fg='white',height=2,width=12,font=('verdana',32))
result_label.grid(columnspan=10)


btn7 = Button(root, text='7', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(7))
btn7.grid(row=1,column=0)
btn7.config(font=('verdana',14))

btn8 = Button(root, text='8', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(8))
btn8.grid(row=1,column=1)
btn8.config(font=('verdana',14))

btn9 = Button(root, text='9', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(9))
btn9.grid(row=1,column=2)
btn9.config(font=('verdana',14))

btn4 = Button(root, text='4', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(4))
btn4.grid(row=2,column=0)
btn4.config(font=('verdana',14))

btn5 = Button(root, text='5', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(5))
btn5.grid(row=2,column=1)
btn5.config(font=('verdana',14))

btn6 = Button(root, text='6', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(6))
btn6.grid(row=2,column=2)
btn6.config(font=('verdana',14))

btn1 = Button(root, text='1', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(1))
btn1.grid(row=3,column=0)
btn1.config(font=('verdana',14))

btn2 = Button(root, text='2', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(2))
btn2.grid(row=3,column=1)
btn2.config(font=('verdana',14))

btn3 = Button(root, text='3', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(3))
btn3.grid(row=3,column=2)
btn3.config(font=('verdana',14))

btn_add = Button(root, text='+', bg='#FF9500', fg='white', width= 6, height=2, command= lambda : get_symbol('+'))
btn_add.grid(row=1,column=3)
btn_add.config(font=('verdana',14))

btn_sub = Button(root, text='-', bg='#FF9500', fg='white', width= 6, height=2, command= lambda : get_symbol('-'))
btn_sub.grid(row=2,column=3)
btn_sub.config(font=('verdana',14))

btn_mul = Button(root, text='*', bg='#FF9500', fg='white', width= 6, height=2, command= lambda : get_symbol('*'))
btn_mul.grid(row=3,column=3)
btn_mul.config(font=('verdana',14))

btn_div = Button(root, text='/', bg='#FF9500', fg='white', width= 6, height=2, command= lambda : get_symbol('/'))
btn_div.grid(row=4,column=3)
btn_div.config(font=('verdana',14))

btn_clear = Button(root, text='C',bg='#D4D4D2',fg='black',width= 6,height=2,command= lambda : clear())
btn_clear.grid(row=5,column=0)
btn_clear.config(font=('verdana',14))

btn0 = Button(root, text='0', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol(0))
btn0.grid(row=4,column=0)
btn0.config(font=('verdana',14))

btn_equal = Button(root, text='=',bg='#FF9500',fg='white',width= 6,height=2,command= lambda : evaluate())
btn_equal.grid(row=5,column=3)
btn_equal.config(font=('verdana',14))

btn_openbracket = Button(root, text='(', bg='#D4D4D2', fg='black', width= 6, height=2, command= lambda : get_symbol('('))
btn_openbracket.grid(row=5,column=1)
btn_openbracket.config(font=('verdana',14))

btn_closebracket = Button(root, text=')', bg='#D4D4D2', fg='black', width= 6, height=2, command= lambda : get_symbol(')'))
btn_closebracket.grid(row=5,column=2)
btn_closebracket.config(font=('verdana',14))


btn_dot = Button(root, text='.', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol('.'))
btn_dot.grid(row=4,column=2)
btn_dot.config(font=('verdana',14))


btn00 = Button(root, text='00', bg='#505050', fg='white', width= 6, height=2, command= lambda : get_symbol('00'))
btn00.grid(row=4,column=1)
btn00.config(font=('verdana',14))




root.mainloop()

