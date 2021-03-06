### Acceso al código fuente e instalación

Como toda especificación en Java, JSR, además del API esta posee una implementación de referencia, como el propio nombre dice, esa implementación servirá de base para las próximas implementaciones. En el caso de la JSR 354, money-api, una implementación de referencia es moneta (Para mas informaciones en relación al codigo fuente del proyecto puedes acceder a [https://github.com/JavaMoney/jsr354-ri](https://github.com/JavaMoney/jsr354-ri)). Basicamente, es posible utilizar moneta de dos formas:

La primera de ellas es accesando a su repositorio de dependencia de maven ([http://mvnrepository.com/artifact/org.javamoney/moneta](http://mvnrepository.com/artifact/org.javamoney/moneta)), por lo que si tu proyecto usa maven, por ejemplo, basta adicionar una dependencia de moneta em su proyecto de la siguiente forma:

```
        <dependency>
            <groupId>org.javamoney</groupId>
            <artifactId>moneta</artifactId>
            <version>moneta_version</version>
        </dependency>
```

Para Gradle:
```
'org.javamoney:moneta:moneta_version'
```

Para Yvi:
```
<dependency org="org.javamoney" name="moneta" rev="moneta_version"/>
```


La otra forma es bajando el código-fuente y compilandolo, para eso será necesario seguir algunos pasos, mas basicamente es baja el parent o instalarlo y enseguida instalar moneta. Vale recordar que para realizar ese procedimiento es necesario tener git, Java 8 y maven instalado y configurado en su maquina.


Bajar el código de javamoney-parent, para esto solo ejecute el siguiente comando:

```
git clone https://github.com/JavaMoney/javamoney-parent.git
```

Enseguida accese a la carpeta:
```
cd javamoney-parent
```

Compile el código-fuente e instalelo en su repositório local, en nuestro caso tambien saltaremos las pruebas solo para que sea mas rápido:

```
mvn clean install -Dmaven.test.skip
```

Listo, una vez hecho todo eso el proximo paso será realizar la instalación de moneta.

Bajar el código de moneta, para esto solo ejecute el siguiente comando:

```
git clone git@github.com:JavaMoney/jsr354-ri.git
```

Enseguida accede a la carpeta:

```
cd jsr354-ri
```

Compile el código-fuente e instalelo en su repositório local, en nuestro caso tambien saltaremos las pruebas solo para que sea mas rápido:

```
mvn clean install -Dmaven.test.skip
```


Listo, código-fuente instalado y podrá ser utilizado tranquilamente. En el caso del libro estamos utilizando como base un master del repositório, osea, es recomendable que baje el código-fuente y lo instale localmente. Para tener acceso al código-fuente del ejemplo basta con accesar:

* [https://github.com/otaviojava/money-api-book-samples](https://github.com/otaviojava/money-api-book-samples)

