# oop-programming-python
import sys

class cpa_complex:
    def __init__(self, re, im):
        if type(re) not in [int, float]:
            raise TypeError("Bad type:re")
        if type(im) not in [int, float]:
            raise TypeError("Bad type:im")
        self.re = float(re)
        self.im = float(im)

    def __add__(self, other):
        print("INSIDE __add__")
        tmp_re = self.re + other.re
        tmp_im = self.im + other.im
        tmp_c = cpa_complex(tmp_re, tmp_im)
        return (tmp_c)

    def __str__(self):
        return "(" + str(self.re) + ")+i(" + str(self.im) + ")"

def main():

    c1 = cpa_complex(1, 4)
    c2 = cpa_complex(3, 6) 
    print("HERE")
    
    c3 = c1 + c2

    print("THERE")
    print("c1:", c1)
    print("c2:", c2)
    print("c3:", c3)
main()
