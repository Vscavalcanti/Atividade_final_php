[README .md](https://github.com/user-attachments/files/22539790/README.md)
# Projeto Oficina de Artes - Site em PHP

Aplicação simples em **PHP + HTML** para uma pequena oficina de artes, com CRUD de informações sobre a oficina e galeria de imagens.  

## Funcionalidades

- **Home (index.php):** exibe o último registro cadastrado em “Sobre a Oficina” (título, texto e foto).  
- **Sobre a Oficina (sobre.php):** CRUD completo (criar, listar, editar e excluir) com upload de imagem.  
- **Galeria (galeria.php):** exibe todas as fotos cadastradas em miniatura.  
- **Contato (contato.php):** página estrutural (conteúdo será inserido depois).  
- **Includes reutilizáveis:** `header.php` com menu (Home, Sobre, Galeria, Contato) e `footer.php` com créditos.  

## Tecnologias

- PHP 8.x (ou compatível)  
- MySQL 
- PDO (para conexão e queries com tratamento de erros)  
- HTML puro (sem CSS, para aplicação posterior de estilos)  

## Estrutura do Banco de Dados

**Banco:** `oficina_db`  
**Tabela:** `sobre`  

```sql
CREATE DATABASE oficina_db;
USE oficina_db;

CREATE TABLE sobre (
  id INT AUTO_INCREMENT PRIMARY KEY,
  titulo VARCHAR(150) NOT NULL,
  descricao TEXT NOT NULL,
  foto_path VARCHAR(255),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```  

## Como rodar o projeto

# Clonar repositório
git clone https://github.com/Vscavalcanti/Atividade_final_php.git
cd Atividade_final_php/Site

# Configurar banco de dados
# 1. Criar o banco usando o script SQL fornecido (acima ou em /db.sql)
# 2. Ajustar as credenciais no arquivo db.php (host, usuário, senha, nome do banco)

# Acessar no navegador
http://localhost:8000


## Observações

- Extensões aceitas para upload de imagens: **jpg, jpeg, png, gif, webp**  
- O site está sem CSS propositalmente para permitir que o estilo seja aplicado depois.  
