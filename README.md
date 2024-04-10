##   Solicita una contraseña que inicie con un número y verifica si coincide con la primera ingresada.
#  Si se cometen tres errores al ingresar la contraseña, muestra un mensaje de aviso y cierra el programa.
    
def solicitar_contraseña():
    numero_de_intentos = 3
    contraseña_valida = False

    for i in range(numero_de_intentos):
        contraseña1 = input("Ingrese su contraseña (debe comenzar con un número): ")

        # Verifica si la contraseña inicia con un dígito
        if contraseña1[0].isdigit():
            contraseña2 = input("Repita su contraseña: ")

            # Verifica si ambas contraseñas coinciden
            if contraseña1 == contraseña2:
                print("Contraseña válida. ")
                contraseña_valida = True
                break
            else:
                print(f"Incorrecto. {numero_de_intentos - i - 1} intentos restantes.")
        else:
            print("La contraseña debe comenzar con un número.")

    if not contraseña_valida:
        print("Has excedido el número de intentos permitidos. El programa se cerrará.")

# Ejecuta la función principal
solicitar_contraseña()
