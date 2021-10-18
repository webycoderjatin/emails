from tkinter import *
import smtplib
tk = Tk()
tk.geometry("400x300")
tk.resizable(0,0)
email_icon = PhotoImage(file="C:\\Users\\mycom\\OneDrive\\Documents\\email.png")
tk.iconphoto(tk,email_icon)
tk.title("Send Instant Email")
v = StringVar()
v1 = StringVar()
v2 = StringVar()
v3 = StringVar()
label1 = Label(tk,text="Send emails",font="Courier",bg="#3498db",fg="white").grid(row=0,column=3)

label2 = Label(tk,text="Your email",font="Courier",bg="#3498db",fg="white").grid(row=1,column=0)
entry1 = Entry(tk,font="Courier",textvariable=v).grid(row=1,column=3,columnspan=100)

label3 = Label(tk,text="Email password",font="Courier",bg="#3498db",fg="white").grid(row=3,column=0)
entry1 = Entry(tk,font="Courier",textvariable=v1).grid(row=3,column=3)

label4 = Label(tk,text="Your message",font="Courier",bg="#3498db",fg="white").grid(row=5,column=0)
entry1 = Entry(tk,font="Courier",textvariable=v2).grid(row=5,column=3)

label5 = Label(tk,text="Reciever email",font="Courier",bg="#3498db",fg="white").grid(row=6,column=0)
entry1 = Entry(tk,font="Courier",textvariable=v3).grid(row=6,column=3)
def check_send():
    get1 = v.get()
    get2 = v1.get()
    get3 = v2.get()
    get4 = v3.get()
    if "@" in get1:
        print("")
        server = smtplib.SMTP('smtp.gmail.com',587)
        server.starttls()
        server.login(get1,get2)
        server.sendmail(get1,get4,get3)
        Label(tk,text="------Email sent------",font="Courier",bg="#3498db",fg="white").grid(row=7,column=2,columnspan=200)
    elif "" in get1:
        Label(tk,text="Please enter email address",font="Courier",bg="#3498db",fg="red").grid(row=2,column=2,columnspan=200)
    else:
        Label(tk,text="Invalid email address",font="Courier",bg="#3498db",fg="red").grid(row=2,column=2,columnspan=100)
button1 = Button(tk,text="Send mail",font="Courier",bg="#2ecc71",border=0,fg="white",command=check_send).grid(row=7,column=3)

tk.config(bg="#3498db")
tk.mainloop()
