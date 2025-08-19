# Liquidación-y-pagos-uv

Integrantes:

- Elizabeth Oneto
- Joaquín Aguilera
- Vicente Cruces
 
# Tablas BD

- Contrato
- Reemplazo
- Reportes
- Urgencias Médicas
  
# Contrato
+--------------------+------------------------------------------------------------+------+-----+---------+-------+
| Field              | Type                                                       | Null | Key | Default | Extra |
+--------------------+------------------------------------------------------------+------+-----+---------+-------+
| rut_empleado       | int                                                        | NO   | PRI | NULL    |       |
| nombre             | varchar(20)                                                | NO   |     | NULL    |       |
| apellido_paterno   | varchar(20)                                                | NO   |     | NULL    |       |
| apellido_materno   | varchar(20)                                                | NO   |     | NULL    |       |
| genero             | enum('H','M','X','O')                                      | NO   |     | NULL    |       |
| especialidad       | enum('Enfermería','Kinesiología','Tecnología','Medico')    | NO   |     | NULL    |       |
| inicio_de_contrato | date                                                       | NO   |     | NULL    |       |
| sueldo_bruto       | int                                                        | NO   |     | NULL    |       |
| sueldo_liquido     | int                                                        | YES  |     | NULL    |       |
| telefono1          | int                                                        | NO   |     | NULL    |       |
| telefono2          | int                                                        | YES  |     | NULL    |       |
| correo             | varchar(15)                                                | YES  |     | NULL    |       |
| direccion          | varchar(50)                                                | YES  |     | NULL    |       |
+--------------------+------------------------------------------------------------+------+-----+---------+-------+

# Reportes+--------------------+------------------------------------------------------------+------+-----+---------+-------+
| Field              | Type                                                       | Null | Key | Default | Extra |
+--------------------+------------------------------------------------------------+------+-----+---------+-------+
| rut_empleado       | int                                                        | NO   | PRI | NULL    |       |
| nombre             | varchar(20)                                                | NO   |     | NULL    |       |
| apellido_paterno   | varchar(20)                                                | NO   |     | NULL    |       |
| apellido_materno   | varchar(20)                                                | NO   |     | NULL    |       |
| genero             | enum('H','M','X','O')                                      | NO   |     | NULL    |       |
| especialidad       | enum('Enfermería','Kinesiología','Tecnología','Medico')    | NO   |     | NULL    |       |
| inicio_de_contrato | date                                                       | NO   |     | NULL    |       |
| sueldo_bruto       | int                                                        | NO   |     | NULL    |       |
| sueldo_liquido     | int                                                        | YES  |     | NULL    |       |
| telefono1          | int                                                        | NO   |     | NULL    |       |
| telefono2          | int                                                        | YES  |     | NULL    |       |
| correo             | varchar(15)                                                | YES  |     | NULL    |       |
| direccion          | varchar(50)                                                | YES  |     | NULL    |       |
+--------------------+------------------------------------------------------------+------+-----+---------+-------+

+---------------------------+------------------------------------------------------------+------+-----+---------+-------+
| Field                     | Type                                                       | Null | Key | Default | Extra |
+---------------------------+------------------------------------------------------------+------+-----+---------+-------+
| rut_empleado              | int                                                        | NO   | MUL | NULL    |       |
| nombre_empleado           | varchar(20)                                                | NO   |     | NULL    |       |
| apellido_paterno_empleado | varchar(20)                                                | NO   |     | NULL    |       |
| apellido_materno_empleado | varchar(20)                                                | NO   |     | NULL    |       |
| especializacion           | enum('Enfermería','Kinesiología','Tecnología','Medico')    | NO   |     | NULL    |       |
| id_paciente               | int                                                        | YES  |     | NULL    |       |
| nombre_paciente           | varchar(20)                                                | YES  |     | NULL    |       |
| apellido_paterno_paciente | varchar(20)                                                | YES  |     | NULL    |       |
| apellido_materno_paciente | varchar(20)                                                | YES  |     | NULL    |       |
| descripcion               | text                                                       | NO   |     | NULL    |       |
| observación               | text                                                       | YES  |     | NULL    |       |
| tipo_de_reporte           | varchar(15)                                                | NO   |     | NULL    |       |
+---------------------------+------------------------------------------------------------+------+-----+---------+-------+

# Reemplazos

+------------------------+------------------------------------------------------------+------+-----+---------+----------------+
| Field                  | Type                                                       | Null | Key | Default | Extra          |
+------------------------+------------------------------------------------------------+------+-----+---------+----------------+
| id_reemplazo           | int                                                        | NO   | PRI | NULL    | auto_increment |
| rut_reemplazado        | int                                                        | NO   | MUL | NULL    |                |
| nombre_reemplazado     | varchar(20)                                                | NO   |     | NULL    |                |
| apellido1_reemplazado  | varchar(20)                                                | NO   |     | NULL    |                |
| apellido2_reemplazado  | varchar(20)                                                | NO   |     | NULL    |                |
| fecha                  | datetime                                                   | YES  |     | NULL    |                |
| especializacion        | enum('Enfermería','Kinesiología','Tecnología','Medico')    | YES  |     | NULL    |                |
| rut_reemplazante       | int                                                        | NO   | MUL | NULL    |                |
| nombre_reemplazante    | varchar(20)                                                | NO   |     | NULL    |                |
| apellido1_reemplazante | varchar(20)                                                | NO   |     | NULL    |                |
| apellido2_reemplazante | varchar(20)                                                | NO   |     | NULL    |                |
| pacientes              | int                                                        | YES  |     | NULL    |                |
| observacion            | text                                                       | YES  |     | NULL    |                |
+------------------------+------------------------------------------------------------+------+-----+---------+----------------+


# Urgencias Médicas
+-----------------+------------------------------------------------------------+------+-----+---------+----------------+
| Field           | Type                                                       | Null | Key | Default | Extra          |
+-----------------+------------------------------------------------------------+------+-----+---------+----------------+
| id_urgencia     | int                                                        | NO   | PRI | NULL    | auto_increment |
| rut_empleado    | int                                                        | NO   | MUL | NULL    |                |
| id_paciente     | int                                                        | NO   |     | NULL    |                |
| especializacion | enum('Enfermería','Kinesiología','Tecnología','Medico')    | NO   |     | NULL    |                |
| fecha           | datetime                                                   | NO   |     | NULL    |                |
| observacion     | text                                                       | NO   |     | NULL    |                |
| ala             | varchar(20)                                                | NO   |     | NULL    |                |
| procedimiento   | text                                                       | NO   |     | NULL    |                |
+-----------------+------------------------------------------------------------+------+-----+---------+----------------+

