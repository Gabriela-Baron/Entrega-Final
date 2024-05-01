# Entrega-Final

/*
 * INSTITUCION UNIVERSITARIA POLITECNICO GRAMCOLOMBIANO
 * MODULO CONCEPTOS FUNDAMENTALES DE PPROGRAMACION [GRUPO B02]
 * ENTREGA FINAL- SEMANAS 7 Y 8. 
 * 
 * INTEGRANTES SUBGRUPO 10
 * ROBINSON AMADO PEÑA - 100273913
 * GABRIELA ALEXANDRA BARÓN BARRETO - 100285411
 * JEFERSON MEDINA GOMEZ - 100289745
 * KAROL MELISSA GOMEZ COLMENARES - 
 * DAVID SANCHEZ - 
 */


ingreso de los datos (productos vendidos por vendedor, vendedores y productos).

# Para empezar organizamos los datos de los vendedores en  los que se especificaron los nombres, apellidos, tipo de documento y el numero correspondiente de cada uno de los vendedores.

![image](https://github.com/Gabriela-Baron/Primera-Entrega/assets/164106618/88d4d90c-c0e7-4a04-9fe0-6b7f498573d6)

# Siguiente a eso validamos los datos del producto en los que se determinaron los idsPriductos, la cantidad de los mismos, los precios y nombres de los productos correspondientes.

![image](https://github.com/Gabriela-Baron/Primera-Entrega/assets/164106618/e231190a-b206-4327-a179-58a39e470b48)

# Por medio del arreglo para almacenar las ventas totales por vendedor.

![image](https://github.com/Gabriela-Baron/Primera-Entrega/assets/164106618/2a6e03f1-5188-4fe2-a129-337f100c1270)

# Se generaron los datos en el formato CSV.

![image](https://github.com/Gabriela-Baron/Primera-Entrega/assets/164106618/d6733352-bbea-4914-b516-52349a742ac1)

# Se calcularon las ventas totales por vendedor, donde se tubo en cuenta los nombres de los vendedores, sus ventas totales, la cantidad de productos y se tuvieron en cuenta los precios de los productos.

![image](https://github.com/Gabriela-Baron/Primera-Entrega/assets/164106618/e6c80cbd-bd48-4905-8f27-b000d45d4c2f)

# Se relacionan las ventas totales por vendedor.

![image](https://github.com/Gabriela-Baron/Primera-Entrega/assets/164106618/c401deae-c55d-4e0d-8888-7c9d9419ebab)

# Se busca al vendedor que recaudo mas dinero, teniendo en cuenta la función if con el cual se tienen en cuenta las ventas totales por vendedor.

![image](https://github.com/Gabriela-Baron/Primera-Entrega/assets/164106618/1751b980-1a15-4f61-89eb-d36edba5c210)

# Finalizando se ejecuta el resultado del vendedor que recaudo mas dinero, con todas las especificaciones.

![image](https://github.com/Gabriela-Baron/Primera-Entrega/assets/164106618/582b8a86-a701-4444-b894-f8047007599f)

//



public class GenerateInfoFiles {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		//DATOS VENDEDORES
		String [] nombresVendedores = {"CARLOS ANTONIO", "VERONICA LISNEY","ANDRES"};
		String [] apellidosVendedores = {"CASTRO BERNAL", "CARO BUENO", "SOTO RODRIGUEZ"};
		String [] tipoDocumentos  = {"CC", "CC", "CC"};
		String[] numeroDocumentos = {"1070959820", "1010152330", "1012356427"};
		
		//DATOS DEL PRODUCTO		
		int [] idsProductos = {101,102,103};
		int [][] cantidadesProductos = {
				{12,24,32},
				{2,15,10},
				{20,10,4}
		};
		double [] preciosProductos = {12000000, 67000000, 89000000};
		String [] nombresProductos = {"VEHICULO", "CAMIONETA", "CAMION"};
		
		//ARREGLO PARA ALMACENAR LAS VENTAS TOTALES POR VENDEDOR
		double [] ventasTotalesPorVendedor = new double[nombresVendedores.length];
		
		
		
		//GENERAR DATOS EN FORMATO CSV
		System.out.println("Datos en formato CSV;");
		
		//CALCULAR VENTAS TOTALES POR VENDEDOR
		for (int i = 0; i < nombresVendedores.length; i++) {
			for (int j = 0; j < nombresProductos.length; j++) {
				ventasTotalesPorVendedor[i] += cantidadesProductos[i][j] * preciosProductos[j];
			}
			// Mostrar las ventas totales por vendedor
			System.out.println(nombresVendedores[i] + ";" + apellidosVendedores[i] + ";" + ventasTotalesPorVendedor[i]);
		}
		
        // Encontrar el vendedor que recaudó más dinero
        int indiceVendedorMasVentas = 0;
        double maxVentas = ventasTotalesPorVendedor[0];
        for (int i = 1; i < ventasTotalesPorVendedor.length; i++) {
            if (ventasTotalesPorVendedor[i] > maxVentas) {
                 maxVentas = ventasTotalesPorVendedor[i];
                 indiceVendedorMasVentas = i;
                
			}
			
		}
        // Mostrar el vendedor que recaudó más dinero
        System.out.println("El vendedor que recaudó más dinero es:");
        System.out.println("Nombre: " + nombresVendedores[indiceVendedorMasVentas]);
        System.out.println("Apellido: " + apellidosVendedores[indiceVendedorMasVentas]);
        System.out.println("Tipo de Documento: " + tipoDocumentos[indiceVendedorMasVentas]);
        System.out.println("Número de Documento: " + numeroDocumentos[indiceVendedorMasVentas]);
        System.out.println("Total Recaudado: " + ventasTotalesPorVendedor[indiceVendedorMasVentas]);
		
	}
}


La primera parte de la segunda entrega consistió en encontrar al vendedor que recaudó menos dinero, en donde tuvimos en cuenta el índice de Vendedor con menos ventas y las Ventas totales por vendedor, gracias a esto podemos ver el índice mínimo de ventas por vendedor.

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/4d63acaf-0561-4020-9f19-0dc5ec6f4e73)

Para encontrar al vendedor que recaudó menos dinero, fue con ayuda del comando (System.out.println) buscamos al vendedor que recaudó menos dinero, en donde también codificamos para ver el nombre, apellido, tipo de documento, número de documento para finalizar mostrándonos el total recaudado. Luego le dimos un número a cada vendedor, esto con el fin de poder filtrar más rápido a cada vendedor y así mismo realizamos la operación matemática simplificando la ecuación para obtener el resultado para este vendedor. 

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/6ae06927-7271-446d-bdbc-6bf5366abad7)

Después pasamos a crear la lista de cadenas con la información de cada vendedor, generando los datos en el formato CSV, en la que tuvimos en cuenta la información de cada vendedor teniendo en cuenta sus respectivos nombres y apellidos para proceder a ver las ventas totales de cada uno de ellos.

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/5d1d077e-661d-4d1d-a566-25cccbe3f1ec)

Nosotros organizamos la lista de cadenas por ventas totales de mayor a menor en la cual tuvimos presente la información de cada vendedor junto con el total del recaudo.

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/84dfb033-04ac-4543-aca9-bb2a979aa2f1)




![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/10025a44-f344-4fac-9227-12e0f766c49f)


Esta parte del código es el encargado de escribir datos sobre los vendedores en un archivo CSV llamado (reporte_ventas_vendedores.csv) donde cada vendedor está representado como una fila de datos y los atributos del vendedor como una columna que está separada por punto y coma, la parte del código (BufferredWriter writer = new BufferedWriter( “reporte_ventas_vendedore.csv))), BufferedWriter es un “envoltorio” alrededor del FileWriter que lo que hace es mejorar la eficiencia de escritura. Y FileWriter se encarga de escribir en un archivo, si no existe, lo crea; si ya existe lo que hará es sobreescribirlo.


![image](https:/Para escribir en el archivo SCV ingresamos a la ruta del archivo, validamos por nombre y el total del recaudo para así visualizar la información de los vendedores. 

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/a8368b0a-d415-4dc4-adec-93ff35755f3e)



# NOVEDADES DEL CÓDIGO 

Se corrige el método para organizar a los vendedores por medio de las ventas totales de mayor a menor cantidad de dinero recaudado por cada vendedor. Utilizamos el algoritmo de ordenamiento como lo es el algoritmo de (BURBUJA) el cual nos sirvió para organizar los nombres como las ventas totales de cada vendedor. 

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/e928af3d-dc8e-4d44-ab76-d2b93f15d9a1)


En el código agregamos la variable (TEMP) la cual nos ayudo a almacenar temporalmente un valor durante la operación de intercambio, en este caso nos permitió utilizar esto para guardar los valores como nombre, apellido, tipo de documento de cada vendedor en el proceso de intercambio. 

NOTA: Si ocurre un error este se va imprimir en un mensaje de (ERROR) por consola señalando que tipo de error ocurrió, esto nos va a permitir identificar los bugs para así permitirnos solucionarlos, todo esto con base a la escritura de los archivos.

/github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/01664fc4-bd91-4022-a5a0-5e7b5414759d)


Aquí también se añade uno de los puntos solicitados de la entrega, que los productos vendidos por cantidad están ordenados en forma descendente.

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/23cadc0b-c73b-4295-9020-1ced8a99e103)


En el código agregamos el método createSalesMenFile, el cual es el encargado de crear el archivo pseudoaleatorio CSV con los datos del vendedor que proporcionamos al cual se llamó productos.csv.

NOTA: Si ocurre un error este se va imprimir en un mensaje de (ERROR) por consola señalando que tipo de error ocurrió, esto nos va a permitir identificar los bugs para así permitirnos solucionarlos, todo esto con base a la escritura de los archivos.


![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/364df78a-4fa8-4249-8d66-3850c4b2c2c9)


Encontramos también una función en java llamada printProductsFile que nos permite imprimir el contenido del archivo por consola, adicional a eso incluimos FileName de tipo String que representa la ruta del archivo que se imprimirá. El bloque  Try-with-resources, es otra función para abrir y manejar un la lectura de archivos, en el caso de BufferedReader que lee el archivo fileName, hay que tener presente que cada una de las iteraciones del bucle éste va a leer una línea del archivo con el método readLine(), del BufferedReader y que Line (variable) es la linea leida que es la que almacena esta, si la línea no es nula, quiere decir que hay contenido y este va imprimir por consola utilizando el System.out.pintIn(Line).

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/d65ad97f-d1e5-442b-9cdd-0729ee85cc0b)

# ASPECTOS DEL PROYECTO CON ARCHIVO TXT.

Conclusion.txt

> [!NOTE]
> - [Conclusion.txt]
> - [Directorio de archivos adjuntos](conclusion-txt).


# CODIGO DE LA ENTREGA FINAL.

/*
 * INSTITUCION UNIVERSITARIA POLITECNICO GRAMCOLOMBIANO
 * MODULO CONCEPTOS FUNDAMENTALES DE PPROGRAMACION [GRUPO B02]
 * ENTREGA PROYECTO 1 - ESCENARIO 3
 * 
 * INTEGRANTES SUBGRUPO 10
 * ROBINSON AMADO PEÑA - 100273913
 * GABRIELA ALEXANDRA BARÓN BARRETO - 100285411
 * JEFERSON MEDINA GOMEZ - 100289745
 * KAROL MELISSA GOMEZ COLMENARES - 
 * DAVID SANCHEZ - 
 */

import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;
import java.util.Random;


public class GenerateInfoFiles {

	//Metodo principal
	public static void main (String[] args) {
		//DATOS VENDEDORES
		String [] nombresVendedores = {"CARLOS ANTONIO", "VERONICA LISNEY","ANDRES"};
		String [] apellidosVendedores = {"CASTRO BERNAL", "CARO BUENO", "SOTO RODRIGUEZ"};
		String [] tipoDocumentos  = {"CC", "CC", "CC"};
		String[] numeroDocumentos = {"1070959820", "1010152330", "1012356427"};
		
		int [][] cantidadesProductos = {
				{12,24,32},
				{2,15,10},
				{20,10,4}
		};
		int [] preciosProductos = {12000000, 67000000, 89000000};
		String [] nombresProductos = {"VEHICULO", "CAMIONETA", "CAMION"};
		
		//ARREGLO PARA ALMACENAR LAS VENTAS TOTALES POR VENDEDOR
		int [] ventasTotalesPorVendedor = new int[nombresVendedores.length];
	      // GENERAR DATOS EN FORMATO CSV
        System.out.println("Generando archivo CSV...");
        System.out.println("Datos en formato CSV;");
		System.out.println();
		
		//CALCULAR VENTAS TOTALES POR VENDEDOR
		System.out.println("Ventas totales por vendedor ordenador de mayor a menor recaudo de dinero");
		for (int i = 0; i < nombresVendedores.length; i++) {
			for (int j = 0; j < nombresProductos.length; j++) {
				ventasTotalesPorVendedor[i] += cantidadesProductos[i][j] * preciosProductos[j];
			}
			// Mostrar las ventas totales por vendedor
			System.out.println(nombresVendedores[i] + ";" + apellidosVendedores[i] + ";" + " $ " + ventasTotalesPorVendedor[i]);
		}
		
		System.out.println();
		// ORDENAR VENDEDORES POR VENTAS TOTALES (Burbuja)
        for (int i = 0; i < ventasTotalesPorVendedor.length - 1; i++) {
            for (int j = 0; j < ventasTotalesPorVendedor.length - 1 - i; j++) {
                if (ventasTotalesPorVendedor[j] < ventasTotalesPorVendedor[j + 1]) {
                    // Intercambiar valores
                    int tempVentas = ventasTotalesPorVendedor[j];
                    ventasTotalesPorVendedor[j] = ventasTotalesPorVendedor[j + 1];
                    ventasTotalesPorVendedor[j + 1] = tempVentas;

                    // Intercambiar datos de vendedores correspondientes
                    String tempNombre = nombresVendedores[j];
                    nombresVendedores[j] = nombresVendedores[j + 1];
                    nombresVendedores[j + 1] = tempNombre;

                    String tempApellido = apellidosVendedores[j];
                    apellidosVendedores[j] = apellidosVendedores[j + 1];
                    apellidosVendedores[j + 1] = tempApellido;

                    String tempTipoDocumento = tipoDocumentos[j];
                    tipoDocumentos[j] = tipoDocumentos[j + 1];
                    tipoDocumentos[j + 1] = tempTipoDocumento;

                    String tempNumeroDocumento = numeroDocumentos[j];
                    numeroDocumentos[j] = numeroDocumentos[j + 1];
                    numeroDocumentos[j + 1] = tempNumeroDocumento;
                }
            }
        }

        //Bloque para abrir el archivo en modo de escritura
        try (BufferedWriter writer = new BufferedWriter(new FileWriter("reporte_ventas_vendedores.csv"))) {
            writer.write("Nombre;Apellido;Tipo Documento;Numero Documento;Ventas Totales\n");
            for (int i = 0; i < nombresVendedores.length; i++) {
                writer.write(nombresVendedores[i] + ";" + apellidosVendedores[i] + ";" + tipoDocumentos[i] + ";" + numeroDocumentos[i] + ";" + ventasTotalesPorVendedor[i] + "\n");
            }                                                                                                                                                                                                                                        

        } catch (IOException e) {
            System.err.println("Error al escribir en el archivo CSV: " + e.getMessage());
        }    
            // Calcular la cantidad total vendida de cada producto
            int[] cantidadesTotales = new int[nombresProductos.length];
            for (int i = 0; i < nombresProductos.length; i++) {
                for (int j = 0; j < cantidadesProductos.length; j++) {
                    cantidadesTotales[i] += cantidadesProductos[j][i];
                }
            }
            
            // Ordenar los productos por cantidad vendida de manera descendente (usando el método de selección)
            for (int i = 0; i < nombresProductos.length - 1; i++) {
                int maxIndex = i;
                for (int j = i + 1; j < nombresProductos.length; j++) {
                    if (cantidadesTotales[j] > cantidadesTotales[maxIndex]) {
                        maxIndex = j;
                    }
                }
                // Intercambiar el nombre, precio y cantidad de los productos
                String tempNombre = nombresProductos[maxIndex];
                nombresProductos[maxIndex] = nombresProductos[i];
                nombresProductos[i] = tempNombre;

                int tempPrecio = preciosProductos[maxIndex];
                preciosProductos[maxIndex] = preciosProductos[i];
                preciosProductos[i] = tempPrecio;

                int tempCantidad = cantidadesTotales[maxIndex];
                cantidadesTotales[maxIndex] = cantidadesTotales[i];
                cantidadesTotales[i] = tempCantidad;
            }
            
            // IMPRIMIR PRODUCTOS VENDIDOS POR CANTIDAD, ORDENADOS EN FORMA DESCENDENTE
            System.out.println("Productos vendidos por cantidad, ordenados en forma descendente:");
            for (int i = 0; i < nombresProductos.length; i++) {
                System.out.println(nombresProductos[i] + ";" + " $ " + preciosProductos[i] + ";" + cantidadesTotales[i]);
            }
            System.out.println();

            
            // Llamar al método para crear el archivo de productos
            createProductsFile(2); // el numero indica la cantidad de resultados que nos dará
            
            // Imprimir el contenido del archivo de productos
            System.out.println("Contenido del archivo de productos:");
            printProductsFile("productos.csv");
        }

        // Método para crear el archivo de productos con información pseudoaleatoria
        public static void createProductsFile( int productsCount) {
            String[] nombresProductos = {"VEHICULO", "CAMIONETA", "CAMION"};

            try (BufferedWriter writer = new BufferedWriter(new FileWriter("productos.csv"))) {
                writer.write("ID;Nombre;Precio\n");
                Random rand = new Random();
                for (int i = 1; i <= productsCount; i++) {
                    int randomIndex = rand.nextInt(nombresProductos.length);
                    int precio = rand.nextInt(10000) + 1000; // Precio aleatorio entre 1000 y 11000
                    writer.write(i + ";" + nombresProductos[randomIndex] + ";" + precio + "\n");
                }
            } catch (IOException e) {
                System.err.println("Error al escribir en el archivo de productos: " + e.getMessage());
            }
            System.out.println("Archivo de productos generado correctamente.");
        }

        // Método para imprimir el contenido de un archivo de productos
        public static void printProductsFile(String fileName) {
            try (BufferedReader reader = new BufferedReader(new FileReader(fileName))) {
                String line;
                while ((line = reader.readLine()) != null) {
                    System.out.println(line);
                }
            } catch (IOException e) {
                System.err.println("Error al leer el archivo de productos: " + e.getMessage());
            }
            System.out.println("Archivo CSV generado correctamente.");
            
	}

        // Metodo para crear el archivo pseudoaleatorio de ventas de un vendedores
        public static void createSalesMenFile(int randomSalesCount, String name, long id) {
        	try (BufferedWriter writer = new BufferedWriter(new FileWriter("ventas_" + name.replace(" ","")+""+ id + ".csv"))){
				writer.write ("ID Venta;Nombre Vendedor;ID Vendedor;Producto;Cantidad/n");
				Random rand = new Random ();
				for (int i=1; i <= randomSalesCount; i++) {
					String producto = getRandomProduct ();
					int cantidad = rand.nextInt (10) + 1; //cantidad aleatoria entre 1 y 10
					writer.write(i + ";"+ name + ";" + id + ";" + producto + ";" + cantidad + "/n");
				}
			} catch (Exception e) {
				// TODO: handle exception
				System.out.println("Error al escribir en el archivo de ventas: "+ e.getMessage());
			}
        	System.out.println("Archivo de ventas de " + name + " generado correctamente");
		}
        
        private static String getRandomProduct() {
        	String[] nombresProductos = {"VEHICULO" , "CAMIONETA", "CAMION"};
        	Random rand = new Random();
        	int randomIndex = rand.nextInt(nombresProductos.length);
        	return nombresProductos[randomIndex];
			
		}

        // Método para crear un archivo con información de vendedores
    public static void createSalesmanInfoFile(int salesmanCount) {
        // DATOS VENDEDORES
        String[] nombresVendedores = {"CARLOS ANTONIO", "VERONICA LISNEY", "ANDRES"};
        String[] apellidosVendedores = {"CASTRO BERNAL", "CARO BUENO", "SOTO RODRIGUEZ"};
        String[] tipoDocumentos = {"CC", "CC", "CC"};
        String[] numeroDocumentos = {"1070959820", "1010152330", "1012356427"};

        try (BufferedWriter writer = new BufferedWriter(new FileWriter("info_vendedores.csv"))) {
            // Escribir encabezado
            writer.write("Nombre, Apellido, Tipo Documento, Numero Documento, Ventas Totales\n");

            // Generar datos para cada vendedor
            Random rand = new Random();
            for (int i = 0; i < salesmanCount; i++) {
                int index = rand.nextInt(nombresVendedores.length); // Obtener un índice aleatorio
                String nombre = nombresVendedores[index];
                String apellido = apellidosVendedores[index];
                String tipoDocumento = tipoDocumentos[index];

  # MUCHAS GRACIAS
                String numeroDocumento = numeroDocumentos[index];
                int ventasTotales = rand.nextInt(1000000); // Generar ventas totales aleatorias

                // Escribir información del vendedor en el archivo
                writer.write(nombre + ", " + apellido + ", " + tipoDocumento + ", " + numeroDocumento + ", " + ventasTotales + "\n");
            }

            System.out.println("Archivo 'info_vendedores.csv' generado correctamente.");
        } catch (IOException e) {
            System.err.println("Error al escribir en el archivo: " + e.getMessage());
        }
    }

    // Método principal
    public static void main(String[] args) {
        // Verificar si se proporcionó el número correcto de argumentos
        if (args.length != 1) {
            System.out.println("Uso: java GenerateInfoFiles <cantidad_vendedores>");
            return;
        }

        // Parsear la cantidad de vendedores desde el argumento de la línea de comandos
        int cantidadVendedores = Integer.parseInt(args[0]);

        // Generar y escribir la información de los vendedores en un archivo
        createSalesmanInfoFile(cantidadVendedores);
    }
}


