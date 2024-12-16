# tipos-de-datos-primitivos
// Autor: [Torres Suni]
// Fecha: [15/12/2024]
// Página: 1

using System;

namespace FigurasGeometricas
{
    // Clase que representa un círculo
    public class Circulo
    {
        private double radio; // Variable privada para almacenar el radio del círculo

        // Constructor de la clase Circulo
        public Circulo(double radio)
        {
            this.radio = radio;
        }

        // Método para calcular el área del círculo
        // CalcularArea utiliza la fórmula: Área = π * radio^2
        public double CalcularArea()
        {
            return Math.PI * Math.Pow(radio, 2);
        }

        // Método para calcular el perímetro del círculo
        // CalcularPerimetro utiliza la fórmula: Perímetro = 2 * π * radio
        public double CalcularPerimetro()
        {
            return 2 * Math.PI * radio;
        }
    }

    // Clase que representa un rectángulo
    public class Rectangulo
    {
        private double largo;  // Variable privada para almacenar el largo del rectángulo
        private double ancho;  // Variable privada para almacenar el ancho del rectángulo

        // Constructor de la clase Rectangulo
        public Rectangulo(double largo, double ancho)
        {
            this.largo = largo;
            this.ancho = ancho;
        }

        // Método para calcular el área del rectángulo
        // CalcularArea utiliza la fórmula: Área = largo * ancho
        public double CalcularArea()
        {
            return largo * ancho;
        }

        // Método para calcular el perímetro del rectángulo
        // CalcularPerimetro utiliza la fórmula: Perímetro = 2 * (largo + ancho)
        public double CalcularPerimetro()
        {
            return 2 * (largo + ancho);
        }
    }

    // Programa principal para probar las clases
    class Program
    {
        static void Main(string[] args)
        {
            // Crear un objeto de la clase Circulo
            Circulo circulo = new Circulo(5); // Radio de 5 unidades
            Console.WriteLine("Círculo:");
            Console.WriteLine($"Área: {circulo.CalcularArea():F2}");
            Console.WriteLine($"Perímetro: {circulo.CalcularPerimetro():F2}");

            // Crear un objeto de la clase Rectangulo
            Rectangulo rectangulo = new Rectangulo(4, 6); // Largo de 4 unidades, ancho de 6 unidades
            Console.WriteLine("\nRectángulo:");
            Console.WriteLine($"Área: {rectangulo.CalcularArea():F2}");
            Console.WriteLine($"Perímetro: {rectangulo.CalcularPerimetro():F2}");
        }
    }
}
