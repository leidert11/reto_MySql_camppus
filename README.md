### Bloque 1

##### Consultas

1. Listar los nombres de los usuarios

   ```sql
   select nombre from tblUsuarios;
   ```

2. Calcular el saldo máximo de los usuarios de sexo “Mujer”

     ```sql
     select sexo,max(saldo) as saldo_mayor_mujer from tblUsuarios where sexo = 'M';
     ```

3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY

     ```sql
     select nombre,telefono from tblUsuarios where marca = 'NOKIA' or marca = 'BLACKBERRY' or marca = 'SONY';

     SELECT nombre, telefono
     FROM tblUsuarios
     WHERE marca IN ('NOKIA', 'BLACKBERRY', 'SONY');

     ```

4. Contar los usuarios sin saldo o inactivos

     ```sql
     select count(*) as total_usuarios_sin_saldo_inactivos from tblUsuarios where saldo = 0 OR activo = 0;
     ```

5. Listar el login de los usuarios con nivel 1, 2 o 3

     ```sql
     select usuario as login from tblUsuarios where nivel in (1,2,3);
     ```

6. Listar los números de teléfono con saldo menor o igual a 300

     ```sql
     select telefono from tblUsuarios where saldo <= 300;
     ```

7. Calcular la suma de los saldos de los usuarios de la compañia telefónica NEXTEL

     ```sql
     select sum(saldo) as suma_saldos_nextel from tblUsuarios where compania = 'NEXTEL';
     ```

8. Contar el número de usuarios por compañía telefónica

     ```sql
     select compania, count(usuario) as cantidad_usuarios from tblUsuarios group by compania;
     ```

9. Contar el número de usuarios por nivel

     ```sql
     select nivel, count(usuario) as cantidad_usuario from tblUsuarios group by nivel;
     ```

10. Listar el login de los usuarios con nivel 2

      ```sql
     select usuario as login from tblUsuarios where nivel = 2 ;
      ```

11. Mostrar el email de los usuarios que usan gmail

      ```sql
     select usuario, email  from tblUsuarios where email like '%@gmail.com';
      ```

12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA

      ```sql
     select nombre, telefono from tblUsuarios where marca in ('LG','SAMSUNG','MOTOROLA');
      ```

------

### Bloque 2

##### Consultas

1. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG

     ```sql
     select nombre, telefono from tblUsuarios where marca not in ('LG','SAMSUNG');
     ```

2. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL

     ```sql
     select usuario,telefono from tblUsuarios where compania like '%IUSACELL%';
     ```

3. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL

     ```sql
     select usuario , telefono from tblUsuarios where compania !='TELCEL';
     ```

4. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA

     ```sql
     select avg(saldo) as promedio_telefono_nokia from tblUsuarios where marca = 'NOKIA';
     ```

5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL

     ```sql
     select usuario as login , telefono from tblUsuarios where compania in ('IUSACELL','AXEL');
     ```

6. Mostrar el email de los usuarios que no usan yahoo

     ```sql
     select email from tblUsuarios where email not like '%@yahoo.com';
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL

     ```sql
     select usuario as login  , telefono from tblUsuarios where compania not in ('TELCEL','IUSACELL');
     ```

8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON

     ```sql
     select usuario , telefono  from tblUsuarios where compania ='UNEFON';
     ```

9. Listar las diferentes marcas de celular en orden alfabético descendentemente

     ```sql
     select distinct marca from tblUsuarios order by marca desc;
     ```

10. Listar las diferentes compañias en orden alfabético aleatorio

      ```sql
     select distinct compania from tblUsuarios order by rand();
      ```

11. Listar el login de los usuarios con nivel 0 o 2

      ```sql
     select usuario as login from tblUsuarios where nivel in (0,2);
      ```

12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG

      ```sql
     select avg(saldo) as promedio_usuarios_lg from tblUsuarios where marca = 'LG' ;
      ```

------

### Bloque 3

##### Consultas

1. Listar el login de los usuarios con nivel 1 o 3

     ```sql
     select usuario as login from tblUsuarios where nivel in (1,3);
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY

     ```sql
     select nombre ,telefono from tblUsuarios where marca !='BLACKBERRY';
     ```

3. Listar el login de los usuarios con nivel 3

     ```sql
     select usuario as login from tblUsuarios where nivel = 3;
     ```

4. Listar el login de los usuarios con nivel 0

     ```sql
     select usuario as login from tblUsuarios where nivel = 0;
     ```

5. Listar el login de los usuarios con nivel 1

     ```sql
     select usuario as login from tblUsuarios where nivel = 1;
     ```

6. Contar el número de usuarios por sexo

     ```sql
     select sexo , count(*) as numero_usuarios from tblUsuarios group by sexo;
     ```
     ```sql
     SELECT 
    COUNT(CASE WHEN sexo = 'H' THEN 1 END) AS hombres,
    COUNT(CASE WHEN sexo = 'M' THEN 1 END) AS mujeres
     FROM tblUsuarios;
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica AT&T

     ```sql
     select usuario as login , telefono from tblUsuarios where compania in ('AT&T');
     ```

8. Listar las diferentes compañias en orden alfabético descendentemente

     ```sql
     select distinct compania from tblUsuarios order by compania desc;
     ```

9. Listar el login de los usuarios inactivos

     ```sql
     select usuario as login , activo from tblUsuarios where activo is false ;
     ```

10. Listar los números de teléfono sin saldo

      ```sql
     select telefono from tblUsuarios where saldo is false;
      ```

11. Calcular el saldo mínimo de los usuarios de sexo “Hombre”

      ```sql
     select min(saldo) as saldo_minimo_hombre from tblUsuarios where sexo in ('H');
      ```

12. Listar los números de teléfono con saldo mayor a 300

      ```sql
     select telefono from tblUsuarios where saldo > 300;
      ```

------

### Bloque 4

##### Consultas

1. Contar el número de usuarios por marca de teléfono

     ```sql
      # Solucion en 'sql'
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG

     ```sql
      # Solucion en 'sql'
     ```

3. Listar las diferentes compañias en orden alfabético ascendentemente

     ```sql
      # Solucion en 'sql'
     ```

4. Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON

     ```sql
      # Solucion en 'sql'
     ```

5. Mostrar el email de los usuarios que usan hotmail

     ```sql
      # Solucion en 'sql'
     ```

6. Listar los nombres de los usuarios sin saldo o inactivos

     ```sql
      # Solucion en 'sql'
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónicaIUSACELL o TELCEL

     ```sql
      # Solucion en 'sql'
     ```

8. Listar las diferentes marcas de celular en orden alfabético ascendentemente

     ```sql
      # Solucion en 'sql'
     ```

9. Listar las diferentes marcas de celular en orden alfabético aleatorio

     ```sql
      # Solucion en 'sql'
     ```

10. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON

      ```sql
       # Solucion en 'sql'
      ```

11. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA

      ```sql
       # Solucion en 'sql'
      ```

12. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL

      ```sql
       # Solucion en 'sql'
      ```
