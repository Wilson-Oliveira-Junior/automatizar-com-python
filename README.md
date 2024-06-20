# Convertendo Arquivo Excel para Script SQL
# Este script Python foi desenvolvido para ler um arquivo Excel e gerar um script SQL que pode ser utilizado para inserir os dados do Excel em um banco de dados.

### Dependências
pandas: Utilizado para carregar e manipular dados do arquivo Excel.
tqdm: Fornece uma barra de progresso durante o processamento dos dados.
Funcionalidade
O script contém uma função principal gerar_script_sql que realiza as seguintes etapas:

## Leitura do Arquivo Excel

Utiliza o pandas para carregar o arquivo Excel especificado (arquivo_excel).
Geração do Script SQL

## Cria um script SQL de inserção na tabela especificada (nome_tabela).
Itera pelas linhas do DataFrame do pandas para converter cada linha em uma linha de valores no script SQL.
Progresso de Conversão

Utiliza tqdm para exibir uma barra de progresso que mostra o status da conversão.
Escrita do Script SQL

## Remove a vírgula extra da última linha e adiciona um ponto e vírgula no final do script SQL gerado.
Escreve o script SQL em um arquivo no caminho especificado (caminho_output_sql).
Exemplo de Uso
Para usar este script:

Preencha as variáveis arquivo_excel, nome_tabela, e caminho_output_sql com os valores apropriados.
Execute o script Python.
Nota: Certifique-se de ter o pandas e tqdm instalados antes de executar o script.

## Exemplo de Chamada:
python
Copiar código
arquivo_excel = r'C:\caminho\para\arquivo.xlsx'
nome_tabela = 'mytable'
caminho_output_sql = r'C:\caminho\para\output.sql'

gerar_script_sql(arquivo_excel, nome_tabela, caminho_output_sql)
Saída Esperada
Após a execução bem-sucedida, o script irá imprimir uma mensagem indicando onde o script SQL foi salvo.

css
Copiar código
Script SQL gerado com sucesso e salvo em C:\caminho\para\output.sql!
