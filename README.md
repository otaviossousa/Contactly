# Contactly

Uma aplicação web para gerenciar uma agenda de contatos desenvolvida com Django.

## Site Hospedado

Acesse a aplicação em [Contactly](https://agendaotaviossousa.pythonanywhere.com)

## Funcionalidades

- ✅ Registro de usuários
- ✅ Login e logout
- ✅ CRUD de contatos (criar, ler, atualizar e deletar)
- ✅ Busca de contatos
- ✅ Paginação de contatos
- ✅ Upload de imagens para contatos
- ✅ Categorização de contatos
- ✅ Perfil de usuário

## Estrutura do Projeto

- `base_static/`: Arquivos estáticos globais (CSS, JS, imagens)
- `base_templates/`: Templates HTML globais
- `contact/`: Aplicação principal com models, views, forms e templates específicos
- `core/`: Configurações e URLs do projeto
- `media/`: Diretório para upload de arquivos
- `static/`: Diretório para arquivos estáticos coletados
- `utils/`: Scripts utilitários

## Scripts Utilitários

- `utils/create_contacts.py`: Cria contatos aleatórios para testes

## Telas do Sistema

### Tela Inicial
![Tela Inicial](media/images/Tela_Inicial.png)

### Login
![Tela de Login](media/images/Tela_Login.png)

### Registro de Usuário
![Tela de Registro](media/images/Tela_Registrar.png)

### Usuário Logado
![Usuário Logado](media/images/Tela_Usuario_Logado.png)

### Criar Contato
![Criar Contato](media/images/Tela_Criar_Contato.png)

### Dados do Contato
![Dados do Contato](media/images/Tela_Dados_Contato.png)

### Perfil do Usuário
![Perfil do Usuário](media/images/Tela_Perfil_Usuário.png)

### Painel Administrativo
![Admin](media/images/Tela_Admin.png)

### Diagrama DER
![Diagrama DER](media/images/DER_DIAGRAM.png)

## Como Executar

1. Clone o repositório
2. Crie um ambiente virtual: `python -m venv venv`
3. Ative o ambiente: `.\venv\Scripts\activate` (Windows)
4. Instale as dependências: `pip install -r requirements.txt`
5. Execute as migrations: `python manage.py migrate`
6. Crie um superuser: `python manage.py createsuperuser`
7. Inicie o servidor: `python manage.py runserver`
8. Acesse em `http://127.0.0.1:8000/`
