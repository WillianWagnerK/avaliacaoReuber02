package avaliacaoreuber02;

import javax.swing.JOptionPane;

public class avaliacaoReuber02 {

    static String[] produtos = new String[5];
    static int[] valores = new int[5];
    static int vendas[][] = new int[12][5];
    static String[] meses = new String[]{"Janeiro", "Fevereiro", "Março", "Abril", "Maio", "Junho", "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"};
    static String[] prd = new String[]{"primeiro", "segundo", "terceiro", "quarto", "quinto"};

    public static void main(String[] args) {

        menu();

    }

    public static void menu() {

        int opcao;

        do {
            opcao = Integer.parseInt(JOptionPane.showInputDialog("Digite a opção desejada:"
                    + "\n\t1 - Adicionar Produtos "
                    + "\n\t2 - Exibir todos os produtos com vendas mensais "
                    + "\n\t3 - Exibir todos os produtos com valores de vendas mensais "
                    + "\n\t4 - Exibir o preço médio anual de venda de cada produto"
                    + "\n\t5 - Exibir todos os produtos, os valores unitários, e o mês com mais vendas "
                    + "\n\t6 - Sair "));

            switch (opcao) {
                case 1:
                    adicionar();

                    break;

                case 2:
                    produtosevendas();

                    break;

                case 3:
                    produtosevalores();

                    break;

                case 4:
                    valormedioanual();

                    break;

                case 5:
                    maiorDaColuna(5, vendas);

                    break;

                default:
                    JOptionPane.showMessageDialog(null, "Opção Inválida!");
            }

        } while (opcao != 6);
    }

    public static void adicionar() {
      
        for (int k = 0; k < 5; k++) {
            produtos[k] = JOptionPane.showInputDialog("Adicionando o " + prd[k] + " produto \n\tDigite o nome do produto.");           
            valores[k] = Integer.parseInt(JOptionPane.showInputDialog("Qual o valor unitário deste produto?"));

            for (int i = 0; i < 11; i++) {
                vendas[i][k] = Integer.parseInt(JOptionPane.showInputDialog("Digite as vendas do mês de " + meses[i]));
                              
            }
        }

        
    }

    public static void produtosevendas() {

        int prd = 0;
        for (int k = 0; k < 5; k++) {

            System.out.println("Produto " + produtos[k] + " e suas vendas mensais.");
            for (int i = 0; i < 11; i++) {
                System.out.println(meses[i] + ":" + vendas[i][k]);

            }
            System.out.println("--------------------------");
        }

    }

    public static void produtosevalores() {
        System.out.println("Produto " + produtos[0] + " e seus valores de vendas mensais");
        System.out.println(vendas[0][0] * valores[0] + vendas[1][0] * valores[0] + vendas[2][0] * valores[0] + vendas[3][0] * valores[0] + vendas[4][0] * valores[0] + vendas[5][0] * valores[0] + vendas[6][0] * valores[0] + vendas[7][0] * valores[0] + vendas[8][0] * valores[0] + vendas[9][0] * valores[0] + vendas[10][0] * valores[0] + vendas[11][0] * valores[0]);
        System.out.println("----------------------------");
        System.out.println("Produto " + produtos[1] + " e seus valores de vendas mensais");
        System.out.println(vendas[0][1] * valores[1] + vendas[1][1] * valores[1] + vendas[2][1] * valores[1] + vendas[3][1] * valores[1] + vendas[4][1] * valores[1] + vendas[5][1] * valores[1] + vendas[6][1] * valores[1] + vendas[7][1] * valores[1] + vendas[8][1] * valores[1] + vendas[9][1] * valores[1] + vendas[10][1] * valores[1] + vendas[11][1] * valores[1]);
        System.out.println("----------------------------");
        System.out.println("Produto " + produtos[2] + " e seus valores de vendas mensais");
        System.out.println(vendas[0][2] * valores[2] + vendas[1][2] * valores[2] + vendas[2][2] * valores[2] + vendas[3][2] * valores[2] + vendas[4][2] * valores[2] + vendas[5][2] * valores[2] + vendas[6][2] * valores[2] + vendas[7][2] * valores[2] + vendas[8][2] * valores[2] + vendas[9][2] * valores[2] + vendas[10][2] * valores[2] + vendas[11][2] * valores[2]);
        System.out.println("----------------------------");
        System.out.println("Produto " + produtos[3] + " e seus valores de vendas mensais");
        System.out.println(vendas[0][3] * valores[3] + vendas[1][3] * valores[3] + vendas[2][3] * valores[3] + vendas[3][3] * valores[3] + vendas[4][3] * valores[3] + vendas[5][3] * valores[3] + vendas[6][3] * valores[3] + vendas[7][3] * valores[3] + vendas[8][3] * valores[3] + vendas[9][3] * valores[3] + vendas[10][3] * valores[3] + vendas[11][3] * valores[3]);
        System.out.println("----------------------------");
        System.out.println("Produto " + produtos[4] + " e seus valores de vendas mensais");
        System.out.println(vendas[0][4] * valores[4] + vendas[1][4] * valores[4] + vendas[2][4] * valores[4] + vendas[3][4] * valores[4] + vendas[4][4] * valores[4] + vendas[5][4] * valores[4] + vendas[6][4] * valores[4] + vendas[7][4] * valores[4] + vendas[8][4] * valores[4] + vendas[9][4] * valores[4] + vendas[10][4] * valores[4] + vendas[11][4] * valores[4]);
        System.out.println("----------------------------");

    }

    public static void valormedioanual() {
        float media1;
        float media2;
        float media3;
        float media4;
        float media5;

        media1 = (vendas[0][0] + vendas[1][0] + vendas[2][0] + vendas[3][0] + vendas[4][0] + vendas[5][0] + vendas[6][0] + vendas[7][0] + vendas[8][0] + vendas[9][0] + vendas[10][0] + vendas[11][0]) * valores[0] / 12;
        System.out.println(media1);
        System.out.println("O preço médio anual de venda do produto " + produtos[0] + " é de " + media1 + " reais.");
        System.out.println("--------------------------");

        media2 = (vendas[0][1] + vendas[1][1] + vendas[2][1] + vendas[3][1] + vendas[4][1] + vendas[5][1] + vendas[6][1] + vendas[7][1] + vendas[8][1] + vendas[9][1] + vendas[10][1] + vendas[11][1]) * valores[0] / 12;
        System.out.println(media2);
        System.out.println("O preço médio anual de venda do produto " + produtos[1] + " é de " + media2 + " reais.");
        System.out.println("--------------------------");

        media3 = (vendas[0][2] + vendas[1][2] + vendas[2][2] + vendas[3][2] + vendas[4][2] + vendas[5][2] + vendas[6][2] + vendas[7][2] + vendas[8][2] + vendas[9][2] + vendas[10][2] + vendas[11][2]) * valores[0] / 12;
        System.out.println(media3);
        System.out.println("O preço médio anual de venda do produto " + produtos[2] + " é de " + media3 + " reais.");
        System.out.println("--------------------------");

        media4 = (vendas[0][3] + vendas[1][3] + vendas[2][3] + vendas[3][3] + vendas[4][3] + vendas[5][3] + vendas[6][3] + vendas[7][3] + vendas[8][3] + vendas[9][3] + vendas[10][3] + vendas[11][3]) * valores[0] / 12;
        System.out.println(media4);
        System.out.println("O preço médio anual de venda do produto " + produtos[3] + " é de " + media4 + " reais.");
        System.out.println("--------------------------");

        media5 = (vendas[0][4] + vendas[1][4] + vendas[2][4] + vendas[3][4] + vendas[4][4] + vendas[5][4] + vendas[6][4] + vendas[7][4] + vendas[8][4] + vendas[9][4] + vendas[10][4] + vendas[11][4]) * valores[0] / 12;
        System.out.println(media5);
        System.out.println("O preço médio anual de venda do produto " + produtos[4] + " é de " + media5 + " reais.");
        System.out.println("--------------------------");

    }

    public static void maiorDaColuna(int linhas, int[][] vendas) {
        int arr[] = new int[5];
        int x = 0;

        for (int i = 0; i < linhas; i++) { // as linhas são 5 no caso

            int m = vendas[0][i];
            for (int j = 1; j < vendas[i].length; j++) {
                if (vendas[j][i] > m) {
                    m = vendas[j][i];
                }
            }

            arr[x] = m;
            x++;

        }

        for (int z = 0; z < 5; z++) {
            for (int i = 0; i < 11; i++) {
                if (arr[z] == vendas[i][z]) {

                    System.out.println("Produto: " + produtos[z] + "\n\tValor unitário: " + valores[z] + "\n\tO Mês com maior desempenho desse produto foi em " + meses[i] + " com número de vendas = " + arr[z]);

                }

            }

        }

    }

}
