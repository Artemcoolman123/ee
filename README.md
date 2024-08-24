class Widget():
    def __init__(self, tittletext, x_num, y_num):
        self.tittle = tittletext
        self.x = x_num
        self.y = y_num
    def print_info(self):
        print('Напис:', self.tittle)
        print('Розташування', self.x, self.y)
class Button(Widget):
    def __init__(self, tittle_text, x_num, y_num, is_clicked_bool):
        super().__init__(tittle_text, x_num, y_num)
        self.is_clicked = is_clicked_bool
    def click(self):
        self.is_clicked = True
        print('Ви зареестровані')

knopka = Button('Брати участь', 100, 100, False)
knopka.print_info()
answer = input("Бажеєте завереестровані")
if answer == 'так':
    knopka.click()
else:
    print('шкода')
