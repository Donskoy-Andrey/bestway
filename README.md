# Поиск оптимального маршрута

Робот движется по двумерной прямоугольной карте размером $N \times M$. Карта состоит из клеток, каждая клетка имеет высоту в диапазоне $[0,255]$. Из каждой клетки робот может перемещаться в трёх направлениях -- налево, направо или вниз (за исключением находящихся на границе клеток). При перемещении в новую клетку робот затрачивает энергию, равную 1+ высота этой клетки. Робот начинает своё движение из заданной точки $x_s$ самой верхней строки и должен прийти в заданную точку $x_f$ самой нижней строки карты. Необходимо написать программу, которая для заданной карты найдёт наименее энергозатратный маршрут для робота.

Карта - изображение 3-x канальное в формате png, отрисовка карты делается синим цветом, и в программе выбирается только синий канал, в выходном изображении отрисовка пути производится красным цветом. В качестве входных изображений можно создавать изображания  в MS Paint или в любом растровом редакторе. При выборе цвета R и G значения должны равняться нулю, а B можно менять от 0 до 255. 

## Входные данные:
Изображение в формате png, отрисовано оттенками синенго цвета (R=0, G=0, B=[0 ... 255]), количество строк (rows) и столбцов (cols) в изображение (в пикселях), а также пиксельная координата столбца начальной точки (x_s) в первой строке, и координата столбца финальной точки (x_f) в последней строке.

## Выходные данные:
Картинка  в формате png с прочерченным оптимальным путём из начальной точки в конечную.

## Порядок запуска:
1. Создание среды
```
$ mkdir build
$ cd build/
$ cmake ..
& make
```
2. Запуск программы
```
$ program_name input_img.png <rows> <cols> <x_s> <x_f> output_img.png
```
Например,
```
$ ./main ../data/images/input.png 100 100 0 99 ../data/images/out.png
```
Где начальная точка в данном случае в левом верхнем углу, а конечная в правом нижнем.

## Результат

![](https://github.com/Donskoy-Andrey/bestway/blob/master/data/images/out.png?raw=true)