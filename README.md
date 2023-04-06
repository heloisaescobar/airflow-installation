# Instalação do Apache Airflow
Processo de Instalação do Apache Airflow e instalação dos plugins OCI

- Preparação do Ambiente

Criar o diretório onde será instalado o airflow:

´´´
mkdir -p /data/airflow
´´´

Após a Criação do path, vamos instanciar a variável de ambiente:

'''
export AIRFLOW_HOME=/data/airflow/
'''

Agora vamos instalar o pacote do airflow. Executar o comando abaixo:

'''
pip3.8 install apache-airflow
'''

Finalizando a execução do comando acima, o Airflow foi executado com sucesso.


## Inicializando o Airflow

Nesse momento vamos iniciar o airflow com as configurações padrões, posteriormente quando evoluirmos com a nossa arquitetura, vamos refinando as opções de configuração.

- Iniciando o banco de dados de backend

'''
airflow db init
'''

- Após a inicialização do nosso banco de dados de backend, vamos notar que no diretório $AIRFLOW_HOME, terá os arquivos de configuração.

<COLOCAR IMAGEM 3>

- Próximos passo, vamos criar um usuário que vai gerenciar o airflow, para isso executar o comando abaixo:
'''
airflow users create \
--username admin \
--firstname admin \
--lastname admin \
--role Admin \
--email admins@admin.com.br
'''

Na execução do comando, irá solicitar a senha do usuário:

<COLOCAR IMAGEM 4>

- Inicializando o scheduler do Airflow

'''
airflow scheduler
'''

- Inicializando a console web do Airflow

'''
airflow webserver --port 8080
'''

Se todos os comandos executarem com sucesso, seu airflow está disponível para uso.


## Administração através o shell

