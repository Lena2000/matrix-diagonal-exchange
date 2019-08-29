# matrix-diagonal-exchange
Обмен диагоналей введенной матрицы
package обмендиагоналей;

import java.util.Scanner;

/**
 *
 * @author LENOVO
 */
public class Обмендиагоналей {

    /**
     * @param args the command line arguments
     */
      public static void main(String[] args) {
          Scanner sc=new Scanner(System.in);
          System.out.println("Введите размер матрицы:");
          int n=sc.nextInt();
          int k=n*n;
          System.out.println("Введите "+k+" элементов матрицы:");
          int mas[][]=new int[n][n];
          int i;
          int j;
          for(i=0; i<n; i++){
              for(j=0;j<n;j++){
               mas[i][j]=sc.nextInt();
              }
          }
          System.out.println("Ваши элементы матрицы:");
          for(i=0; i<mas.length; i++){
          for(j=0; j<mas[i].length; j++){
              System.out.print(mas[i][j]+ "\t");  
          }
              System.out.println();
          }
          
          int temp;
          for(i=0; i<n; i++){
         
             temp=mas[i][i];
             mas[i][i]=mas[i][n-1-i];
             mas[i][n-1-i]=temp;
         
          }
          
          System.out.println("Ваши элементы новой матрицы:");
          for(i=0; i<mas.length; i++){
          for(j=0; j<mas[i].length; j++){
              System.out.print(mas[i][j]+ "\t");  
          }
              System.out.println();
          }
          
          }
          
          
          
          }
   
  
