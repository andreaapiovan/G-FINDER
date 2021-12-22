import tkinter as tk
from tkinter import ttk
from PIL import ImageTk, Image

#generazione finestre
home= tk.Tk()
liceo=tk.Tk()
itis=tk.Tk()
auleI=tk.Tk()
laboratori=tk.Tk()
palestre=tk.Tk()
auleR=tk.Tk()
auleP=tk.Tk()

#inizializzazione immagini 
#HOME
logo_home= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/Logo.png'))
logo_btn_liceo= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/Liceo_btn.png'))
logo_btn_itis= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/Itis_btn.png'))
#ITIS
logo_itis= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/Scritta Itis.png'))
logo_btn_lab= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/btnLaboratori.png'))
logo_btn_auleI= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/btnAulei.png'))
logo_btn_palestre= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/btnPalestre.png'))
logo_btn_back= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/freccia.png'))
logo_lbl_g= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/ScrittaG.png'))
#LICEO


#inizializzazione finestra HOME
home.attributes('-fullscreen', True)
home.resizable(False, False)
home.title("G-FINDER HOME")
home.configure(background="#9ed7e8")
home.iconbitmap('C:/Users/User/Desktop/G-Finder/logogalilei.ico')
#home.withdraw()

#inizializzazione finestra LICEO
liceo.attributes('-fullscreen', True)
liceo.resizable(False, False)
liceo.title("G-FINDER LICEO")
liceo.configure(background="#9ed7e8")
liceo.iconbitmap('C:/Users/User/Desktop/G-Finder/logogalilei.ico')
liceo.withdraw()

#inizializzazione finestra ITIS
itis.attributes('-fullscreen', True)
itis.resizable(False, False)
itis.title("G-FINDER ITIS")
itis.configure(background="#9ed7e8")
itis.iconbitmap('C:/Users/User/Desktop/G-Finder/logogalilei.ico')
itis.withdraw()

#inizializzazione finestra AULE I
auleI.attributes('-fullscreen', True)
auleI.resizable(False, False)
auleI.title("G-FINDER AULE I")
auleI.configure(background="#9ed7e8")
auleI.iconbitmap('C:/Users/User/Desktop/G-Finder/logogalilei.ico')
auleI.withdraw()

#inizializzazione finestra LABORATORI
laboratori.attributes('-fullscreen', True)
laboratori.resizable(False, False)
laboratori.title("G-FINDER LABORATORI")
laboratori.configure(background="#9ed7e8")
laboratori.iconbitmap('C:/Users/User/Desktop/G-Finder/logogalilei.ico')
laboratori.withdraw()

#inizializzazione finestra PALESTRE
palestre.attributes('-fullscreen', True)
palestre.resizable(False, False)
palestre.title("G-FINDER PALESTRE")
palestre.configure(background="#9ed7e8")
palestre.iconbitmap('C:/Users/User/Desktop/G-Finder/logogalilei.ico')
palestre.withdraw()

#inizializzazione finestra AULE R
auleR.attributes('-fullscreen', True)
auleR.resizable(False, False)
auleR.title("G-FINDER AULE R")
auleR.configure(background="#9ed7e8")
auleR.iconbitmap('C:/Users/User/Desktop/G-Finder/logogalilei.ico')
auleR.withdraw()

#inizializzazione finestra AULE P
auleP.attributes('-fullscreen', True)
auleP.resizable(False, False)
auleP.title("G-FINDER AULE P")
auleP.configure(background="#9ed7e8")
auleP.iconbitmap('C:/Users/User/Desktop/G-Finder/logogalilei.ico')
auleP.withdraw()

#funzioni per il cambio pagina 
def switch_home_liceo(): 
    liceo.deiconify() 
    home.withdraw()

def switch_home_itis():
    itis.deiconify()
    home.withdraw()

def switch_itis_home():
    home.deiconify()
    itis.withdraw()

def switch_liceo_home():
    home.deiconify()
    liceo.withdraw()

def switch_liceo_auleP():
    auleP.deiconify()
    liceo.withdraw()

def switch_liceo_auleR():
    auleR.deiconify()
    liceo.withdraw()

def switch_auleP_liceo():
    liceo.deiconify()
    auleP.withdraw()

def switch_auleR_liceo():
    liceo.deiconify()
    auleR.withdraw()

def switch_itis_laboratori():
    laboratori.deiconify()
    itis.withdraw()

def switch_itis_auleI():
    auleI.deiconify()
    itis.withdraw()

def switch_itis_palestre():
    palestre.deiconify()
    itis.withdraw()

def switch_laboratori_itis():
    itis.deiconify()
    laboratori.withdraw()

def switch_auleI_itis():
    itis.deiconify()
    auleI.withdraw()

def switch_palestre_itis():
    itis.deiconify()
    palestre.withdraw()

#inizializzazione widget finestra HOME
lbl_logo_home= tk.Label(home, image=logo_home, bg="#9ed7e8")
lbl_logo_home.grid(row=1, pady=20, padx=200)

btn_liceo = tk.Button(home, image=logo_btn_liceo, borderwidth=0, command= switch_home_liceo)
btn_liceo.grid(row=2, column=0, pady=60, padx=180, sticky="W")
btn_liceo.configure(background="#9ed7e8")

btn_itis = tk.Button(home, image=logo_btn_itis, borderwidth=0, command= switch_home_itis)
btn_itis.grid(row=2, column=0, padx=180, sticky="E")
btn_itis.configure(background="#9ed7e8")

#inizializzazione widget finestra ITIS
lbl_logo_itis= tk.Label(itis, text="TITOLO ITIS", bg="#9ed7e8")  
lbl_logo_itis.grid(row=1, pady=20, padx=200)

btn_lab =  tk.Button(itis, text="LABORATORI", borderwidth=0, command= switch_itis_laboratori)
btn_lab.grid(row=2, column=0, pady=60, padx=180, sticky="W")
btn_lab.configure(background="#9ed7e8")

btn_auleI = tk.Button(itis, text="AULE I", borderwidth=0, command= switch_itis_auleI)
btn_auleI.grid(row=2, column=0, padx=180, sticky="E")
btn_auleI.configure(background="#9ed7e8")

btn_palestre = tk.Button(itis, text="PALESTRE", borderwidth=0, command=switch_itis_palestre)
btn_palestre.grid(row=3, pady=30)
btn_palestre.configure(background="#9ed7e8")

btn_back = tk.Button(itis, text="BACK", borderwidth=0, command= switch_itis_home)
btn_back.grid(row=4, column=0, pady=20, padx=20, sticky="W")
btn_back.configure(background="#9ed7e8")

lbl_g=tk.Label(itis, text="G" ,bg="#9ed7e8")
lbl_g.grid(row=4, column=0, pady=20, padx=20, sticky="E")

#inizializzazione widget finestra LICEO
lbl_logo_liceo= tk.Label(liceo, bg="#9ed7e8", text="TITOLO LICEO")
lbl_logo_liceo.grid(row=1, pady=20, padx=200)

btn_auleP =  tk.Button(liceo, text="AULE P", borderwidth=0, command= switch_liceo_auleP)
btn_auleP.grid(row=2, column=0, pady=60, padx=180, sticky="W")
btn_auleP.configure(background="#9ed7e8")

btn_auleR = tk.Button(liceo, text="AULE R", borderwidth=0, command= switch_liceo_auleR)
btn_auleR.grid(row=2, column=0, padx=180, sticky="E")
btn_auleR.configure(background="#9ed7e8")

logo_btn_back= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/freccia.png'))
btn_back = tk.Button(liceo, text="BACK" ,borderwidth=0, command= switch_liceo_home)
btn_back.grid(row=4, column=0, pady=20, padx=20, sticky="W")
btn_back.configure(background="#9ed7e8")

logo_lbl_g= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/ScrittaG.png'))
lbl_g=tk.Label(liceo, text="G" ,bg="#9ed7e8")
lbl_g.grid(row=4, column=0, pady=20, padx=20, sticky="E")

#inizializzazione widget finestra AULE I
lbl_logo_auleI= tk.Label(auleI, bg="#9ed7e8", text="TITOLO AULE I")
lbl_logo_auleI.grid(row=1, pady=20, padx=200)

lbl_auleI= tk.Label(auleI, bg="#9ed7e8", text="AULE I")
lbl_logo_auleI.grid(row=2, column=0, pady=60, padx=180, sticky="W")
cmb_auleI= ttk.Combobox(auleI, textvariable=3)
cmb_auleI['values'] = ('i19', 'i20', 'i21') 
cmb_auleI.grid(row=2, column=0, pady=60, padx=180, sticky="E")

logo_btn_back= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/freccia.png'))
btn_back = tk.Button(auleI, text="BACK" ,borderwidth=0, command= switch_auleI_itis)
btn_back.grid(row=3, column=0, pady=20, padx=20, sticky="W")
btn_back.configure(background="#9ed7e8")

logo_lbl_g= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/ScrittaG.png'))
lbl_g=tk.Label(auleI, text="G" ,bg="#9ed7e8")
lbl_g.grid(row=3, column=0, pady=20, padx=20, sticky="E")

#inizializzazione widget finestra PALESTRE
lbl_logo_palestre= tk.Label(palestre, bg="#9ed7e8", text="TITOLO PALESTRE")
lbl_logo_palestre.grid(row=1, pady=20, padx=200)

lbl_palestre= tk.Label(palestre, bg="#9ed7e8", text="PALESTRE")
lbl_logo_palestre.grid(row=2, column=0, pady=60, padx=180, sticky="W")
cmb_palestre= ttk.Combobox(palestre, textvariable=3)
cmb_palestre['values'] = ('Primo piano', 'Secondo piano', 'Terzo piano') 
cmb_palestre.grid(row=2, column=0, pady=60, padx=180, sticky="E")

logo_btn_back= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/freccia.png'))
btn_back = tk.Button(palestre, text="BACK" ,borderwidth=0, command= switch_palestre_itis)
btn_back.grid(row=3, column=0, pady=20, padx=20, sticky="W")
btn_back.configure(background="#9ed7e8")

logo_lbl_g= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/ScrittaG.png'))
lbl_g=tk.Label(palestre, text="G" ,bg="#9ed7e8")
lbl_g.grid(row=3, column=0, pady=20, padx=20, sticky="E")

#inizializzazione widget finestra LABORATORI
lbl_logo_laboratori= tk.Label(palestre, bg="#9ed7e8", text="TITOLO LABORATORI")
lbl_logo_palestre.grid(row=1, pady=20, padx=200)

lbl_laboratori= tk.Label(laboratori, bg="#9ed7e8", text="LABORATORI")
lbl_logo_laboratori.grid(row=2, column=0, pady=60, padx=180, sticky="W")
cmb_laboratori= ttk.Combobox(laboratori, textvariable=3)
cmb_laboratori['values'] = ('Chimica', 'Fisica', 'Informatica') 
cmb_laboratori.grid(row=2, column=0, pady=60, padx=180, sticky="E")

logo_btn_back= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/freccia.png'))
btn_back = tk.Button(laboratori, text="BACK" ,borderwidth=0, command= switch_laboratori_itis)
btn_back.grid(row=3, column=0, pady=20, padx=20, sticky="W")
btn_back.configure(background="#9ed7e8")

logo_lbl_g= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/ScrittaG.png'))
lbl_g=tk.Label(laboratori, text="G" ,bg="#9ed7e8")
lbl_g.grid(row=3, column=0, pady=20, padx=20, sticky="E")

#inizializzazione widget finestra AULE P
lbl_logo_auleP= tk.Label(auleP, bg="#9ed7e8", text="TITOLO AULE P")
lbl_logo_auleP.grid(row=1, pady=20, padx=200)

lbl_auleP= tk.Label(auleP, bg="#9ed7e8", text="AULE P")
lbl_logo_auleP.grid(row=2, column=0, pady=60, padx=180, sticky="W")
cmb_auleP= ttk.Combobox(auleP, textvariable=3)
cmb_auleP['values'] = ('P5', 'P6', 'P7') 
cmb_auleP.grid(row=2, column=0, pady=60, padx=180, sticky="E")

logo_btn_back= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/freccia.png'))
btn_back = tk.Button(auleP, text="BACK" ,borderwidth=0, command= switch_auleP_liceo)
btn_back.grid(row=3, column=0, pady=20, padx=20, sticky="W")
btn_back.configure(background="#9ed7e8")

logo_lbl_g= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/ScrittaG.png'))
lbl_g=tk.Label(auleP, text="G" ,bg="#9ed7e8")
lbl_g.grid(row=3, column=0, pady=20, padx=20, sticky="E")

#inizializzazione widget finestra AULE R
lbl_logo_auleR= tk.Label(auleR, bg="#9ed7e8", text="TITOLO AULE R")
lbl_logo_auleR.grid(row=1, pady=20, padx=200)

lbl_auleR= tk.Label(auleI, bg="#9ed7e8", text="AULE R")
lbl_logo_auleR.grid(row=2, column=0, pady=60, padx=180, sticky="W")
cmb_auleR= ttk.Combobox(auleR, textvariable=3)
cmb_auleR['values'] = ('R5', 'R6', 'R7') 
cmb_auleR.grid(row=2, column=0, pady=60, padx=180, sticky="E")

logo_btn_back= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/freccia.png'))
btn_back = tk.Button(auleR, text="BACK" ,borderwidth=0, command= switch_auleR_liceo)
btn_back.grid(row=3, column=0, pady=20, padx=20, sticky="W")
btn_back.configure(background="#9ed7e8")

logo_lbl_g= ImageTk.PhotoImage(Image.open('C:/Users/User/Desktop/G-Finder/ScrittaG.png'))
lbl_g=tk.Label(auleR, text="G" ,bg="#9ed7e8")
lbl_g.grid(row=3, column=0, pady=20, padx=20, sticky="E")

home.mainloop()
liceo.mainloop()
itis.mainloop()
auleI.mainloop()
auleP.mainloop()
auleR.mainloop()
palestre.mainloop()
laboratori.mainloop()

#per nascondere:
#root.withdraw()
#per aprire/riaprire:
#root.deiconify()
