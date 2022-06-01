1. Выбрать из file1 40 последних строк и записать в file2. 
```
tail -n 40 file1.txt >> file2.txt
```
![image](https://user-images.githubusercontent.com/83524353/171383447-4733b012-e950-4dfc-81c8-6f1d86040745.png)
2. Записать первые 10 строк из file2 в file3.
```
head -n 10 file2.txt > file3.txt
```
![image](https://user-images.githubusercontent.com/83524353/171383521-c2d2e62a-4b8d-4024-8acf-8f7fb38ac02a.png)
3.Выбрать в file2 все строки которые содержат "коко", заменить строку "коко" на "куку" и дописать только первые три вхождения в file3.
```
grep "коко" file2.txt | sed 's/коко/куку/' | head -n 3 >> file3.txt
```
![image](https://user-images.githubusercontent.com/83524353/171383848-23965c8e-58a4-44d5-899e-54e10d0ee0f5.png)
4. Оставить только уникальные строки в file3 и получить количества каждой уникальной строки в виде: КОЛ-ВО СТРОКА.
```
sort file3.txt | uniq -c
```
![image](https://user-images.githubusercontent.com/83524353/171384565-52345d64-75bb-42fa-96fd-4e288950c5cc.png)
