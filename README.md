# Template-Zabbix-Expiracao-de-Dominio
Template para Monitoramento de Validade de Domínio

Testado no zabbix 5.0.9


Instruções de Uso
1° Instale o whois no servidor zabbix
2° coloque o arquivo "data_expire.sh" no caminho:
/usr/lib/zabbix/externalscripts

lembre de atribuir permissão para execução
chmod +xw /usr/lib/zabbix/externalscripts/data_expire.sh

importe o template "Template Expiracao de Dominio.xml" para o zabbix
Crie o host com o dominio que deseja monitorar a data de validade, o ip pode ser do zabbix server ou localhost:
ex:
![image](https://github.com/user-attachments/assets/aa364d02-3305-4bf2-9fd8-bab090642142)

OBS.: Se você tiver mais de 20 dominios para monitorar, recomento criar 2 templates com datas com intervalos de consultas diferentes, pois o registro.br pode bloquear seu ip para consulta durante 24 horas
nesse caso só altera o campo no item de consulta abaixo:
![image](https://github.com/user-attachments/assets/72d780b4-cf1f-41da-92ff-4ff7fbe0614e)
nesse caso, ele irá executar a consulta 1 vez por semana toda segunda feira as 07:00





