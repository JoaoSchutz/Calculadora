Calculadora em C#

O projeto consiste na criação de uma calculadora (que realiza as 4 operações) para fins de atividade da matéria Programming and Data Persistence (Univali). 

Após adicionar todos os buttons correspondentes aos números de 0 a 9 e os botões que chamariam as operações aritméticas como, por exemplo, a operação soma:


----------------------------------------------------------------------------------------------------------------------------------------------------
 O Botão da soma realiza uma estrutura if/else que quando o usuário coloca o valor e clica em +, um label mostra o sinal positivo.
 
        private void button4_Click(object sender, EventArgs e)
        {
            if (txtResultado.Text != "")
            { 
            valor1 = decimal.Parse(txtResultado.Text, CultureInfo.InvariantCulture);
            txtResultado.Text = "";
            operacao = "SOMA";
            lblOperacao.Text = "+";
            }
            else
            {
                MessageBox.Show("Informe um valor para somar.");
            }
        }
----------------------------------------------------------------------------------------------------------------------------------------------------



----------------------------------------------------------------------------------------------------------------------------------------------------
Em seguida, o botão de total captura o valor inserido e chama a operação, também por uma estrutura if/else:

        private void button16_Click(object sender, EventArgs e)
        {
            valor2 = decimal.Parse(txtResultado.Text, CultureInfo.InvariantCulture);

            if (operacao == "SOMA")
            {
                txtResultado.Text = Convert.ToString(valor1 + valor2);
            } else if (operacao == "SUB")
            {
                txtResultado.Text = Convert.ToString(valor1 - valor2);
            } else if (operacao == "DIV")
            {
                txtResultado.Text = Convert.ToString(valor1 / valor2);
            } else if (operacao == "MULT")
            {
                txtResultado.Text = Convert.ToString(valor1 * valor2);
            }
        }
-----------------------------------------------------------------------------------------------------------------------------------------------------
