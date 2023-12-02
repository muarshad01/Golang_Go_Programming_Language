## 169. What are pointers

* All values are stored in memory. 
    * Post office boxes are good analogy for memory
        * Every location in memory has an address. 
        * $\color{red}{A\ pointer\ is\ a\ memory\ address.}$

* Operators
    * ampersand operator (`&`) 
    * dereferencing operator(`*`)
    * pointer to an int (`*int`)

* code
    * https://play.golang.org/p/Ysv5Adn3V1
    * https://play.golang.org/p/BO7zRQN4Xm
    * https://play.golang.org/p/ucJYPu3QkP
    * https://play.golang.org/p/KpLImTmQCa

***

## 170. Seeing type & value for pointers

***

## 171. Dereferencing pointers

***

## 172. Pass by value, pointers / reference types, and mutability

***

## 173. Pointer & value semantics defined

***

## 174. Pointer & value semantics heuristics

***

## 175. Pointers, values, the stack, & the heap

***

## 176. Exploring method sets part 1

***

## 177. Exploring method sets part 2

***

# -----------------------
133. When to use pointers
# -----------------------

* code
    * https://play.golang.org/p/lxsWkhTaYv
    * https://play.golang.org/p/XuI19kjFmb

# --------------
134. Method Sets
# --------------

* Method sets determine what methods attach to a TYPE. It is exactly what the name says: What is the set of methods for a given type? That is its method set.

* IMPORTANT: “The method set of a type determines the INTERFACES that the type implements.....”

* NON-POINTER RECEIVER
    * works with values that are POINTERS or NON-POINTERS.
* POINTER RECEIVER
    * only works with values that are POINTERS.

* Receivers 
---------
(t  T) -- T and *T 
(t *T) -- *T

code
* NON-POINTER RECEIVER & NON-POINTER VALUE: https://play.golang.org/p/2ZU0QX12a8
* NON-POINTER RECEIVER & POINTER VALUE: https://play.golang.org/p/glWZmm0gY6
* POINTER RECEIVER & POINTER VALUE: https://play.golang.org/p/pWFxsg6MSe
* POINTER RECEIVER & NON-POINTER VALUE: https://play.golang.org/p/G3lEy-4Mc8 ( code does not run )
    * this codes does run - notice the difference - method set determines the 
* INTERFACES that the type implements
    * https://play.golang.org/p/KK8gjsAWBZ