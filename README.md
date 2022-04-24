# Work
Its my WORK.
Тут мб будет работа, но это не точно!

from PyQt5.QtCore import Qt, QTime, QTimer
from PyQt5.QtWidgets import QLabel, QPushButton, QLineEdit, QWidget, QApplication, QHBoxLayout, QVBoxLayout

app = QApplication([])
#window                                 
window1 = QWidget()
window1.resize(600,400)
window2 = QWidget()
window2.resize(1000,800)
window3 = QWidget()
window3.resize(400,200)
#window 1
text1_window1 = QLabel('Добро пожаловать в программу ...')
text2_window1 = QLabel('Эта программа создан для помощи людям:...')
v_line_window1 = QVBoxLayout()
button_window1 = QPushButton()

v_line_window1.addWidget(text1_window1, alignment = Qt.AlignLeft)
v_line_window1.addWidget(text2_window1, alignment = Qt.AlignLeft)
v_line_window1.addWidget(button_window1, alignment = Qt.AlignCenter)

window1.setLayout(v_line_window1)
#Button
def push_button():
    window2.show()

button_window1.clicked.connect(push_button)

#window 2
text1_window2 = QLabel('Введите Ф.И.О:')
text2_window2 = QLabel('')
text3_window2 = QLabel('')
text4_window2 = QLabel('')
text5_window2 = QLabel('')
text6_window2 = QLabel('')

h_lin1_window2 = QHBoxLayout()
h_lin2_window2 = QHBoxLayout()
h_lin3_window2 = QHBoxLayout()
h_lin4_window2 = QHBoxLayout()
h_lin5_window2 = QHBoxLayout()
h_lin6_window2 = QHBoxLayout()
h_lin7_window2 = QHBoxLayout()

#Ask
ask1 = QLineEdit()
ask1 = QLineEdit()
ask1 = QLineEdit()
#Timer
def Timer_window2(self):
    time = time.addSecs(-1)
    if time.toString("hh:mm:ss") == "00:00:00":
        self.timer.stop()

time = QTime(0,0,15)
timer = QTimer()
timer.timeout.connect(Timer_window2)
timer.start(1000)




app.exec_()
window1.show()
