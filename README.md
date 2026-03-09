# 🚗 Api_car

API REST para gerenciamento de veículos, desenvolvida com **Django** e **Django REST Framework**.

---

## 📋 Sobre o Projeto

A **Api_car** é uma API que permite cadastrar, consultar, atualizar e remover registros de veículos. O projeto foi desenvolvido com foco em simplicidade e boas práticas de desenvolvimento com Django REST Framework.

---

## 🛠️ Tecnologias Utilizadas

- [Python 3.x](https://www.python.org/)
- [Django](https://www.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- SQLite (banco de dados padrão para desenvolvimento)

---

## 📁 Estrutura do Projeto

```
Api_car/
├── app/               # Configurações principais do projeto Django
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── cars/              # App principal — models, views, serializers e rotas
│   ├── models.py
│   ├── serializers.py
│   ├── views.py
│   └── urls.py
├── manage.py
├── requirements.txt
├── .flake8            # Configuração do linter
└── .gitignore
```

---

## ⚙️ Como Rodar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/mathRyan889/Api_car.git
cd Api_car
```

### 2. Crie e ative um ambiente virtual

```bash
python -m venv venv

# Linux / macOS
source venv/bin/activate

# Windows
venv\Scripts\activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Execute as migrações

```bash
python manage.py migrate
```

### 5. Inicie o servidor

```bash
python manage.py runserver
```

A API estará disponível em: `http://localhost:8000/`

---

## 🔗 Endpoints

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/api/cars/` | Lista todos os veículos |
| `POST` | `/api/cars/` | Cadastra um novo veículo |
| `GET` | `/api/cars/{id}/` | Retorna os detalhes de um veículo |
| `PUT` | `/api/cars/{id}/` | Atualiza todos os dados de um veículo |
| `PATCH` | `/api/cars/{id}/` | Atualiza parcialmente um veículo |
| `DELETE` | `/api/cars/{id}/` | Remove um veículo |

---

## 📦 Exemplo de Requisição

**POST** `/api/cars/`

```json
{
  "marca": "Toyota",
  "modelo": "Corolla",
  "ano": 2022,
  "cor": "Prata",
  "placa": "ABC-1234"
}
```

**Resposta** `201 Created`

```json
{
  "id": 1,
  "marca": "Toyota",
  "modelo": "Corolla",
  "ano": 2022,
  "cor": "Prata",
  "placa": "ABC-1234"
}
```

---

## ✅ Qualidade de Código

O projeto utiliza **flake8** para garantir a qualidade e padronização do código.

Para rodar o linter:

```bash
flake8 .
```

---

## 👨‍💻 Autor

Desenvolvido por [Matheus Ryan](https://github.com/mathRyan889)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Matheus_Ryan-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/matheus-ryan-74110521b/)
[![GitHub](https://img.shields.io/badge/GitHub-mathRyan889-black?style=flat&logo=github)](https://github.com/mathRyan889)

---
