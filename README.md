# SuperBurguer 🍔

Projeto simples de site para uma hamburgueria, feito com **Python + Flask**, páginas HTML usando **Jinja2** e **Tailwind CSS via CDN**.

## Funcionalidades

- Página principal com apresentação e destaques do cardápio.
- Página de login.
- Sessão simples de login e opção de sair.
- Mensagens de feedback para sucesso e erro.
- Layout responsivo com Tailwind CSS via CDN.

## Requisitos

- Python 3.10 ou superior.
- Pip.
- Conexão com a internet para carregar o Tailwind CSS via CDN.

## Como executar

### 1. Entre na pasta do projeto

cd superburguer

### 2. Crie e ative um ambiente virtual

Windows PowerShell:

py -m venv .venv
.venv\\Scripts\\Activate.ps1

Linux/macOS:

python3 -m venv .venv
source .venv/bin/activate

### 3. Instale as dependências

python -m pip install -r requirements.txt

### 4. Configure as credenciais de demonstração (opcional)

Por padrão, o login de demonstração é:

- Usuário: `admin`
- Senha: `burger123`

Para alterar no PowerShell antes de executar:

$env:SUPERBURGUER_USER = "seu_usuario"
$env:SUPERBURGUER_PASSWORD = "sua_senha"
$env:FLASK_SECRET_KEY = "coloque-uma-chave-aleatoria-forte"

Linux/macOS:

export SUPERBURGUER_USER="seu_usuario"
export SUPERBURGUER_PASSWORD="sua_senha"
export FLASK_SECRET_KEY="coloque-uma-chave-aleatoria-forte"

### 5. Inicie o servidor

python app.py

Abra no navegador: <http://127.0.0.1:5000>

## Estrutura do projeto

superburguer/
├── app.py
├── requirements.txt
├── .gitignore
├── README.md
├── templates/
│   ├── base.html
│   ├── index.html
│   └── login.html
└── static/
    └── css/
        └── style.css

## Rotas

| Método | Rota | Descrição |
|---|---|---|
| GET | `/` | Página principal |
| GET, POST | `/login` | Formulário e validação de login |
| GET | `/logout` | Encerra a sessão |

## Aviso de segurança

Este é um projeto inicial para estudo. O login usa credenciais de demonstração configuráveis por variáveis de ambiente e **não** possui cadastro de usuários, banco de dados, recuperação de senha, proteção contra tentativas repetidas ou configuração completa de produção. Não publique assim na internet sem implementar esses controles, configurar HTTPS e definir uma `FLASK_SECRET_KEY` forte. Para produção, execute com um servidor WSGI como Gunicorn e mantenha `FLASK_DEBUG=0`.

O Tailwind CSS está incluído pelo CDN para facilitar o protótipo. Para um projeto de produção, considere compilar os estilos localmente.
