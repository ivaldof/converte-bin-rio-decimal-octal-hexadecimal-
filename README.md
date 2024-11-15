
1. Binário para Decimal:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.print("Digite um número binário (use ponto para fracionários, ex: 101.101): ");
        String numeroBinario = ler.nextLine();
        
        // Dividir o número em parte inteira e fracionária
        String[] partes = numeroBinario.split("\\.");
        String parteInteira = partes[0];
        String parteFracionaria = partes.length > 1 ? partes[1] : "";

        // Converter a parte inteira do binário para decimal
        int numeroDecimalInteiro = Integer.parseInt(parteInteira, 2);

        // Converter a parte fracionária do binário para decimal
        double numeroDecimalFracionario = 0;
        for (int i = 0; i < parteFracionaria.length(); i++) {
            if (parteFracionaria.charAt(i) == '1') {
                numeroDecimalFracionario += Math.pow(2, -(i + 1));
            }
        }

        // Resultado final: soma da parte inteira e fracionária
        double numeroDecimal = numeroDecimalInteiro + numeroDecimalFracionario;
        System.out.println("O número decimal é: " + numeroDecimal);
    }
}

           

2. Decimal para Binário:

import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
    Scanner ler = new Scanner(System.in);
        System.out.println("Digite um número decimal:");
        int numeroDecimal = ler.nextInt();
        
        String numeroBinario = Integer.toBinaryString(numeroDecimal);
        System.out.print("O número binário é: " + numeroBinario);
        
	}
}
            

3. Binário para Octal:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.print("Digite um número binário: ");
        String numeroBinario = ler.nextLine();

        // Preencher à esquerda com zeros se o comprimento não for múltiplo de 3
        int padding = 3 - (numeroBinario.length() % 3);
        if (padding != 3) {
            numeroBinario = "0".repeat(padding) + numeroBinario;
        }

        // Converter o binário em octal
        StringBuilder numeroOctal = new StringBuilder();
        for (int i = 0; i < numeroBinario.length(); i += 3) {
            String grupo = numeroBinario.substring(i, i + 3);
            int valorOctal = Integer.parseInt(grupo, 2);
            numeroOctal.append(valorOctal);
        }

        System.out.println("O número octal é: " + numeroOctal);
    }
}

            

4. Octal para Binário:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.print("Digite um número octal: ");
        String numeroOctal = ler.nextLine();

        StringBuilder numeroBinario = new StringBuilder();
        
        for (char digitoOctal : numeroOctal.toCharArray()) {
            int valorDecimal = Character.getNumericValue(digitoOctal);
            String binario = Integer.toBinaryString(valorDecimal);

            // Preencher com zeros à esquerda para garantir 3 bits
            while (binario.length() < 3) {
                binario = "0" + binario;
            }
            
            numeroBinario.append(binario);
        }

        System.out.println("O número binário é: " + numeroBinario);
    }
}


            

5. Decimal para Octal:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.println("Digite um número decimal:");
        int numeroDecimal = ler.nextInt();

        // Convertendo para octal
        String numeroOctal = Integer.toOctalString(numeroDecimal);
        System.out.print("O número octal é: " + numeroOctal);
    }
}

            

6. Octal para Decimal:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.println("Digite um número octal:");
        String numeroOctal = ler.nextLine();

        // Convertendo para decimal
        int numeroDecimal = Integer.parseInt(numeroOctal, 8);
        System.out.print("O número decimal é: " + numeroDecimal);
    }
}
           

7. Hexadecimal para Decimal:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.println("Digite um número hexadecimal:");
        String numeroHexadecimal = ler.nextLine();

        // Convertendo para decimal
        int numeroDecimal = Integer.parseInt(numeroHexadecimal, 16);
        System.out.print("O número decimal é: " + numeroDecimal);
    }
}

            

8. Decimal para Hexadecimal:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.print("Digite um número decimal: ");
        int numeroDecimal = ler.nextInt();

        // Converter o número decimal para hexadecimal
        String numeroHexadecimal = Integer.toHexString(numeroDecimal).toUpperCase();

        System.out.println("O número hexadecimal é: " + numeroHexadecimal);
    }
}


            

9. Binário para Hexadecimal:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.println("Digite um número binário:");
        String numeroBinario = ler.nextLine();

        // Convertendo binário para decimal
        int numeroDecimal = Integer.parseInt(numeroBinario, 2);

        // Convertendo decimal para hexadecimal
        String numeroHexadecimal = Integer.toHexString(numeroDecimal).toUpperCase();
        
        System.out.print("O número hexadecimal é: " + numeroHexadecimal);
    }
}

           

10. Hexadecimal para Binário:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        System.out.println("Digite um número hexadecimal:");
        String numeroHexadecimal = ler.nextLine();

        // Convertendo hexadecimal para decimal
        int numeroDecimal = Integer.parseInt(numeroHexadecimal, 16);

        // Convertendo decimal para binário
        String numeroBinario = Integer.toBinaryString(numeroDecimal);
        
        System.out.print("O número binário é: " + numeroBinario);
    }
}

11. de todos para todos:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        
        while (true) {
            System.out.println("Escolha a conversão:");
            System.out.println("1. Binário para Decimal");
            System.out.println("2. Decimal para Binário");
            System.out.println("3. Binário para Octal");
            System.out.println("4. Octal para Binário");
            System.out.println("5. Decimal para Octal");
            System.out.println("6. Octal para Decimal");
            System.out.println("7. Hexadecimal para Decimal");
            System.out.println("8. Decimal para Hexadecimal");
            System.out.println("9. Binário para Hexadecimal");
            System.out.println("10. Hexadecimal para Binário");
            System.out.println("0. Sair");
            System.out.print("Opção: ");
            int opcao = ler.nextInt();
            ler.nextLine(); // Limpar o buffer

            if (opcao == 0) {
                break;
            }

            switch (opcao) {
                case 1: // Binário para Decimal
                    System.out.print("Digite um número binário: ");
                    String binario = ler.nextLine();
                    int decimalFromBinario = Integer.parseInt(binario, 2);
                    System.out.println("Decimal: " + decimalFromBinario);
                    break;

                case 2: // Decimal para Binário
                    System.out.print("Digite um número decimal: ");
                    int numeroDecimal = ler.nextInt();
                    String binarioFromDecimal = Integer.toBinaryString(numeroDecimal);
                    System.out.println("Binário: " + binarioFromDecimal);
                    break;

                case 3: // Binário para Octal
                    System.out.print("Digite um número binário: ");
                    binario = ler.nextLine();
                    decimalFromBinario = Integer.parseInt(binario, 2);
                    String octalFromBinario = Integer.toOctalString(decimalFromBinario);
                    System.out.println("Octal: " + octalFromBinario);
                    break;

                case 4: // Octal para Binário
                    System.out.print("Digite um número octal: ");
                    String octal = ler.nextLine();
                    int decimalFromOctal = Integer.parseInt(octal, 8);
                    String binarioFromOctal = Integer.toBinaryString(decimalFromOctal);
                    System.out.println("Binário: " + binarioFromOctal);
                    break;

                case 5: // Decimal para Octal
                    System.out.print("Digite um número decimal: ");
                    numeroDecimal = ler.nextInt();
                    String octalFromDecimal = Integer.toOctalString(numeroDecimal);
                    System.out.println("Octal: " + octalFromDecimal);
                    break;

                case 6: // Octal para Decimal
                    System.out.print("Digite um número octal: ");
                    octal = ler.nextLine();
                    decimalFromOctal = Integer.parseInt(octal, 8);
                    System.out.println("Decimal: " + decimalFromOctal);
                    break;

                case 7: // Hexadecimal para Decimal
                    System.out.print("Digite um número hexadecimal: ");
                    String hexadecimal = ler.nextLine();
                    int decimalFromHexadecimal = Integer.parseInt(hexadecimal, 16);
                    System.out.println("Decimal: " + decimalFromHexadecimal);
                    break;

                case 8: // Decimal para Hexadecimal
                    System.out.print("Digite um número decimal: ");
                    numeroDecimal = ler.nextInt();
                    String hexadecimalFromDecimal = Integer.toHexString(numeroDecimal).toUpperCase();
                    System.out.println("Hexadecimal: " + hexadecimalFromDecimal);
                    break;

                case 9: // Binário para Hexadecimal
                    System.out.print("Digite um número binário: ");
                    binario = ler.nextLine();
                    decimalFromBinario = Integer.parseInt(binario, 2);
                    String hexadecimalFromBinario = Integer.toHexString(decimalFromBinario).toUpperCase();
                    System.out.println("Hexadecimal: " + hexadecimalFromBinario);
                    break;

                case 10: // Hexadecimal para Binário
                    System.out.print("Digite um número hexadecimal: ");
                    hexadecimal = ler.nextLine();
                    decimalFromHexadecimal = Integer.parseInt(hexadecimal, 16);
                    String binarioFromHexadecimal = Integer.toBinaryString(decimalFromHexadecimal);
                    System.out.println("Binário: " + binarioFromHexadecimal);
                    break;

                default:
                    System.out.println("Opção inválida.");
            }
            System.out.println();
        }
        ler.close();
    }
}
