import requests 
import re
from bs4 import BeautifulSoup 




import tkinter as tk

from tkinter.ttk import Notebook
from tkinter import ttk
import requests   
from tkinter import *


def getdatagoogle():
    q = e1.get()
    p = e2.get()
    escaped_search_term = q

    number_results = p

    language_code = 'en'


    result = []
    URL = 'https://www.google.com/search?q={}&num={}&hl={}'.format(escaped_search_term, number_results, language_code)
    
    r = requests.get(URL)

    soup = BeautifulSoup(r.content, 'html.parser') 
    
    for node in soup.findAll('h3'):
        res  = (''.join(node.findAll(text=True)))
        result.append(res)
        T.insert(END,"-------------------")
    #msg.showinfo("Results:",result)
        #T.insert(END,len(result))
        T.insert(END,'.')
        T.insert(END,res)
        T.insert(END,"\n")

        
        
  
    
    reslt =[]
    soup = BeautifulSoup(r.content, 'html.parser')        
        
    for j in soup.findAll('cite'):
        resl  = (''.join(j.findAll(text=True)))
        reslt.append(resl)
        T1.insert(END,"-------------------")
        T1.insert(END,len(reslt))
        T1.insert(END,'.')
        T1.insert(END,resl)
        T1.insert(END,"\n")
  
 
       
        

    




def getdatayoutube():
    ys = []
    q = e1.get()
    url3 = ('https://www.youtube.com/results?search_query='+q)
    r3 = requests.get(url3)
    soup3 = BeautifulSoup(r3.content, 'html.parser') 
    
    for node in soup3.find_all("h3"):

        
        yr = (''.join(node.findAll(text=True)))
        ys.append(yr)
        T2.insert(END,"-------------------")
        T2.insert(END,len(ys))
        T2.insert(END,'.')
        T2.insert(END,yr)
        T2.insert(END,"\n")

        


top = Tk()    

Label(top ,text="Search by Keyword : ")

top.title("News Search by Arindam Kumar Paul")        
top.geometry("1000x800")

Label(top ,text="Search Keyword : ")

H = Label(top ,text="Enter the keyword: ")

H.pack()
e1 = Entry(top, width = 150)





H1 = Label(top ,text="How many result you want to see : ")


e2 = Entry(top,width = 150)




b = Button(top, text='Find Titles of Google Result', command=getdatagoogle)

b2 = Button(top, text='Find Youtube Videos', command=getdatayoutube)


e1.pack()
H1.pack()
e2.pack()
b.pack()
b2.pack()
   
    
#e3 = Entry(top)
#e3.grid(row=2, column=1)
        
        
        
S = Scrollbar(top)


#Label(top,text="Google Search Results :")

#S = Text(top, height=10, width=50)
T = Text(top, height=10, width=30)



S.config(command=T.xview)
T.config(yscrollcommand=S.set)





#S = Text(top, height=10, width=50)
T1 = Text(top,  height=8, width=50)




T1.config(yscrollcommand=S.set)
    



#S = Text(top, height=10, width=50)
T2 = Text(top,  height=8, width=50)




T2.config(yscrollcommand=S.set)

L = Label(top,text="Titles of Google Search Results")
L.pack()
T.pack(side="top",fill="x")

L1 = Label(top,text="Links of Google Search Results")
L1.pack(side="top")
T1.pack(side="top",fill="x")
L2 = Label(top,text="Youtube Videos")
L2.pack(side="top")
T2.pack(side="top",fill="x")
S.pack()







mainloop()
