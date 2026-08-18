# Proyecto-final-talendig-OA


### Tratamiento de nulos
La variable se encontraba almacenada como texto y presentaba 11 registros con espacios en blanco. Los registros afectados correspondían a clientes con tenure = 0. Debido a que no habían acumulado permanencia, los valores fueron tratados como cargos totales de $0 y posteriormente la variable fue convertida a tipo numérico.


### Dupliciados
No se encontraron registros duplicados, por lo que no fue necesario aplicar eliminación de duplicados.

También encontramos el problema especial que pide explícitamente el entregable:
**TotalCharges** llegaba como texto a pesar de representar una variable numérica.
Lo corregimos convirtiéndola a numérica.


### Validacion dee variables categoricas

for col in df.select_dtypes(include="object").columns:
    print(f"\n--- {col} ---")
    print(df[col].value_counts(dropna=False))

Este código recorre todas las columnas de texto (categorías) de tu DataFrame e imprime un resumen que muestra qué valores existen en cada una y cuántas veces se repite cada valor.

Es uno de los pasos más comunes durante la fase de Exploración de Datos (EDA) para entender las variables cualitativas.


### Feature Engineering

