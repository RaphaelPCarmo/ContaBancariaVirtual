
# 🏦 Desafio Java - Simulação de Conta Bancária

Este projeto em **Java** simula um pequeno sistema bancário com funcionalidades básicas de uma conta corrente.  
Ele foi desenvolvido para praticar conceitos fundamentais de **entrada de dados, estrutura condicional e laços de repetição**.

---

## 🚀 Funcionalidades
- Consultar saldo atual  
- Transferir valores (com verificação de saldo)  
- Receber valores (depósito)  
- Encerrar o programa  

---

## 💻 Tecnologias utilizadas
- **Java 17+**  
- **Scanner (entrada de dados via console)**  

---

## 🧠 Conceitos praticados
- Estruturas condicionais (`if / else if / else`)  
- Estruturas de repetição (`while`)  
- Manipulação de variáveis e tipos primitivos  
- Interação com o usuário via console  

---

## ▶️ Como executar
1. Clone o repositório:  
   ```bash
   git clone https://github.com/raphaelperimdocarmo/desafio-java-conta-bancaria.git
````

2. Compile o código:

   ```bash
   javac Desafio.java
   ```
3. Execute:

   ```bash
   java Desafio
   ```

---

## 📦 Código-fonte (Desafio.java)

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
        System.out.println("\nNome do cliente: " + nome);
        System.out.println("Tipo conta: " + tipoConta);
        System.out.println("Saldo atual: " + saldo);
        System.out.println("\n************************");

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

            if (opcao == 1) {
                System.out.println("O saldo atualizado é: " + saldo);
            } else if (opcao == 2) {
                System.out.println("Qual valor deseja transferir?");
                double valor = leitura.nextDouble();
                if (valor > saldo) {
                    System.out.println("Não há saldo suficiente para a transferência.");
                } else {
                    saldo -= valor;
                    System.out.println("Novo saldo: " + saldo);
                }
            } else if (opcao == 3) {
                System.out.println("Valor recebido: ");
                double valor = leitura.nextDouble();
                saldo += valor;
                System.out.println("Novo saldo: " + saldo);
            } else if (opcao != 4) {
                System.out.println("Resposta inválida.");
            }
        }

        leitura.close();
        System.out.println("Programa encerrado. Obrigado por utilizar o sistema!");
    }
}
```

---

## 📸 Exemplo de execução

```
**************************
Nome do cliente: Clark Kent
Tipo conta: Corrente
Saldo atual: 2599.99
**************************

DIGITE SUA OPÇÃO
1 - Consultar saldo
2 - Transferir valor
3 - Receber valor
4 - Sair
```

---

## 👨‍💻 Autor

**Raphael Perim do Carmo**
📚 Estudante de Ciência da Computação
💼 Buscando oportunidades em tecnologia e desenvolvimento de software

🔗 [LinkedIn - Raphael Perim do Carmo](https://www.linkedin.com/in/raphaelperimdocarmo)
