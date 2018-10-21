# try_cath

package uso_try_catch;

/**
 *
 * @author WILDER M
 */
public class switch_txt {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        
        
        
        
    }
    
}



mein class

package uso_try_catch;

import java.io.BufferedReader;
import java.io.File;
import java.io.IOException;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.util.logging.Level;
import java.util.logging.Logger;
import javax.swing.JOptionPane;

/**
 *
 * @author WILDER M
 */
public class try_catch {

    private String archivo;
    
    public void leerArchivo()throws FileNotFoundException,IOException, IOException{
        File archivo = new File ("D:\\todo java\\try_catch\\prueba.txt");
        FileReader fr = new FileReader(archivo);
        BufferedReader bf = new BufferedReader(fr);
        String linea = null;
        while((linea=bf.readLine())!=null){
        System.out.println(linea); 
        }
       
    
    }

public void leerArchivo2(){
    
        try {
            leerArchivo();
        } catch (FileNotFoundException ex){
            JOptionPane.showMessageDialog(null,"no se ha encontrado el archivo, por favor verificar la ruta");
            
        }catch(IOException e){
            
            JOptionPane.showMessageDialog(null,"ha ocurrido una opcion verificada");
            
        }
        
}
    
    public static void main(String[] args) {
        
        try_catch prueba = new try_catch();
       prueba.leerArchivo2();
        
       
       
        
  
        
    }
  

    
}
