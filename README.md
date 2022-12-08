# Semana03Miercoles.md
Semana 03 - Día Miércoles - 07/12/2022

# Tabla de Multiplicar

Algoritmo TablaMultiplicar
	
	Imprimir " Introducir tabla a multiplicar "
	Leer X
	Contador <- 1
	
	Imprimir "   "
	Imprimir " Tabla del ", X
	Imprimir "   "
	
	Mientras Contador <= 10 Hacer
		
		Producto <- X * Contador
		Imprimir X, " * ", Contador, " = ", Producto
		
		Contador <- Contador + 1
		
	FinMientras
	
	
FinAlgoritmo


# Calculadora con pregunta de nueva operación

Algoritmo CalculadoraPlus
	
	//Solicitar dos números y validar que son enteros
	
	RestoX <- 0
	RestoZ <- 0
	Respuesta <- "n"
	
	Repetir
		
		Repetir
		
			Si RestoX <> 0 O RestoZ <> 0
			
				Limpiar Pantalla
				Imprimir " Introduzca nuevamente ambos valores "
				Imprimir "                                   "
			
			FinSi
		
			Imprimir " Introduzca el primer valor entero "
			Leer X
			Imprimir " Introduzca el segundo valor entero "
			Leer Z
		
			RestoX <- X - Trunc(X)
			RestoZ <- Z - Trunc(Z)

		Hasta Que RestoX = 0 & RestoZ = 0
	
		Repetir
		
			Imprimir " Indique la operación que desea realizar: "
			Imprimir "                   "
			Imprimir " Operaciones válidas: Suma + "
			Imprimir " Operaciones válidas: Resta - "
			Imprimir " Operaciones válidas: Multiplicación * "
			Imprimir " Operaciones válidas: División / "
			
			Leer OP
		
		Si OP = "+" O OP = "-" O OP = "*" O OP = "/"
			
			Entonces
			
				Si OP = "+"
				
					Resul <- X + Z
					Imprimir " El resultado de la suma es ", Resul
					
				FinSi
				
				Si OP = "-"
					
					Resul <- X - Z
					Imprimir " El resultado de la resta es ", Resul
					
				FinSi
				
				Si OP = "*"
					
					Resul <- X * Z
					Imprimir " El resultado de la multiplicación es ", Resul
					
				FinSi
				
				Si OP = "/"
					
					Resul <- X / Z
					Imprimir " El resultado de la división es ", Resul
					
				FinSi
					
			Sino
				
				Limpiar Pantalla
				Imprimir " La operación no existe, introduzcala nuevamente  "
				Imprimir "                   "
				
		FinSi
			
	
		Hasta Que OP = "+" O OP = "-" O OP = "*" O OP = "/"
	
		Imprimir " Desea realizar otra operación? "
		Imprimir " S = SI     N = NO "
		Leer Respuesta
	
	Hasta Que Respuesta = "n"
	
FinAlgoritmo
