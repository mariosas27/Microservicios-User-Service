# DEPARTMENT-SERVICE
## Requisitos
El funcionamiento de este proyecto va de la mano de service-registry, cloud-gateway y department-service
## Funcionamiento
### Petición POST
User-service realiza inserciones de usuarios a través de una peticón POST, el cuerpo de la petición debe de ser en formato JSON.
#### Ejemplo
```json
{
  "firstName":"Alumno Nombre",
  "lastName":"Alumno Apellido",
  "email":"Alumno Correo",
  "departmentId":"Alumno Departamento ID"
}
```

### Petición GET
User-service realiza consultas de departamentos con peticiones GET, para esto se debe de colocar en la url el dirección del servicio, seguido de una diagonal y el *id* del usuario. Esta petición además de consultar información acerca del estudiante, también consulta la información del departamento relacionado, por lo que hace uso del microservicio de Department-service.

