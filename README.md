<!DOCTYPE html>
<html>
<body>

<h1>Agenda de Contatos</h1>

<h2>Código ainda em desenvolvimento</h2>

<p>Este repositório contém um script Python para gerenciar uma agenda de contatos. O script permite adicionar novos contatos, armazenando informações como nome, número de telefone e e-mail, e exibe a lista completa de contatos ao final.</p>

<h2>Código do Projeto</h2>
<pre>
<code>
import pandas as pd

print("Bem-vindo à sua agenda de contatos.")

mostrar_agenda = pd.DataFrame()

def adicionar_contato(mostrar_agenda):

    nome = input("Digite o nome do contato: ")
    numero = input("Digite o número do contato: ")
    email = input("Digite o e-mail do contato: ")
    
    novo_contato = pd.DataFrame({"Nome": [nome], "Número": [numero], "E-mail": [email]})
    mostrar_agenda = pd.concat([mostrar_agenda, novo_contato], ignore_index=True)
        
    return mostrar_agenda


while True:
    continuar = input("Deseja adicionar um contato? (s/n): ")
    
    if continuar.lower() == 'n':
        break
    
    elif continuar.lower() not in "sn":
        print("Resposta inválida. Por favor, responda apenas com 's' ou 'n'.")
    
    elif continuar.lower() == "s":
        mostrar_agenda = adicionar_contato(mostrar_agenda)

print(mostrar_agenda)
</code>
</pre>

<h2>Estrutura do Código</h2>

<p>O código está organizado para facilitar a adição de contatos em uma agenda, utilizando a biblioteca pandas para manipulação de dados.</p>

<h3>Lista de Funções</h3>
<ul>
    <li><strong>adicionar_contato(mostrar_agenda)</strong>
        <ul>
            <li>Solicita ao usuário o nome, número de telefone e e-mail do contato.</li>
            <li>Adiciona o novo contato à agenda existente.</li>
            <li>Retorna a agenda atualizada.</li>
        </ul>
    </li>
</ul>

<h2>Requisitos do Sistema</h2>
<p>Para rodar a aplicação, são necessários os seguintes requisitos do sistema:</p>
<ul>
    <li><strong>Sistema Operacional:</strong> Windows 7 ou superior, macOS 10.13 ou superior, ou distribuições Linux modernas.</li>
    <li><strong>Python:</strong> Python 3.6 ou superior.</li>
    <li><strong>Bibliotecas Python:</strong> pandas.</li>
</ul>

<h2>Execução</h2>
<p>Para executar o script de agenda de contatos utilizando o Visual Studio Code (VSCode), siga os passos abaixo:</p>
<ol>
    <li>Abra o Visual Studio Code.</li>
    <li>Certifique-se de que a extensão do Python está instalada no VSCode. Caso não esteja, você pode instalá-la a partir da aba de extensões.</li>
    <li>Baixe o script Python do repositório e salve-o em um diretório de sua escolha.</li>
    <li>No VSCode, clique em <strong>File</strong> > <strong>Open Folder</strong> e navegue até o diretório onde o script foi salvo. Abra esse diretório.</li> 
    <li>Clique duas vezes no arquivo do script para abri-lo no editor.</li>
    <li>Com o arquivo aberto, clique no botão "Run" no canto superior direito (Símbolo de "Play") ou pressione <code>F5</code> para executar o script.</li>
</ol>

<h2>Exemplo de Uso</h2>
<ol>
    <li>O usuário será saudado com uma mensagem de boas-vindas à agenda de contatos.</li>
    <li>O usuário será solicitado a inserir o nome, número de telefone e e-mail de um contato.</li>
    <li>Após adicionar um contato, o programa perguntará se deseja adicionar outro contato.</li>
    <li>O usuário pode continuar adicionando contatos até decidir parar, digitando 'n'.</li>
    <li>Ao finalizar, a lista completa de contatos será exibida.</li>
</ol>

<h2>Contribuição</h2>
<p>Se você quiser contribuir para este projeto, sinta-se à vontade para abrir um pull request ou relatar problemas no repositório.</p>

<h2>Licença</h2>
<p>Este projeto está licenciado sob a <a href="https://opensource.org/licenses/MIT">MIT License</a>.</p>

</body>
</html>
