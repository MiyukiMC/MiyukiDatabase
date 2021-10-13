# MiyukiDatabase

Cansou de perder tempo criando o sistema de banco de dados para seu plugin?

Então nosso framework de banco de dados irá te ajudar.

Além de contar com 5 tipos de banco de dados diferentes,
você pode criar as tabelas automaticamente com anotações. Veja exemplos no modo de uso.

Com fácil instalação no maven/gradle, você poderá usar ele sem dificuldades 
e isso lhe ajudará em seus projetos.

# Maven/Gradle

Ultima versão: [Download]("")

### Maven

```xml
<dependency>
    <groupId>miyuki.database</groupId>
    <artifactId>MiyukiDatabase</artifactId>
    <version>1.0.0</version>
</dependency>
```

### Gradle

Para versões antigas do gradle, use _'compile'_ em vez de _'implementation'_

```gradle

repositories {
    mavenCentral()
    
    maven {
        name 'miyukidatabase'
        url ''
    }
}

dependencies {
    implementation("miyuki.database:MiyukiDatabase:1.0.0")
}
```

# Exemplos

Neste framework contamos com 5 tipos de database, são eles:

* MySQL
* MySQL Legacy.
* SQLite
* H2
* MariaDB

Veja também:
* [Tipos de dados]("")
* [???](")

###Criação da database:

```java
public class MyApplication {
    
    public static void main(String[] args) {
        
    }
    
}
```

###Criação de tabelas:


####Exemplos:
```java
@Table(name = "myplugin_users") // Nome da tabela.
public class User {
    
    // opção de ser key primária.
    @PrimaryKey
    
    // type = o tipo da coluna, se for varchar, necessário colocar o size.
    @Column(type = ColumnType.VARCHAR, size = 16)
    private String name;
    
    @Column(type = ColumnType.INTEGER)
    private int age;
    
    @Column(type = ColumnType.VARCHAR, size = 32)
    private String password;
    
    // Getters & Setters...
}
```

