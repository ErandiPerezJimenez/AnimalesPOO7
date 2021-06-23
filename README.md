# AnimalesPOO7
Page Git
package Zoologico;

public class main {

    public static void main(String[] args) {

        Ballena animal = new Ballena(4, "Perlita", "Fondo de Bikini", "Gris", 15);
        animal.setNumeroAletas(3);
        animal.getNumeroAletas();
        System.out.println(animal.toString());
        animal.comer();
        animal.pelearConPinocho();

        System.out.println("**********************************************");

        Perro perro1 = new Perro(4, "Eva", "Calle", "Negro");
        perro1.setColorCollar("Morado");
        perro1.getColorCollar();
        System.out.println(perro1.toString());
        perro1.hacerTrucos();
        perro1.comer();
        
        System.out.println("**********************************************");
        
        Pajaro pajaro = new Pajaro(2, "Colibri", "Canada", "Azul y Rojo");
        pajaro.setTipoPico("Puntiagudo");
        pajaro.getTipoPico();
        System.out.println(pajaro.toString());
        pajaro.volar();
        pajaro.recolectarRamas();
        pajaro.comer();

    }
}
************************************************************************************************************************************************
package Zoologico;

public class Animal {
    private String nombre,origen,color;
    public Animal() {
    }
    public Animal(String nombre, String origen, String color) {
        this.nombre = nombre;
        this.origen = origen;
        this.color = color;
    }
    public String getNombre() {
        return nombre;
    }
    public String getOrigen() {
        return origen;
    }
    public String getColor() {
        return color;
    }
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
    public void setOrigen(String origen) {
        this.origen = origen;
    }
    public void setColor(String color) {
        this.color = color;
    }
    public void sonido(String sonido) {
        System.out.println("Sonido:"+sonido); 
    }
    public void comer() {
        System.out.println("Este animal come");
    }
    @Override
    public String toString() {
        return super.toString()+ "Animal{" + "nombre=" + nombre +
                ", origen=" + origen + ", color=" + color + '}';
    }
}
***************************************************************************************************************************************************************
package Zoologico;


public class AnimalAcuatico extends Animal {
    private int numeroAletas;

    public AnimalAcuatico() {
    }
     

    public AnimalAcuatico(int numeroAletas, String nombre, String origen, String color) {
        super(nombre, origen, color);
        this.numeroAletas = numeroAletas;
        
        
    }

    public int getNumeroAletas() {
        return numeroAletas;
    }

    public void setNumeroAletas(int numeroAletas) {
        this.numeroAletas = numeroAletas;
    }
    
    @Override
    public void comer() {
        System.out.println("La ballena come peces");
    }
    public void nadar(){
        System.out.println("La ballena nada mucho en verano");
    }

    @Override
    public String toString() {
        return super.toString()+"AnimalAcuatico{" + "numeroAletas=" + numeroAletas + '}';
    }
    
    
}
**********************************************************************************************************************************************************************
package Zoologico;

public class AnimalAereo extends Animal {

    private int numeroAlas;

    public AnimalAereo(int numeroAlas, String nombre, String origen, String color) {
        super(nombre, origen, color);
        this.numeroAlas = numeroAlas;
    }

    public int getNumeroAlas() {
        return numeroAlas;
    }

    public void setNumeroAlas(int numeroAlas) {
        this.numeroAlas = numeroAlas;
    }

    public void volar() {
        System.out.println("El colibri vuela muy rapido");
    }

    @Override
    public void comer() {
        System.out.println("Los colibris comen flores y algunos insectos pequeños");
    }

    @Override
    public String toString() {
        return super.toString() + "AnimalAereo{" + "numeroAlas=" + numeroAlas + '}';
    }

}

*****************************************************************************************************************************************************************
package Zoologico;


public class AnimalTerrestre extends Animal{
    private int numeroPatas;

    public AnimalTerrestre(int numeroPatas, String nombre, String origen, String color) {
        super(nombre, origen, color);
        this.numeroPatas = numeroPatas;
    }

    public int getNumeroPatas() {
        return numeroPatas;
    }

    public void setNumeroPatas(int numeroPatas) {
        this.numeroPatas = numeroPatas;
    }
           
    public void correr(){
        System.out.println("El perro corre muy rapido");
    }
    @Override
    public void comer(){
        System.out.println("El perro come croquetas y pollo");
    }

    @Override
    public String toString() {
        return super.toString()+ "AnimalTerrestre{" + "numeroPatas=" + numeroPatas + '}';
    }
    
}

***********************************************************************************************************************************************************************
package Zoologico;

public class Ballena extends AnimalAcuatico {

    private int largo;

    public Ballena(int numeroAletas, String nombre, String origen, String color, int largo) {
        super(numeroAletas, nombre, origen, color);
        this.largo = largo;
    }

    public int getLargo() {
        return largo;
    }

    public void setLargo(int largo) {
        this.largo = largo;
    }

    public void pelearConPinocho() {
        System.out.println("Se comio a pinocho :(");
    }

    @Override
    public String toString() {
        return super.toString() + "Ballena{" + "largo=" + largo + '}';
    }
}
********************************************************************************************************************************************************************************
package Zoologico;

public class Pajaro extends AnimalAereo {

    private String tipoPico;

    public Pajaro(int numeroAlas, String nombre, String origen, String color) {
        super(numeroAlas, nombre, origen, color);
    }

    public String getTipoPico() {
        return tipoPico;
    }

    public void setTipoPico(String tipoPico) {
        this.tipoPico = tipoPico;
    }

    public void recolectarRamas() {
        System.out.println("El colibri recolecta ramas para hacer su nido");
    }

    @Override
    public String toString() {
        return super.toString() + "Pajaro{" + "tipoPico=" + tipoPico + '}';
    }

}
***************************************************************************************************************************************************************************
package Zoologico;

public class Perro extends AnimalTerrestre {

    private String colorCollar;

    public Perro(int numeroPatas, String nombre, String origen, String color) {
        super(numeroPatas, nombre, origen, color);
    }

    public String getColorCollar() {
        return colorCollar;
    }

    public void setColorCollar(String colorCollar) {
        this.colorCollar = colorCollar;
    }

    public void hacerTrucos() {
        System.out.println("Se hace el muerto y saluda con la patita");
    }

    @Override
    public String toString() {
        return super.toString() + "Perro{" + "colorCollar=" + colorCollar + '}';
    }

}
