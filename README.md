# atividade-1
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("===== MENU =====");
        Console.WriteLine("1 - Maior número");
        Console.WriteLine("2 - Maior de idade");
        Console.WriteLine("3 - Média das notas");
        Console.WriteLine("4 - Par ou Ímpar");
        Console.WriteLine("5 - Tabuada");
        Console.Write("Escolha uma opção: ");

        int opcao = int.Parse(Console.ReadLine());

        switch (opcao)
        {
            case 1:
                Console.Write("Digite o primeiro número: ");
                double n1 = double.Parse(Console.ReadLine());

                Console.Write("Digite o segundo número: ");
                double n2 = double.Parse(Console.ReadLine());

                if (n1 > n2)
                    Console.WriteLine($"O maior número é {n1}");
                else if (n2 > n1)
                    Console.WriteLine($"O maior número é {n2}");
                else
                    Console.WriteLine("Os dois números são iguais.");
                break;

            case 2:
                Console.Write("Digite sua idade: ");
                int idade = int.Parse(Console.ReadLine());

                if (idade >= 18)
                    Console.WriteLine("Você é maior de idade.");
                else
                    Console.WriteLine("Você é menor de idade.");
                break;

            case 3:
                Console.Write("Nota 1: ");
                double nota1 = double.Parse(Console.ReadLine());

                Console.Write("Nota 2: ");
                double nota2 = double.Parse(Console.ReadLine());

                Console.Write("Nota 3: ");
                double nota3 = double.Parse(Console.ReadLine());

                double media = (nota1 + nota2 + nota3) / 3;

                Console.WriteLine($"Média: {media:F2}");

                if (media >= 7)
                    Console.WriteLine("Aprovado!");
                else if (media >= 5)
                    Console.WriteLine("Recuperação!");
                else
                    Console.WriteLine("Reprovado!");
                break;

            case 4:
                Console.Write("Digite um número: ");
                int numero = int.Parse(Console.ReadLine());

                switch (numero % 2)
                {
                    case 0:
                        Console.WriteLine("Par");
                        break;

                    default:
                        Console.WriteLine("Ímpar");
                        break;
                }
                break;

            case 5:
                Console.Write("Digite um número inteiro positivo: ");
                int numeroInteiro = int.Parse(Console.ReadLine());

                if (numeroInteiro > 0)
                {
                    for (int i = 1; i <= 10; i++)
                    {
                        Console.WriteLine($"{numeroInteiro} x {i} = {numeroInteiro * i}");
                    }
                }
                else
                {
                    Console.WriteLine("Digite um número positivo.");
                }
                break;

            default:
                Console.WriteLine("Opção inválida.");
                break;
        }
    }
}
