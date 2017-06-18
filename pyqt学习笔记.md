# pyqt学习笔记

---

使用数据库的时候，利用fetchall函数来取得数据库中的信息，如果里面包含该信息，则长度大于0

---

疑问，qt的窗口设置的时候，多个窗口重复设置，如何才能让其正确的显示，其机制是什么？（视频1.21.47）[视频链接][1]

```python
    self.welcomeWindow = Qtgui.QMainWindow()
    self.ui = Ui_MainWindow()
    self.ui.setupUi(self.welcomeWindow)
    self.welcomeWindow.show()
```
理解：在setupUi函数之中，将传入的对象进行了加工，所以后期的使用都是使用的自己传入的对象

---

## 设置messageBox

设置messagebox的Icon可以使用setIcon(QtGui.QMessageBox.Warning)
设置标题setWindowTitle(title)
设置文字setText(message)
设置标准按钮？setStandardButton(QtGui.QMessageBox.ok)
执行?exec_()

---

```python
    self.btn.cliked.connect(响应函数)
```

---

## **接收信息**

在做聊天室的时候发现，对于接受消息所单独启用的线程，是无法在那个线程之中直接对消息进行添加的

> 思路
>
> 改变方式，线程直接接受消息，使用一个时钟循环在很短的时间之内不停地对于label进行刷新，如果有线程接收到的新消息就进行添加





[1]: https://www.youtube.com/watch?v=4Y5zjTJ9LV4