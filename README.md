# txt 
def f(x):
    return x**3 -( x**2) + 2

def find_root(a, b, tolerance):
    while abs(b - a) > tolerance:
        c = (a + b) / 2
        if f(c) == 0:
            return round(c, 4)
        elif f(a) * f(c) < 0:
            b = c
        else:
            a = c
    return round((a + b) /2 , 4)

# Kullanıcıdan girişleri alma
a = float(input("Birinci değeri girin: "))
b = float(input("İkinci değeri girin: "))
tolerance = float(input("Tolerans değerini girin: "))

# Kökü bulma ve sonucu yazdırma
root = find_root(a, b, tolerance)
print("Kök:", root)
