# Auditoría de Entidades con Hibernate Envers

Ejemplo de implementación de **auditoría de entidades utilizando Hibernate Envers** en una aplicación Java con JPA.

El proyecto demuestra cómo registrar automáticamente los cambios realizados sobre entidades persistidas en una base de datos, permitiendo mantener un historial de modificaciones.

---

## Tecnologías utilizadas

- Java  
- JPA (Java Persistence API)  
- Hibernate  
- Hibernate Envers  
- Maven  

---

## ¿Qué es Hibernate Envers?

Hibernate Envers es un módulo de Hibernate que permite **auditar entidades de forma automática**, registrando los cambios realizados en la base de datos.

Cada vez que una entidad es creada, modificada o eliminada, Envers guarda una revisión del estado de la entidad en tablas de auditoría.

Esto permite:

- Mantener historial de cambios
- Consultar versiones anteriores de una entidad
- Implementar trazabilidad de datos

---

## Funcionamiento

Para habilitar auditoría en una entidad se utiliza la anotación:

```java
@Audited
@Entity
public class Producto {
}```

Al persistir cambios, Envers genera automáticamente tablas de auditoría con el historial de revisiones.

## Ejemplo de tablas generadas:

- producto
- producto_AUD
- revinfo

Estas tablas almacenan las distintas versiones de cada registro junto con información de revisión.

## Estructura del proyecto

src
 ├── model
 ├── repository
 ├── service
 └── config

##Casos de uso de Envers

Hibernate Envers es útil en sistemas que requieren:

- auditoría de datos
- trazabilidad de cambios
- control histórico de registros
- cumplimiento normativo

Ejemplos de sistemas:

- sistemas financieros
- ERPs
- sistemas de gestión empresarial

Autor

Gonzalo Moyano
Estudiante de Ingeniería en Sistemas enfocado en desarrollo Backend con Java y Spring.
