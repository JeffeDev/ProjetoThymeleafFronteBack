<div align="center">
  <h1>Java MVC - Thymeleaf e Bootstrap</h1>
  <p>
	  Projeto desenvolvido em Java com Thymeleaf  🤿 ☕ <br>
	  Desenvolvido com 💙 por Jefferson Cesar de Souza.<br>
	  Como Portifólio em meu Git
  </p>
</div>

## ⚙️ Boa Práticas 
O Spring MVC é um framework Java que ajuda no desenvolvimento de 
aplicações Web, facilita o trabalho com o protocolo HTTP e a 
criação de HTML dinamicamente, 
seguindo boas práticas de desenvolvimento.


## 🛠️ Tecnologias utilizadas

Java 1.8 com Maven

Vamos criar um projeto Java, Maven, versão 2.7 no 
pacote br.com.alura.mvc e vamos adicionar algumas dependências: 

* **Spring Web** → Spring MVC com Rest e TomCat

* **Thimeleaf**    → Gerenciar as Views HTML

* **Dev Tools**    → O Spring Dev Tools faz o restart da aplicação, 
facilitando nossa vida, Não tem que ficar derrubando servidor, etc.

Banco de Dados MySQL


## 🖥️ Dependencias

#### Dependências Maven
````
	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-thymeleaf</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>
		<dependency>
	      <groupId>org.springframework.boot</groupId>
	      <artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
		      <groupId>mysql</groupId>
		      <artifactId>mysql-connector-java</artifactId>
		      <scope>runtime</scope>
		</dependency>
		
		<dependency>
		      <groupId>org.springframework.boot</groupId>
		      <artifactId>spring-boot-starter-validation</artifactId>
		</dependency>		

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-devtools</artifactId>
			<scope>runtime</scope>
			<optional>true</optional>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
			<exclusions>
				<exclusion>
					<groupId>org.junit.vintage</groupId>
					<artifactId>junit-vintage-engine</artifactId>
				</exclusion>
			</exclusions>
		</dependency>
	</dependencies>

````

## 📒 Conteúdos  

**BackEnd**: [Java](https://github.com/JeffeDev)

**FrontEnd**: Thymeleaf, Bootstrap, HTML5, CSS e VueJS


O Spring Data JPA utiliza interfaces para fazer a comunicação, 
retirei a class e substitui por interface:

```java
package br.com.alura.mvc.mudi.repository;

import java.util.List;

import javax.persistence.EntityManager;
import javax.persistence.PersistenceContext;
import javax.persistence.Query;

import org.springframework.stereotype.Repository;

import br.com.alura.mvc.mudi.model.Pedido;

@Repository
public class interface PedidoRepository {
	@PersistenceContext
	private EntityManager entityManager;
	
	public List<Pedido> recuperaTodosPedidos(){
		Query query = entityManager.createQuery("select p from Pedido p", Pedido.class);
		return query.getResultList();
	}
}
```

O Spring Data recupera os dados pelo nome da classe, por exemplo, 
nosso método recuperaTodosPedidos() é substituido por FindAll(), 
E não precisa colocar este “Select p from Pedido p” o Spring data 
já sabe fazer isto sem que precise implementar alguma coisa.

## 🎯 O que o projeto faz:
  - [X] Um cadastro de Pedidos.


## 📸 Screenshots
####  📌 Back-End e Front-End 

aplicação back-end usando as tecnologias Java com Spring;
aplicação Front-End com Thymeleaf, JueJS e BootsTrap


## ❔ Dúvidas?!
Se tiver alguma dúvida sobre este repositório, envie para jeffe.info@gmail.com




