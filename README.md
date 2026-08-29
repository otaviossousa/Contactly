# Contactly

> Agenda de contatos web desenvolvida em Django para registrar, buscar, organizar e manter dados pessoais em uma interface simples.

[![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-5.1.5-092E20?logo=django&logoColor=white)](https://www.djangoproject.com/)
[![SQLite](https://img.shields.io/badge/Database-SQLite-003B57?logo=sqlite&logoColor=white)](https://www.sqlite.org/)

![Tela inicial da aplicação](media/images/Tela_Inicial.png)

## Sobre

O Contactly é uma aplicação web para gerenciar uma agenda de contatos. O projeto permite que usuários criem uma conta, façam login e mantenham uma lista de pessoas com dados básicos como nome, telefone, e-mail, categoria e foto.

A solução foi implementada com Django e usa templates do próprio framework para renderizar a interface e o fluxo de autenticação. O sistema também conta com pesquisa, paginação e administração via painel do Django.

## Destaques

- 🔐 Registro e login de usuários
- 📇 CRUD completo de contatos
- 🔎 Busca por nome, sobrenome, telefone e e-mail
- 📄 Paginação da listagem
- 🖼️ Upload de imagem para cada contato
- 🏷️ Organização por categoria
- 👤 Edição do perfil do usuário
- 🧩 Painel administrativo do Django

## Como funciona

A aplicação segue o fluxo típico de uma agenda pessoal:

1. O usuário cria uma conta ou acessa o sistema com login.
2. O cadastro de contatos é feito em uma tela específica.
3. Cada contato possui dados básicos e pode ter uma imagem associada.
4. A listagem permite visualizar contatos em páginas e realizar buscas.
5. Os registros ficam vinculados ao usuário autenticado e podem ser atualizados ou removidos.

Além disso, o projeto define categorias para agrupar contatos e expõe a administração do Django para gestão interna.

## Demonstração

A aplicação já está disponível em produção neste endereço:

- [Contactly](https://agendaotaviossousa.pythonanywhere.com)

Algumas telas do projeto estão presentes na pasta [media/images](media/images):

![Login](media/images/Tela_Login.png)

![Registro](media/images/Tela_Registrar.png)

![Criar contato](media/images/Tela_Criar_Contato.png)

![Dados do contato](media/images/Tela_Dados_Contato.png)

![Perfil do usuário](media/images/Tela_Perfil_Usuário.png)

![Painel administrativo](media/images/Tela_Admin.png)

![Diagrama DER](media/images/DER_DIAGRAM.png)

## Tecnologias

| Categoria | Tecnologia |
|---|---|
| Linguagem | Python |
| Framework web | Django |
| Banco de dados | SQLite |
| Manipulação de imagens | Pillow |
| Templates | Django Templates |
| Administração | Django Admin |

## Estrutura do projeto

```text
Contactly/
├── base_static/            # arquivos estáticos globais
├── base_templates/         # templates compartilhados
├── contact/                # aplicação principal do projeto
│   ├── migrations/         # migrações do banco de dados
│   ├── templates/          # templates da agenda de contatos
│   ├── views/              # views da aplicação
│   ├── admin.py            # cadastro de modelos no admin
│   ├── forms.py            # formulários de cadastro e contato
│   ├── models.py           # modelos de Contact e Category
│   ├── urls.py             # rotas da aplicação
│   └── tests.py            # testes do app
├── core/                   # configuração do projeto Django
│   ├── settings.py         # configurações gerais
│   ├── urls.py             # urls do projeto
│   ├── asgi.py             # entrypoint ASGI
│   └── wsgi.py             # entrypoint WSGI
├── media/                  # arquivos enviados pelos usuários
├── utils/                  # scripts utilitários
│   └── create_contacts.py  # geração de contatos para testes
├── manage.py               # gerenciamento do projeto Django
├── requirements.txt        # dependências do projeto
├── README.md               # documentação do repositório
└── .gitignore              # arquivos ignorados pelo Git
```

## Principais rotas

A aplicação define as rotas abaixo no arquivo [contact/urls.py](contact/urls.py):

| Método | Rota | Descrição |
|---|---|---|
| GET | `/` | lista os contatos ativos |
| GET | `/search/` | busca contatos por texto |
| GET/POST | `/contact/create/` | criação de novo contato |
| GET/POST | `/contact/<id>/update/` | atualização de contato |
| GET/POST | `/contact/<id>/delete/` | exclusão de contato |
| GET/POST | `/user/create/` | cadastro de usuário |
| GET/POST | `/user/login/` | autenticação |
| GET | `/user/logout/` | logout |
| GET/POST | `/user/update/` | atualização do perfil do usuário |
| GET | `/admin/` | painel administrativo do Django |

## Como executar

### Pré-requisitos

- Python instalado no ambiente
- pip disponível
- Git para clonar o repositório

### Passo a passo

```bash
git clone https://github.com/<seu-usuario>/Contactly.git
cd Contactly
python -m venv venv
```

Ative o ambiente virtual:

```bash
# Windows
venv\Scripts\activate

# Linux/macOS
source venv/bin/activate
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Aplique as migrações e inicie o projeto:

```bash
python manage.py migrate
python manage.py runserver
```

Acesse a aplicação em:

```text
http://127.0.0.1:8000/
```

Para criar um administrador do Django:

```bash
python manage.py createsuperuser
```

## Documentação e recursos

O repositório possui material visual e de apoio importante nas pastas abaixo:

- [media/images](media/images) — capturas de tela e diagramas
- [contact/templates](contact/templates) — templates da aplicação
- [contact/models.py](contact/models.py) — estrutura dos modelos principais
- [contact/forms.py](contact/forms.py) — validações e formulários
- [contact/views](contact/views) — lógica das operações da agenda

## Observações

O projeto é um exemplo funcional de agenda pessoal em Django com autenticação, cadastro de contatos e gestão visual via templates. A base de dados padrão configurada no projeto é SQLite, e a aplicação está preparada para uso local e para implantação em ambientes compatíveis com Django.
