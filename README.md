# Actividad_entregable_1

# Codigo fuente
```java
package actividades_comentarios;
/**
 * clase que lee un array de notas y busca la mayor de ellas, si se repite y hace la media
 * @author Saul Sánchez Fernández
 * @version 1.0
 */
public class AnalisisNotas {
	/**
	 * Metodo main, se ejecuta las aprtes del codigo para su prueba
	 * @param args
	 */
    public static void main(String[] args) {
    	/**
    	 * lista de notas
    	 */
        int[] notas = {5, 7, 3, 7, 2, 9, 7};
        /**
         * veces que se repite la mas alta
         */
        int contador = 0;
        /**
         * nota maxima
         */
        int notaMaxima = notas[0];
        /**
         * nota media
         */
        double notaMedia = 0;
        
        /**
         * LLamada a metodo para generar la nota maxima
         */
        notaMaxima = definirNota(notaMaxima, notas);
        System.out.println("Nota mas alta: " + notaMaxima);
        /**
         * llamada a metodo para contar las repeticiones de la nota maxima
         */
        contador = contarNotas(notaMaxima, notas, contador);
       
        /**
         * salida por pantalla de las repeticiones de la nota maxima
         */
        if (contador > 1) {
        	System.out.println("La nota mas alta se repite " + contador +" veces");
        }else {
        	System.out.println("La nota mas alta no se repite");
        }
        notaMedia = media(notas);
        
        /**
         * salida por pantalla de si la nota media es superor o inferior a 5
         */
        if (notaMedia >= 5) {
            System.out.println("BIEN la nota media es: " + notaMedia);
        } else {
            System.out.println("MAL la nota media es: " + notaMedia);
        }
    }
    
    /**
     * define la nota mas alta de la lista
     * @param notaMaxima
     * @param notas
     * @return
     */
    public static int definirNota(int notaMaxima, int[] notas) {
    	
    	for (int i = 1; i < notas.length; i++) {
            if (notas[i] > notaMaxima) {
                notaMaxima = notas[i];
            }
        }
    	
    	return notaMaxima;
    }
    /**
     * cuenta cuantas veces se repite la nota mas alta
     * @param notaMaxima
     * @param notas
     * @param contador
     * @return
     */
    public static int contarNotas(int notaMaxima, int[] notas, int contador) {
    	for (int i = 0; i < notas.length; i++) {
            if (notas[i] == notaMaxima) {
                contador++;
            }
        }
    	return contador;
    }
   
    /**
     * calcula la nota media
     * @param notas
     * @return
     */
    public static double media(int notas[]) {
    	
    	 int totalNotas = 0;
         for (int i = 0; i < notas.length; i++) {
             totalNotas += notas[i];
         }

         double notaMedia = (double) totalNotas / notas.length;
         return notaMedia;
    }
}

```
