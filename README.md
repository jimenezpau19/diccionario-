# import pandas as pd
print("MENU")
print("1 leer archivo")
print("2 mostrar cantidad de registros")
print("3 mostrar datos estadisticos")
print("4 consultas mayor o menor que")
print("5 salir")

df=pd.read_csv("Prestamos.csv")
while True:
    op=input("seleccione una opcion: ")
    if op=="1":
        print("leer archivo")
        df =pd.read_csv("Prestamos.csv")
    if op=="2":
        print("mostrar cantidad de registros")
        pritn=df.head(5)
    if op=="3":
        print("mostrar datos estadisticos")
        print(df["promedio"].min())
        print(df["Seleccionados"].max())
        print(df["Sustentantes"].median())
    if op=="4":
        print("consultas mayor o menor que")
        print(df[df["promedio"] > 50])
        print(df[df["promedio"] < 100])
    if op=="5":
        print("saliste")
        break
else:
    print("opcion invalida, intente de nuevo")
