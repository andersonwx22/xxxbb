using System;
using System.Net;
using System.IO;
using System.Windows.Forms;

namespace teste
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            VerificarAtualizacao();
        }

        private void VerificarAtualizacao()
        {
            string currentVersion = "0000xx0000"; // Versão atual do seu programa
            string latestVersion = GetLatestVersionFromGitHub(); // Obtém a versão mais recente do GitHub

            if (latestVersion != currentVersion)
            {
                DialogResult result = MessageBox.Show("Há uma nova versão disponível. Deseja atualizar?", "Atualização Disponível", MessageBoxButtons.YesNo);
                if (result == DialogResult.Yes)
                {
                    DownloadAndInstallUpdate();
                }
            }
            else
            {
                MessageBox.Show("Seu programa está atualizado!");
            }
        }

        private string GetLatestVersionFromGitHub()
        {
            // Implemente o código para acessar seu arquivo de versão no GitHub
            // Exemplo:
            using (WebClient client = new WebClient())
            {
                return client.DownloadString("https://raw.githubusercontent.com/andersonwx22/xxxbb/main/README.md");
            }
        }

        private void DownloadAndInstallUpdate()
        {
            // Implemente o código para baixar e instalar a atualização
            // Exemplo:
            using (WebClient client = new WebClient())
            {
                client.DownloadFile("https://raw.githubusercontent.com/andersonwx22/xxxbb/main/README.md", "teste");
            }

            // Após baixar, extraia os arquivos e substitua os antigos
            // Reinicie o programa após a instalação
        }
    }
}
