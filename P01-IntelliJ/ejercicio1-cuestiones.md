# Cuestiones de las fases PACKAGE e INSTALL

## Fase PACKAGE

- ¿Qué goals se ejecutan?

Se ejecutan las goals de la fase 1 a la 17. Es decir, las siguientes goals en este orden:
	- resources:resources
	- compiler:compile
	- resources:testResources
	- compiler:testCompile
	- surefire:test
	- jar:jar

- ¿Qué hace? ¿Qué artefacto genera? ¿Dónde se genera durante la fase package?

Genera un paquete .jar del proyecto Maven. Dicho paquete se almacena en la raíz del directorio simpleMavenProject/target.

## Fase INSTALL

- ¿Qué goals se	ejecutan?

Se ejecutan las	goals de la fase 1 a la	22. Es decir, las siguientes goals en este orden:
        - resources:resources
        - compiler:compile
        - resources:testResources
        - compiler:testCompile
        - surefire:test
        - jar:jar
	- install:install


- ¿Qué hace? ¿Qué artefacto genera? ¿Dónde se genera durante la	fase package?

Genera el mismo .jar que con PACKAGE, sólo que lo copia en un repositorio local. En mi caso, me lo ha copiado a /home/isma/.m2/repository/ppss/P01/simpleMavenProject/1.0-SNAPSHOT/simpleMavenProject-1.0-SNAPSHOT.jar

- ¿Qué hace exactamente la fase INSTALL? ¿Dónde se copia exactamente en tu disco duro el artefacto correspondiente?

Como se ha dicho antes, genera el .jar (igual que en PACKAGE) sólo que lo copia en un repositorio local.

# ¿Para qué nos puede servir que el empaquetado de nuestro proyecto esté almacenado en nuestro repositorio local Maven?

Nos puede servir para utilizar el paquete como dependencia en otro proyecto que tengamos, sin necesidad de subirlo a internet o a un servidor compartido.
