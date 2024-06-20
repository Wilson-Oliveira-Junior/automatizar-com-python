import pandas as pd
import os
from tqdm import tqdm  # Para mostrar barra de progresso

# Função para ler o arquivo Excel e gerar o script SQL
def gerar_script_sql(arquivo_excel, nome_tabela, caminho_output_sql):
    # Carregar o arquivo Excel
    df = pd.read_excel(arquivo_excel)

    # Gerar o script SQL
    script_sql = f"INSERT INTO {nome_tabela} (Coluna1, Coluna2, ...) VALUES\n"

    total_linhas = len(df)
    with tqdm(total=total_linhas, desc="Convertendo") as pbar:
        for index, row in df.iterrows():
            values = tuple(row.values)
            script_sql += f"    {values},\n"
            pbar.update(1)  # Atualiza a barra de progresso a cada linha processada

    # Remover a vírgula extra da última linha e adicionar o ponto e vírgula final
    script_sql = script_sql.rstrip(',\n') + ';'

    # Escrever o script SQL em um arquivo no caminho especificado
    with open(caminho_output_sql, 'w') as file:
        file.write(script_sql)

    print(f"Script SQL gerado com sucesso e salvo em {caminho_output_sql}!")

# Exemplo de uso
if __name__ == "__main__":
    arquivo_excel = r''  # Caminho para o arquivo Excel
    nome_tabela = 'mytable'
    caminho_output_sql = r''  # Caminho absoluto para o arquivo output.sql

    gerar_script_sql(arquivo_excel, nome_tabela, caminho_output_sql)
