# ![OWASP VulnerableApp by Indra](https://raw.githubusercontent.com/SasanLabs/VulnerableApp/master/docs/logos/Coloured/iconColoured.png) OWASP VulnerableApp Indra Fork

Aplicación que se basa en el proyecto https://github.com/SasanLabs/VulnerableApp, el cual tiene de manera deliberada muchas vulnerabilidades actuales del mercado y pretendemos identificar con el escaneo con SonarQube, como ejercicio práctico en la comunidad Java Indra Colombia.

**VulnerableApp** es un proyecto de OWASP, que se utiliza como una aplicación de ejemplo deliberadamente vulnerable para propósitos educativos y de prueba de seguridad. Permite a los desarrolladores y profesionales de seguridad practicar la identificación y corrección de vulnerabilidades comunes en aplicaciones web. Se puede utilizar junto con herramientas como SonarQube para analizar y mejorar la seguridad del código, identificando y solucionando problemas de seguridad potenciales.

## Tecnologías que utiliza
- Java8
- Maven
- Spring Boot
- ReactJS
- Javascript/TypeScript
    
## Tipos de vulnerabilidades actualmente soportadas

1. [JWT Vulnerability](https://github.com/rahozindracompany/owasp-vulnerable-app/blob/master/src/main/java/org/sasanlabs/service/vulnerability/jwt/)
2. [Command Injection](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/commandInjection)
3. [File Upload Vulnerability](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/fileupload)
4. [Path Traversal Vulnerability](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/pathTraversal)
5. [SQL Injection](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/sqlInjection)
    1. [Error Based SQLi](https://github.com/rahozindracompany/owasp-vulnerable-app/blob/master/src/main/java/org/sasanlabs/service/vulnerability/sqlInjection/ErrorBasedSQLInjectionVulnerability.java)
    2. [Union Based SQLi](https://github.com/rahozindracompany/owasp-vulnerable-app/blob/master/src/main/java/org/sasanlabs/service/vulnerability/sqlInjection/UnionBasedSQLInjectionVulnerability.java)
    3. [Blind SQLi](https://github.com/rahozindracompany/owasp-vulnerable-app/blob/master/src/main/java/org/sasanlabs/service/vulnerability/sqlInjection/BlindSQLInjectionVulnerability.java)
6. [XSS](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/xss)
    1. [Persistent XSS](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/xss/persistent)
    2. [Reflected XSS](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/xss/reflected)
7. [XXE](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/xxe)
8. [Open Redirect](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/urlRedirection)
    1. [Http 3xx Status code based](https://github.com/rahozindracompany/owasp-vulnerable-app/blob/master/src/main/java/org/sasanlabs/service/vulnerability/urlRedirection/Http3xxStatusCodeBasedInjection.java)
9. [SSRF](https://github.com/rahozindracompany/owasp-vulnerable-app/tree/master/src/main/java/org/sasanlabs/service/vulnerability/ssrf)

## Inicio rápido

```bash
git clone https://github.com/rahozindracompany/owasp-vulnerable-app.git
cd owasp-vulnerable-app
mvn clean install
mnv sonar:sonar
mvn spring-boot:run
```
Abrir URL en navegador:

http://localhost:9090/VulnerableApp/

### Conectandose a la base de datos embebida H2
Para acceder a la base de datos desde el navegador ir a: `http://localhost:9090/VulnerableApp/h2`

Database Connection properties:
```properties
JDBC Url: jdbc:h2:mem:testdb
User Name: admin
Password: hacker
```
## Contact
In case you are stuck with any of the steps or understanding anything related to project and its goals, feel free to shoot a mail at karan.sasan@owasp.org or raise an [issue](https://github.com/SasanLabs/owasp-vulnerable-app/issues) and we will try our best to help you.

## Documentación y referencias

1. [Documentación](https://sasanlabs.github.io/VulnerableApp)
2. [Documenación de diseño](https://sasanlabs.github.io/owasp-vulnerable-app/DesignDocumentation.html)
3. [Owasp VulnerableApp](https://owasp.org/www-project-vulnerableapp/)
5. [Vídeo resumido](https://www.youtube.com/watch?v=AjL4B-WwrrA&ab_channel=OwaspVulnerableApp)