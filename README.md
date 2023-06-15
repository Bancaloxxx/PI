import java.util.Scanner;

public class PI {
    static Scanner input = new Scanner(System.in);
    static Random random = new Random();
    static int opcao;
    static int chances;

 static int boasVindas() {
        do {
            System.out.println("1 - Instruções")
            System.out.println("3 - Créditos");
            System.out.println("4 - Sair");
            System.out.print("Escolha uma opcao: ");
            opcao = input.nextInt();
            switch (opcao) {
                case 1:
                    System.out.println("Você escolheu a opcao Instruções");
                    return 1;
                case 2:
                    System.out.println("Você escolheu a opcao Jogar");
                    return 2;
                case 3:
                    System.out.println("Você escolheu a opcao Créditos");
                    return 3;
                case 4:
                    return 4;
                default:
                    System.out.println("opcao inválida!");
            }
        } while (opcao < 1 || opcao > 4);
        return opcao;
    }

    static void instruções() {
        do {
            System.out.println("Instruções");
            System.out.println("1 - Jogar o jogo");
            System.out.println("2 - Voltar ao menu principal");
            System.out.print("Escolha uma opcao: ");
            opcao = input.nextInt();
            switch (opcao) {
                case 1:
                    System.out.println("Você escolheu a opcao Jogar o jogo");
                    break;
                case 2:
                    System.out.println("Você escolheu a opcao Voltar ao menu principal");
                    primeiraEtapa();
                    break;
                default:
                    System.out.println("opcao inválida!");
            }
        } while (opcao != 1 && opcao != 2);
    }

    static void creditos() {
        do {
            System.out.println("Augusto Henrique Ramos Bitiano Giovanna Bancala Gabriela Aruda Samuel Silva");
            System.out.println("1 - Voltar ao menu principal");
            System.out.println("2 - Sair");
            System.out.print("Escolha uma opcao: ");
            opcao = input.nextInt();
            switch (opcao) {
                case 1:
                    System.out.println("Você escolheu a opcao Voltar ao menu principal");
                    primeiraEtapa();
                    break;
                case 2:
                    sair();
                    break;
                default:
                    System.out.println("opcao inválida!");
            }
        } while (opcao != 1 && opcao != 2);
    }

    static void sair() {
        System.out.println("Você escolheu a opcao Sair");
    }

    static void primeiraEtapa() {
        opcao = boasVindas();
        switch (opcao) {
            case 1:
                instruções();
                break;
            case 2:
                comecoJogo();
                break;
            case 3:
                creditos();
                break;
            case 4:
                sair();
                break;
            default:
                System.out.println("opcao inválida!");
        }
    }

    static void comecoJogo() {
        chances = 5;
        System.out.println("Bem vindo ao Jogo!");
        System.out.println("Historia do jogo...");
        funcaoQueSorteiaFuncao1();
    }

    static void opcoesDoJogo() {
        do {
            System.out.println("1 - Continua");
            System.out.println("2 - Sair");
            opcao = input.nextInt();
            switch (opcao) {
                case 1:
                    funcaoQueSorteiaFuncao1();
                    break;
                case 2:
                    sair();
                    break;
                default:
                    break;
            }
        } while (opcao != 1 && opcao != 2);
    }
