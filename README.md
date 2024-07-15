# iSpring

La API Mr. Rebujito está destinada a la organización de ferias, teniendo como principal objetivo facilitar el proceso de petición de licencias a los ayuntamientos por parte de las casetas. Además, el sistema también permitirá a las casetas gestionar todo lo relativo a la administración de sus socios y su carta.

## Contexto

La API Mr. Rebujito está diseñada para mejorar la gestión y organización de ferias, enfocándose en:

- Facilitar el proceso de petición de licencias a los ayuntamientos.
- Permitir a las casetas gestionar la administración de sus socios y su carta.

## Requisitos de Información

1. **Actores del sistema**: Administradores, ayuntamientos, casetas y socios.
    - Para cada actor, el sistema debe almacenar:
      - Nombre
      - Foto opcional
      - Correo electrónico
      - Número de teléfono opcional
      - Dirección opcional
    - Administradores y socios:
      - Primer apellido
      - Segundo apellido opcional
    - Casetas:
      - Razón social
      - Aforo máximo
      - Si es pública o privada
    - Ayuntamiento:
      - Número máximo de licencias que se podrán aceptar
2. **Solicitudes de Licencia**:
    - Las casetas pueden solicitar licencias a los ayuntamientos.
    - Estado de la solicitud: "PENDIENTE", "APROBADA" o "RECHAZADA".
    - Estado inicial: "PENDIENTE" hasta que el ayuntamiento la apruebe o rechace.
3. **Gestión de Socios**:
    - Una caseta puede inscribir un número arbitrario de socios.
4. **Carta de Casetas**:
    - Las casetas pueden tener una carta con productos.
    - Datos de cada producto:
      - Nombre
      - Tipo de alimento ("COMIDA" o "BEBIDA")
      - Precio

## Requisitos Funcionales

1. **Actor no registrado** debe ser capaz de:
    - Registrarse como caseta o socio.
    - Listar los ayuntamientos.
    - Listar y mostrar las casetas y sus cartas.
2. **Actor registrado** debe ser capaz de:
    - Realizar las mismas acciones que un actor no registrado, excepto registrarse.
    - Editar sus datos personales.
3. **Actor registrado como caseta** debe ser capaz de:
    - Gestionar las solicitudes de licencia hechas a los ayuntamientos: listarlas, mostrarlas y crearlas. Si el estado es "PENDIENTE", podrá eliminarla.
    - Gestionar sus cartas: listar, añadir, eliminar y modificar productos.
    - Añadir/Eliminar nuevos socios.
4. **Actor registrado como ayuntamiento** debe ser capaz de:
    - Listar y mostrar todas sus casetas (aquellas con licencias aceptadas).
    - Gestionar las solicitudes de licencia: listar, mostrar, aceptar/rechazar.
5. **Actor registrado como socio** debe ser capaz de:
    - Realizar las mismas acciones que un actor no registrado, excepto registrarse.
    - Listar y mostrar las casetas a las que pertenece.
6. **Actor registrado como administrador** debe ser capaz de:
    - Registrar a otros administradores.
    - Registrar a los ayuntamientos.