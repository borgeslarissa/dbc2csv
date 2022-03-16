# dbc2csv
Conversão de arquivo .dbc para .csv usando R


#os arquivos utilizados são disponibilizados pela plataforma DataSus do Ministério da Sáude

Primeiro passo
- Consulta aos arquivos em: https://datasus.saude.gov.br/transferencia-de-arquivos/
- Pensar o nome do objeto onde vai colocar a informação, por exemplo: equip_SP_2021_01

Segundo passo:
- Salvar em um diretório e copiar o caminho, exemplo: /home/lari/datasus/CNES/200508_/Dados/EQ

Terceiro passo:
- Abrir o Rstudio e no console carregar: require(read.dbc) ou library(read.dbc)

Quarto passo: 
- Colocar o conteudo dentro do arquivo no objeto, digitando no console:
equip_SP_2021_01 <- read.dbc(' /home/lari/datasus/CNES/200508_/Dados/EQ/EQSP2101.dbc',as.is=T)

Quinto passo:
- Para salvar o arquivo é só digitar no console:
write.csv2(equip_SP_2021_01, file="/home/lari/equipamentos.csv")
