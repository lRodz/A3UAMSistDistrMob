### **Título do Trabalho**  
*Sistema de análise e validação de CNPJ utilizando API externa e persistência de dados.*

---

# 📚 **Sumário**
1. Introdução  
2. Desenvolvimento  
3. Resultados  

---

# **1. Introdução**

## 📌 **Contextualização do tema**
O projeto aborda o problema de identificação de empresas falsas por meio da validação de **CNPJ**.  
Em um cenário onde golpes envolvendo empresas inexistentes são cada vez mais frequentes, ferramentas que consultam bases oficiais se tornam essenciais para garantir segurança em negociações, cadastros e transações.

O sistema desenvolvido permite realizar consultas através de uma interface web integrada a um backend que verifica a autenticidade do CNPJ informado.

---

## ❗ **Problema que a solução busca resolver**
A dificuldade de verificar rapidamente se um CNPJ realmente existe e está ativo pode levar usuários e empresas a caírem em fraudes.

**Pergunta central do problema:**  
👉 *Como permitir ao usuário validar, de forma simples e confiável, se uma empresa realmente existe e está registrada?*

A solução aborda isso consultando:
- Uma base de CNPJs (BrasilAPI)  
- Uma API externa (Receita Federal) caso o dado não esteja armazenado internamente  

---

## 🎯 **Objetivos do trabalho**
- Criar um **sistema web funcional** para consulta e validação de CNPJ  
- Integrar o backend com uma **API externa** para obtenção de dados reais  
- Realizar **persistência automática** dos dados encontrados  
- Exibir ao usuário:
  - CNPJ
  - Nome fantasia  
- Retornar mensagens adequadas quando:
  - O CNPJ é inválido  
  - O CNPJ não possui registro ativo  

---

## 📝 **Justificativa da escolha do tema**
A escolha do tema se justifica por sua relevância prática:

- Validação de CNPJ é um processo comum em empresas e sistemas corporativos  
- Reduz riscos de fraudes  
- Permite aplicar conceitos essenciais de programação e arquitetura:
  - Consumo de APIs externas  
  - Arquitetura em camadas  
  - Persistência de dados  
  - Desenvolvimento com Java + Spring Boot  
  - Integração cliente-servidor  

O tema também contribui academicamente para estudos relacionados a segurança e confiabilidade da informação.

---

# **2. Desenvolvimento**

## 🧩 **Desenho da solução**

<img width="3468" height="1356" alt="Fluxograma" src="https://github.com/user-attachments/assets/2019e904-1cd5-4ba2-839b-8adc37b34f86" />

### Arquitetura utilizada:
- Arquitetura **Cliente–Servidor**
- Padrão **MVC (Model–View–Controller)**

### Fluxo resumido:
1. Usuário insere o CNPJ na interface (HTML/CSS)  
2. Backend recebe a requisição (Spring Boot)  
3. Verifica se o CNPJ está salvo no banco  
4. Se não estiver, consulta a API da Receita Federal  
5. Caso encontrado, salva no banco e retorna ao usuário  
6. Caso contrário, exibe mensagem de CNPJ inválido/inexistente  

---

## ⚙ **Implementação**

### **Tecnologias utilizadas**

#### 🔹 Backend
- **Java 17**
- **Spring Boot**
  - spring-boot-starter-web  
  - spring-boot-starter-data-jpa  

#### 🔹 Banco de Dados
- **MySQL**

#### 🔹 Frontend
- **HTML5**  
- **CSS3**

#### 🔹 API Externa
- **Receita Federal (via BrasilAPI)**  

---

## 🔗 **Repositório GitHub**
📍 https://github.com/lRodz/A3UAMSistDistrMob

---

# **3. Resultados**
