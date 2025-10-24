
# 🔢 Desafio Java - Simulação de Conta Bancária

Um sistema simples em **Java** que permite ao usuário consultar saldo, transferir e receber valores em uma conta corrente.  
Este projeto é ideal para praticar lógica de programação, estruturas condicionais e laços de repetição.

### Built with

* ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
* ![Scanner](https://img.shields.io/badge/Scanner-Blue?style=for-the-badge)

<h2> ✨ Funcionalidades </h2>

- 🔄 Consultar saldo atualizado
- 💸 Transferir valores (com verificação de saldo)
- 💰 Receber valores (depósito)
- 🚪 Sair do sistema

<h2> 🚀 Como Executar o Projeto </h2>

• Clone o repositório:  
```bash
git clone https://github.com/raphaelperimdocarmo/desafio-java-conta-bancaria.git
````

• Compile o código:

```bash
javac Desafio.java
```

• Execute o programa:

```bash
java Desafio
```

<h2> 📦 Código-fonte (Desafio.java) </h2>

```java
import java.util.Scanner;

public class Desafio {
    public static void main(String[] args) {
        String nome = "Clark Kent";
        String tipoConta = "Corrente";
        double saldo = 2599.99;
        int opcao = 0;
        Scanner leitura = new Scanner(System.in);

        System.out.println("**************************");
        System.out.println("Nome: " + nome);
        System.out.println("Conta: " + tipoConta);
        System.out.println("Saldo: " + saldo);
        System.out.println("************************");

        String menu = """
            DIGITE SUA OPÇÃO
            1 - Consultar saldo
            2 - Transferir valor
            3 - Receber valor
            4 - Sair
        """;

        while (opcao != 4) {
            System.out.println(menu);
            opcao = leitura.nextInt();

            switch(opcao) {
                case 1 -> System.out.println("Saldo atualizado: " + saldo);
                case 2 -> {
                    System.out.println("Valor para transferir:");
                    double valor = leitura.nextDouble();
                    if (valor > saldo) System.out.println("Saldo insuficiente.");
                    else { saldo -= valor; System.out.println("Novo saldo: " + saldo); }
                }
                case 3 -> {
                    System.out.println("Valor recebido:");
                    double valor = leitura.nextDouble();
                    saldo += valor;
                    System.out.println("Novo saldo: " + saldo);
                }
                case 4 -> System.out.println("Encerrando o sistema...");
                default -> System.out.println("Opção inválida!");
            }
        }
        leitura.close();
    }
}
```

<h2> 🎯 Objetivo do Projeto </h2>

Este projeto foi criado com o objetivo de praticar:

🧩 Lógica de programação em Java
🔄 Estruturas condicionais e laços de repetição
💻 Interação com o usuário via console

<h2> 📝 Licença </h2>

Este projeto é de uso livre e sem fins comerciais.
Sinta-se à vontade para estudar, modificar e compartilhar! 🚀

<h2> 👤 Criado por </h2>
<img src="https://github.com/RaphaelPCarmo.png" width="120" style="border-radius: 30%"><br>

<strong>Raphael Perim do Carmo</strong>

<table align="center">
  <tr>
    <td align="center">
      <a href="https://www.linkedin.com/in/raphael-perim-do-carmo-512166315">
        <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/RaphaelPCarmo">
        <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
      </a>
    </td>
    <td align="center">
      <a href="mailto:raphael.perim123@gmail.com">
        <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/>
      </a>
    </td>
  </tr>
</table>

