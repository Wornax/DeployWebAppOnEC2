# Passo a Passo: Deploy de Aplicação Web Estática na AWS EC2

Este guia fornece instruções passo a passo para realizar o deploy de uma aplicação web estática em uma instância EC2 da AWS (Amazon Web Services).

## Pré-Requisitos

Antes de começar, certifique-se de ter o seguinte:

- Conta na AWS.
- Conhecimentos básicos de Linux e linha de comando.
- Conhecimentos básicos sobre servidores web e configuração de sites.

## Passo 1: Configuração da Instância EC2
Neste repositório eu mostro como eu criei uma EC2 usando terraform: https://github.com/Wornax/CreateEC2withTerraform

## Passo 2: Instalação e Configuração do Apache

1. Conecte-se à instância EC2

![image](https://github.com/Wornax/DeployWebAppOnEC2/assets/105296448/23740308-d837-4062-955d-195660da375a)

2. Atualize os pacotes do sistema:

sudo yum update -y

3. Instale o servidor web Apache:

sudo yum install httpd -y

4. Inicie o serviço Apache e configure-o para iniciar automaticamente após o reboot:

sudo service httpd start
sudo chkconfig httpd on


## Passo 3: Transferência dos Arquivos da Aplicação

1. Transfira os arquivos da aplicação para a instância EC2 usando SCP ou outro método de sua preferência.
2. Copie os arquivos para o diretório de documentos do Apache (geralmente /var/www/html/).

## Passo 4: Acesso à Aplicação Web

1. Abra um navegador web e insira o endereço IP público da sua instância EC2.
2. Você deve ver sua aplicação web sendo servida pelo servidor Apache.

## Passo 5: Opcional - Configurações Adicionais

1. Configure um nome de domínio personalizado para sua instância EC2 usando o Route 53 ou outro serviço de DNS.
2. Configure SSL/TLS para habilitar o suporte a HTTPS na sua aplicação web.
3. Explore outras configurações e personalizações disponíveis no Apache para otimizar o desempenho e a segurança.

Com estes passos, você realizou com sucesso o deploy de uma aplicação web estática na AWS EC2 utilizando o servidor web Apache

![image](https://github.com/Wornax/DeployWebAppOnEC2/assets/105296448/ad2e5506-c1ba-436a-a25f-e7c2e26ca78d)

![image](https://github.com/Wornax/DeployWebAppOnEC2/assets/105296448/b37068fd-37f6-4c69-9e21-e25060ee4f15)





