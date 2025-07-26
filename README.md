# 🧊 GeloFácil - Sistema de Gestão para Fábrica de Gelo

Um sistema completo de gestão para fábricas de gelo, desenvolvido com FastAPI (backend) e HTML/CSS/JavaScript (frontend).

## 📋 Funcionalidades

- **Autenticação segura** com JWT tokens
- **Gestão de produtos** (estoque, preços, estoque mínimo)
- **Interface responsiva** com design moderno
- **API RESTful** completa
- **Banco de dados SQLite** para simplicidade
- **Documentação automática** da API

## 🚀 Instalação e Configuração

### Pré-requisitos
- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)

### Passos para instalação

1. **Clone ou baixe o projeto**
   ```bash
   # Navegue para a pasta do projeto
   cd "Gelo Facil"
   ```

2. **Instale as dependências**
   ```bash
   pip install -r requirements.txt.txt
   ```

3. **Execute o servidor**
   ```bash
   python -m uvicorn main:app --reload
   ```

4. **Acesse o sistema**
   - Interface web: http://localhost:8000
   - Documentação da API: http://localhost:8000/docs

## 📁 Estrutura do Projeto

```
Gelo Facil/
├── main.py              # Backend FastAPI
├── index.html           # Interface frontend
├── requirements.txt.txt  # Dependências Python
├── gelofacil.db        # Banco de dados SQLite
├── test_api.py         # Script de testes
└── README.md           # Este arquivo
```

## 🔧 Configuração do Sistema

### Primeiro Acesso

1. Acesse http://localhost:8000
2. Clique em "Registre-se" para criar sua primeira conta
3. Use o email e senha criados para fazer login
4. Comece a cadastrar seus produtos

### Funcionalidades Disponíveis

- **Autenticação**: Registro e login de usuários
- **Gestão de Produtos**: 
  - Cadastrar novos produtos
  - Editar produtos existentes
  - Visualizar estoque atual
  - Alertas de estoque baixo
  - Controle de preços

## 🔌 API Endpoints

### Autenticação
- `POST /token` - Login (obter token)
- `POST /users/register` - Registrar novo usuário
- `GET /users/me` - Informações do usuário logado

### Produtos
- `GET /products/` - Listar todos os produtos
- `GET /products/{id}` - Obter produto específico
- `POST /products/` - Criar novo produto
- `PUT /products/{id}` - Atualizar produto
- `DELETE /products/{id}` - Deletar produto

## 🧪 Testes

Execute o script de testes para verificar se tudo está funcionando:

```bash
python test_api.py
```

## 🔒 Segurança

- Autenticação JWT com tokens de 60 minutos
- Senhas criptografadas com bcrypt
- Validação de dados com Pydantic
- Proteção contra ataques comuns

## 🛠️ Tecnologias Utilizadas

### Backend
- **FastAPI** - Framework web moderno e rápido
- **SQLAlchemy** - ORM para banco de dados
- **Pydantic** - Validação de dados
- **python-jose** - Implementação JWT
- **passlib** - Criptografia de senhas
- **uvicorn** - Servidor ASGI

### Frontend
- **HTML5** - Estrutura da página
- **Tailwind CSS** - Framework CSS utilitário
- **JavaScript** - Lógica da interface
- **Fetch API** - Comunicação com backend

### Banco de Dados
- **SQLite** - Banco de dados local

## 📊 Modelos de Dados

### Usuário (User)
- `id`: Identificador único
- `email`: Email do usuário (único)
- `hashed_password`: Senha criptografada
- `is_active`: Status ativo/inativo

### Produto (Product)
- `id`: Identificador único
- `name`: Nome do produto
- `quantity`: Quantidade em estoque
- `min_stock`: Estoque mínimo
- `price`: Preço de venda

## 🚨 Solução de Problemas

### Erro de Conexão
- Verifique se o servidor está rodando
- Confirme se a porta 8000 está livre
- Teste com `python test_api.py`

### Erro de Dependências
- Execute `pip install -r requirements.txt.txt`
- Verifique se o Python está na versão 3.8+

### Problemas de Banco de Dados
- O arquivo `gelofacil.db` é criado automaticamente
- Para resetar, delete o arquivo e reinicie o servidor

## 📝 Próximas Funcionalidades

- [ ] Gestão de clientes
- [ ] Controle de vendas
- [ ] Relatórios financeiros
- [ ] Gestão de despesas
- [ ] Backup automático
- [ ] Múltiplos usuários com permissões

## 🤝 Contribuição

Para contribuir com o projeto:

1. Faça um fork do repositório
2. Crie uma branch para sua feature
3. Commit suas mudanças
4. Push para a branch
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

## 📞 Suporte

Para suporte ou dúvidas:
- Abra uma issue no repositório
- Consulte a documentação da API em `/docs`
- Execute os testes para verificar a instalação

---

**Desenvolvido com ❤️ para facilitar a gestão de fábricas de gelo** 