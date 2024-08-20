import java.util.Random;

public class TablaTem {

    public static void main(String[] args) {
        Random numRan = new Random();
        
        String[] ciudades = {"Cali", "Medellín", "Bogotá", "Pasto", "Barranquilla", "Manizales"};
        
        int numFilas = 101;
   
        double[][] temperaturas = new double[numFilas][ciudades.length];
        
        for (int i = 0; i < numFilas; i++) {
            for (int j = 0; j < ciudades.length; j++) {
                temperaturas[i][j] = numRan.nextDouble() * 100; 
            }
        }
        
    
        System.out.printf("%-10s", "Fila");
        for (String ciudad : ciudades) {
            System.out.printf("%-15s", ciudad);
        }
        System.out.println();
        
        for (int i = 0; i < numFilas; i++) {
            System.out.printf("%-10d", i + 1); 
            for (int j = 0; j < ciudades.length; j++) {
                System.out.printf("%-15.2f", temperaturas[i][j]);
            }
            System.out.println();
        }
    }
}
