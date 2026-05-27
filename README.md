# 🎓 AlunoOnline API

API para gerenciamento acadêmico desenvolvida com **Spring Boot**, permitindo o controle de alunos, professores, disciplinas e notas. O sistema disponibiliza operações REST para cadastro, consulta, atualização e gerenciamento do desempenho acadêmico dos estudantes.

---

## 🚀 Tecnologias Utilizadas

* **Java 17**
* **Spring Boot 3**
* **Spring Data JPA**
* **Lombok**
* **MySQL**
* **Maven**
* **Insomnia** (Testes das rotas)
* **DBeaver** (Gerenciamento do banco)

---

## 🏗️ Arquitetura do Projeto

O projeto segue o padrão **MVC (Model-View-Controller)** com separação em camadas para melhor organização e manutenção:

### 📌 Model
Responsável pelas entidades do banco de dados.

Exemplos:
- `Aluno`
- `Professor`
- `Disciplina`

### 📌 Repository
Camada responsável pelo acesso aos dados utilizando `JpaRepository`.

Exemplo:
```java
public interface AlunoRepository extends JpaRepository<Aluno, Integer> {
}
```

### 📌 Service
Responsável pelas regras de negócio da aplicação.

Exemplos:
- Cadastro de alunos
- Matrícula em disciplinas
- Atualização de notas

### 📌 Controller
Responsável pela exposição dos endpoints REST.

---

## 🛠️ Funcionalidades Implementadas

### 👨‍🎓 Alunos

| Funcionalidade | Verbo HTTP | Endpoint |
|---|---|---|
| Cadastrar aluno | POST | `/alunos` |
| Listar alunos | GET | `/alunos` |
| Buscar aluno por ID | GET | `/alunos/{id}` |
| Atualizar aluno | PUT | `/alunos/{id}` |
| Remover aluno | DELETE | `/alunos/{id}` |

---

### 👨‍🏫 Professores

| Funcionalidade | Verbo HTTP | Endpoint |
|---|---|---|
| Cadastrar professor | POST | `/professores` |
| Listar professores | GET | `/professores` |
| Buscar professor por ID | GET | `/professores/{id}` |
| Atualizar professor | PUT | `/professores/{id}` |
| Remover professor | DELETE | `/professores/{id}` |

---

### 📚 Disciplinas

| Funcionalidade | Verbo HTTP | Endpoint |
|---|---|---|
| Cadastrar disciplina | POST | `/disciplinas` |
| Listar disciplinas | GET | `/disciplinas` |
| Buscar disciplina por ID | GET | `/disciplinas/{id}` |
| Atualizar disciplina | PUT | `/disciplinas/{id}` |
| Excluir disciplina | DELETE | `/disciplinas/{id}` |

---

### 📝 Notas

| Funcionalidade | Verbo HTTP | Endpoint |
|---|---|---|
| Atualizar nota do aluno | PATCH | `/alunos/{id}/notas` |

Essa funcionalidade permite atualizar as notas dos alunos vinculados às disciplinas cadastradas.

---

## 📸 Demonstração das Requisições (Insomnia)

Nesta seção, estão os testes realizados durante o desenvolvimento.

### 1. Criar Registro (POST)
<img width="1920" height="1080" alt="Screenshot_41" src="https://github.com/user-attachments/assets/5733b5a9-b304-4163-bc44-b2911472af48" />

### 2. Listar Todos (GET)
<img width="1920" height="1080" alt="Screenshot_44" src="https://github.com/user-attachments/assets/139228a1-7ab6-4649-91e9-6df77e73189d" />

### 3. Atualizar Registro (PUT)
<img width="1920" height="1080" alt="Screenshot_45" src="https://github.com/user-attachments/assets/ee5bbe41-519e-471a-9b7e-049e9f74a749" />


### 4. Deletar Registro (DELETE)
<img width="1920" height="1080" alt="Screenshot_46" src="https://github.com/user-attachments/assets/9ef2e808-c458-4809-87e3-177b232f7930" />

### 5. Buscar por Id (GET)
<img width="1920" height="1080" alt="Screenshot_47" src="https://github.com/user-attachments/assets/2d825bed-0540-4bb0-ac10-cf06ce920e14" />

2.Requisições no Insomnia
Criando uma Disciplina (POST):
<img width="1920" height="1080" alt="Screenshot_72" src="https://github.com/user-attachments/assets/e39c4ce8-e0b5-4b36-9c10-baa8c865ad80" />


Listando Todas as Disciplinas (GET):
<img width="1920" height="1080" alt="Screenshot_78" src="https://github.com/user-attachments/assets/afbe1414-6451-4e0b-ab85-379bc1421cea" />



Listando Disciplina Por Id (GET):
<img width="1920" height="1080" alt="Screenshot_77" src="https://github.com/user-attachments/assets/abce4289-85a8-4db2-afd4-61f2cfd5992d" />


Atualizando uma Disciplina (PUT):
<img width="1920" height="1080" alt="Screenshot_73" src="https://github.com/user-attachments/assets/94469857-9a74-4627-9d88-fdf875abee6c" />
<img width="1920" height="1080" alt="Screenshot_74" src="https://github.com/user-attachments/assets/9ee5a02c-69bd-42b0-80c5-101169e06460" />


Deletando uma Disciplina (DELETE):
<img width="1920" height="1080" alt="Screenshot_75" src="https://github.com/user-attachments/assets/e614f17a-9d01-4b74-8823-7888825fb26f" />
<img width="1920" height="1080" alt="Screenshot_76" src="https://github.com/user-attachments/assets/b1394ea8-cf26-4f86-b3ca-c3e98c43e96e" />

Criando uma Matricula (POST):
<img width="1920" height="1080" alt="Screenshot_79" src="https://github.com/user-attachments/assets/e88f3edb-d248-4641-af9e-4dae90847fec" />



Trancando uma Matricula (PATCH):
<img width="1920" height="1080" alt="Screenshot_80" src="https://github.com/user-attachments/assets/b96191e3-353f-4a97-bf58-d7a21d7b45a8" />


Atualizando uma Matricula (PATCH): 
<img width="1920" height="1080" alt="Screenshot_81" src="https://github.com/user-attachments/assets/5a9c2bda-58dc-4241-9691-bd315c14c8b1" />

## 🗄️ Banco de Dados (DBeaver)

Visualização das tabelas e dados persistidos no banco de dados após os testes das rotas.


### Tabela de Matriculas Atualizada Depois De Testes:
<img width="1920" height="1080" alt="Screenshot_82" src="https://github.com/user-attachments/assets/006e9031-8561-4d48-9a3e-1bad550b316e" />

### Tabela de Alunos
<img width="1920" height="1080" alt="Screenshot_49" src="https://github.com/user-attachments/assets/e1939dab-925b-4df8-bf3d-7bd62def450c" />


### Tabela de Professores
<img width="1920" height="1080" alt="Screenshot_50" src="https://github.com/user-attachments/assets/af27a1c7-b3ce-4506-a5a1-465abcc468ab" />

---

## 🔗 Fluxo do Projeto

O sistema segue o seguinte fluxo:

Professor → Disciplina → Aluno → Nota

Onde:

- Professores podem estar vinculados a disciplinas;
- Alunos podem cursar disciplinas;
- Cada aluno possui notas relacionadas ao seu desempenho.

---

## 🔧 Como Executar o Projeto

### 1. Clonar o repositório

```bash
git clone https://github.com/caiograciano08/ALUNOSAPI.git
```

### 2. Abrir na IDE

Importe o projeto no:

- IntelliJ IDEA
- Eclipse
- Spring Tool Suite

### 3. Baixar dependências

Aguarde o Maven instalar automaticamente.

### 4. Configurar banco

Altere o arquivo:

```properties
application.properties
```

Exemplo:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/alunoonline
spring.datasource.username=root
spring.datasource.password=senha

spring.jpa.hibernate.ddl-auto=update
```

### 5. Executar

Inicie a classe principal:

```java
ApiApplication.java
```

A API ficará disponível em:

```bash
http://localhost:8080
```

---

## 📚 Referência

Projeto baseado no guia de apoio da disciplina:

https://aluno-online-uniesp-guia.vercel.app/

---

## 👨‍💻 Autor

Caio Graciano

Curso: Ciência da Computação – UNIESP
