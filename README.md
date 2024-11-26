# Calculadora
def sumar(a, b):
    return a + b

def restar(a, b):
    return a - b

def multiplicar(a, b):
    return a * b

def dividir(a, b):
    if b != 0:
        return a / b
    else:
        return "Error: División por cero"

def suma_avanzada(numeros):
    return sum(numeros)

def menu():
    print("Seleccione una operación:")
    print("1. Sumar")
    print("2. Restar")
    print("3. Multiplicar")
    print("4. Dividir")
    print("5. Suma avanzada")
    print("6. Salir")

    opcion = int(input("Ingrese su elección (1/2/3/4/5/6): "))

    if opcion in [1, 2, 3, 4]:
        num1 = float(input("Ingrese el primer número: "))
        num2 = float(input("Ingrese el segundo número: "))

        if opcion == 1:
            print(f"Resultado: {sumar(num1, num2)}")
        elif opcion == 2:
            print(f"Resultado: {restar(num1, num2)}")
        elif opcion == 3:
            print(f"Resultado: {multiplicar(num1, num2)}")
        elif opcion == 4:
            print(f"Resultado: {dividir(num1, num2)}")
    elif opcion == 5:
        numeros = list(map(float, input("Ingrese los números separados por espacio: ").split()))
        print(f"Resultado: {suma_avanzada(numeros)}")
    elif opcion == 6:
        print("Saliendo...")
        return
    else:
        print("Opción no válida. Intente de nuevo.")

    menu()

if __name__ == "__main__":
    menu()
