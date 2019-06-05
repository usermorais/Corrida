# Corrida
Resultados para corrida com o ranking dos Pilotos

Crie um arquivo SUAS-INSTRUÇÕES.txt para adicionar algum comentário/observação que achar importante;

Comentarei o projeto no README também :).

Os códigos em SQL para gerar os resultados estão nos arquivos:
- "Script Pilotos.sql" ou
- "Script Pilotos.txt"

Segue passos importantes para entender a linha de raciocínio utilizada na solução.

1 - Criamos uma tabela para receber os dados com o mesmo número de campos que o arquivo de log oferece.
2 - Os dados do arquivo LOG foram formatados manualmente para realizar o UPLOAD na tabela (INSERT).
3 - Obs.: Como o arquivo de LOG não possui uma separação de campos lógica (campos separados por ";", "TAB", ",", ETC.), não fizemos a importação automática direto de um arquivo "TXT". O que seria correto pensando em automatizar a leitura dos resultados em novos arquivos de LOG (O ideal, seria ajustar o gerador do arquivo de LOG para respeitar uma formatação padrão).
4 - Criamos uma consulta Recursiva (para gerar o ranking dos pilotos) e uma consulta (com subconsultas) para gerar os cálculos dos resultados solicitados, evitando criação de novos campos na tabela ou de uma procedure apenas para mostrar os dados solicitados.
5 - Com apenas a consulta disponível, basta utiliza-la em qualquer sistema direto ou a mesma dentro de uma VIEW para trazer os dados solicitados.
