<p align="center"><b>МОНУ НТУУ КПІ ім. Ігоря Сікорського ФПМ СПіСКС</b></p>
<p align="center">
<b>Звіт з лабораторної роботи 1</b><br/>
"Обробка списків з використанням базових функцій"<br/>
дисципліни "Вступ до функціонального програмування"
</p>
<p align="right"><b>Студент(-ка)</b>: Приймак Юліанна КВ-23</p>
<p align="right"><b>Рік</b>: 2025</p>

## Загальне завдання

```lisp
;; Оголошення списку
CL-USER> (setq my-list (list 'a 1 (list 'b 2) '() 22))
(A 1 (B 2) NIL 22)

;; Виведення голови списку
CL-USER> (car my-list) 
A

;; Виведення хвоста списку
CL-USER> (cdr my-list) 
(1 (B 2) NIL 22)

;; Виведення третього елемента списку
CL-USER> (nth 2 my-list) 
(B 2)

;; Виведення останнього елемента списку
CL-USER> (car (last my-list)) 
22

;; ATOM  1  - не список
CL-USER> (atom (car my-list)) 
T

;; ATOM  2 - список
CL-USER> (atom (nth 2 my-list)) 
NIL

;; LISTP  1 - не список
CL-USER> (listp (car (last my-list))) 
NIL

;; LISTP  2 - список
CL-USER> (listp (nth 2 my-list)) 
T

;; EQ  1 - не однакові
CL-USER> (eq (nth 2 my-list) '(b 2))
NIL

;; EQUAL  2 - однакові
CL-USER> (equal (nth 2 my-list) '(b 2))
T

 ;; EQUALP  3 - однакові
CL-USER> (equalp '(B 2) '(b 2))
T

;; APPEND
CL-USER> (append my-list (nth 2 my-list))
(A 1 (B 2) NIL 22 B 2) 

```
## Варіант 21 (5)
<p align="center">
 
```lisp
CL-USER> (let ((under1 (list 4 'e)))
  (let ((v5 (list 'D under1 (list 5) 'F)))
    v5))

(D (4 E) (5) F)
```
</p>

 
