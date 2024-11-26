# AWS SNS Topic Creator

## Descrição

Este projeto demonstra como criar tópicos no Amazon Simple Notification Service (SNS) usando a biblioteca Boto3, o SDK oficial da AWS para Python. Ele exemplifica a automação de tarefas relacionadas ao SNS, incluindo a criação de tópicos e o envio de mensagens para esses tópicos.

## Recursos 

- Criação de tópicos no Amazon SNS.
- Envio de mensagens para os tópicos criados.
- Configuração e gerenciamento simplificados através do Python e da biblioteca Boto3.

- ## Tecnologias Utilizadas

- **Python 3.10+**
- **AWS SDK (Boto3)**
- **Amazon SNS**

   ## Pré-requisitos

Antes de usar este projeto, certifique-se de que você possui:

- Uma conta ativa na AWS.
- O AWS CLI instalado e configurado em sua máquina.
- Python 3.10 ou superior instalado.
- A biblioteca Boto3 instalada. Você pode instalá-la com o comando:
  ```bash
  pip install boto3
Instalação
Clone o repositório:
git clone https://github.com/jltdsjrdev/AWS--sns.git

cd AWS--sns

Instale as dependências necessárias:
pip install -r requirements.txt

## Configure suas credenciais AWS:
aws configure


## Estrutura do Projeto:



AWS--sns/
├── create-topic.py          # Script principal para criar tópicos SNS
├── requirements.txt         # Dependências do projeto
├── README.md                # Documentação do projeto
└── .gitignore               # Arquivos ignorados no Git
Como Usar
Execute o script principal para criar um tópico:


python create-topic.py
Siga as instruções exibidas no terminal para criar e gerenciar seus tópicos SNS.

Exemplo de Uso
Abaixo está um trecho de código básico usado no script:


import boto3

sns_client = boto3.client('sns')

# Criação de um tópico SNS
response = sns_client.create_topic(Name='MeuTopico')
print(f"Tópico criado com sucesso: {response['TopicArn']}")

# Envio de uma mensagem para o tópico
sns_client.publish(
    TopicArn=response['TopicArn'],
    Message='Mensagem de teste',
    Subject='Assunto do teste'
)


Licença
Este projeto está licenciado sob a MIT License.

Contribuindo
Contribuições são bem-vindas! Para contribuir:

Faça um fork do repositório.
Crie uma branch para sua feature:

git checkout -b minha-feature
Commit suas alterações.
Faça um push para sua branch:

git push origin minha-feature
Abra um Pull Request.
