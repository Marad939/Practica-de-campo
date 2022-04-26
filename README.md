SubProceso Subir_CV(UserTable Por Referencia)

Definir Confimación,,terminar messages, input Como Caracter;
Definir i, documentLength Como Entero;
Definir boom Como Logico;

Limpiar Pantalla;
Escribir "+---------------------------------------------------------------+";
Escribir "|                  SUBIR CURRICULUM VITAE                       |";
Escribir "+---------------------------------------------------------------+";

backToScreenWelcome();

boom = Falso;

Dimension messages[2];
messages[1] = "- ¿Desea Subir CV? Indicar SI o NO:";

i = 1;

Mientras Mayusculas(input) <> "X" & boom = Falso Hacer
	input = validateFieldsEmpty(messages[i]);
	
	Si Mayusculas(input) <> "X" Entonces
		Segun i Hacer
			1:
				input = Mayusculas(input);
				Si input == "SI" O input == "NO" Entonces
					Confirmación = input;
					boom = Verdadero;
				SiNo
					Escribir "** El valor ingresado debe ser SI o NO. **";
					i = i - 1;
				FinSi
				
			2:
				terminar = input;	
		FinSegun
		
		i = i + 1;
	FinSi
FinMientras

Si boom = Verdadero Entonces
	// function insert here
	Escribir "Guardando Curriculum...";
	Esperar 500 Milisegundos;
	Escribir "Guardando Curriculum...";
	Esperar 500 Milisegundos;
	Escribir "Curriculum guardado!";
	Escribir "Para regresar al menu principal, presione cualquier tecla...";
	Esperar Tecla;
FinSi

Limpiar Pantalla;
FinSubProceso





SubProceso subir_legajo(UserTable Por Referencia)
	
	Definir confimación,terminar, messages, input Como Caracter;
	Definir i, documentLength Como Entero;
	Definir boom2 Como Logico;
	
	Limpiar Pantalla;
	Escribir "+---------------------------------------------------------------+";
	Escribir "|                  SUBIR LEGAJO DE INGRESANTE                   |";
	Escribir "+---------------------------------------------------------------+";
	
	backToScreenWelcome();
	
	boom2= Falso;
	
	Dimension messages[2];
	messages[1] = "- ¿Desea Subir CV? Indicar SI o NO:";
	
	i = 1;
	
	Mientras Mayusculas(input) <> "X" & boom = Falso Hacer
		input = validateFieldsEmpty(messages[i]);
		
		Si Mayusculas(input) <> "X" Entonces
			Segun i Hacer
				1:
					input = Mayusculas(input);
					Si input == "SI" O input == "NO" Entonces
						Confirmación = input;
						boom = Verdadero;
					SiNo
						Escribir "** El valor ingresado debe ser SI o NO. **";
						i = i - 1;
					FinSi
					
				2:
					terminar = input;	
			FinSegun
			
			i = i + 1;
		FinSi
	FinMientras
	
	Si boom2 = Verdadero Entonces
		// function insert here
		Escribir "Guardando Documentos...";
		Esperar 500 Milisegundos;
		Escribir "Guardando Documentos...";
		Esperar 500 Milisegundos;
		Escribir "Documentos almacenados!";
		Escribir "Para regresar al menu principal, presione cualquier tecla...";
		Esperar Tecla;
	FinSi
	
	Limpiar Pantalla;
FinSubProceso
