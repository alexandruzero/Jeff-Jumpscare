from threading import Thread
from tkinter import *
from PIL import Image, ImageTk      # pip install Pillow
from playsound import playsound
# Keyboard and mouse modules
import keyboard
from pynput.mouse import Controller


def fullscreen():
    root = Tk()
    root.geometry('1920x1080')
    root.attributes('-fullscreen', True)
    image = Image.open('jeff.png')
    photo = ImageTk.PhotoImage(image)
    display = Label(image=photo)
    display.pack()
    root.mainloop()


def sound_effect():
    # Choice ??
    while True:
        playsound('scream0.mp3')


def disable_all():
    flag = 1
    mouse = Controller()
    for i in range(150):
        keyboard.block_key(i)
    while flag == 1:
        mouse.position = (0, 0)


t1 = Thread(target=fullscreen)
t1.start()

t2 = Thread(target=sound_effect)
t2.start()
# Uncomment to block keyboard and mouse
# t3 = Thread(target=disable_all)
# t3.start()
