---
title: Tipo simple de privilegeType
description: Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a las cuentas de usuario y de grupo. Entre los privilegios de cada usuario se incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- Programador de tareas de tipo simple privilegeType
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4864364a4752d72bd5305c5c2591b7d27391517f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676649"
---
# <a name="privilegetype-simple-type"></a>Tipo simple de privilegeType

Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a las cuentas de usuario y de grupo. Entre los privilegios de cada usuario se incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.

``` syntax
<xs:simpleType name="privilegeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="SeCreateTokenPrivilege"
         />
        <xs:enumeration
            value="SeAssignPrimaryTokenPrivilege"
         />
        <xs:enumeration
            value="SeLockMemoryPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseQuotaPrivilege"
         />
        <xs:enumeration
            value="SeUnsolicitedInputPrivilege"
         />
        <xs:enumeration
            value="SeMachineAccountPrivilege"
         />
        <xs:enumeration
            value="SeTcbPrivilege"
         />
        <xs:enumeration
            value="SeSecurityPrivilege"
         />
        <xs:enumeration
            value="SeTakeOwnershipPrivilege"
         />
        <xs:enumeration
            value="SeLoadDriverPrivilege"
         />
        <xs:enumeration
            value="SeSystemProfilePrivilege"
         />
        <xs:enumeration
            value="SeSystemtimePrivilege"
         />
        <xs:enumeration
            value="SeProfileSingleProcessPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseBasePriorityPrivilege"
         />
        <xs:enumeration
            value="SeCreatePagefilePrivilege"
         />
        <xs:enumeration
            value="SeCreatePermanentPrivilege"
         />
        <xs:enumeration
            value="SeBackupPrivilege"
         />
        <xs:enumeration
            value="SeRestorePrivilege"
         />
        <xs:enumeration
            value="SeShutdownPrivilege"
         />
        <xs:enumeration
            value="SeDebugPrivilege"
         />
        <xs:enumeration
            value="SeAuditPrivilege"
         />
        <xs:enumeration
            value="SeSystemEnvironmentPrivilege"
         />
        <xs:enumeration
            value="SeChangeNotifyPrivilege"
         />
        <xs:enumeration
            value="SeRemoteShutdownPrivilege"
         />
        <xs:enumeration
            value="SeUndockPrivilege"
         />
        <xs:enumeration
            value="SeSyncAgentPrivilege"
         />
        <xs:enumeration
            value="SeEnableDelegationPrivilege"
         />
        <xs:enumeration
            value="SeManageVolumePrivilege"
         />
        <xs:enumeration
            value="SeImpersonatePrivilege"
         />
        <xs:enumeration
            value="SeCreateGlobalPrivilege"
         />
        <xs:enumeration
            value="SeTrustedCredManAccessPrivilege"
         />
        <xs:enumeration
            value="SeRelabelPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseWorkingSetPrivilege"
         />
        <xs:enumeration
            value="SeTimeZonePrivilege"
         />
        <xs:enumeration
            value="SeCreateSymbolicLinkPrivilege"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El tipo simple **privilegeType** define los siguientes valores.



| Value                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | Se requiere para crear un token primario. Derecho de usuario: cree un objeto de token.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | Obligatorio para asignar el token principal de un proceso. Derecho de usuario: reemplazar un token de nivel de proceso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | Necesario para bloquear páginas físicas en la memoria. Derecho de usuario: bloquear páginas en la memoria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | Necesario para aumentar la cuota asignada a un proceso. Derecho de usuario: ajuste de las cuotas de memoria para un proceso. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeUnsolicitedInputPrivilege     | Necesario para leer la entrada no solicitada de un dispositivo terminal. Derecho de usuario: no aplicable. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | Se requiere para crear una cuenta de equipo. Derecho de usuario: agregar estaciones de trabajo al dominio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege                  | Este privilegio identifica su titular como parte de la base del equipo de confianza. A algunos subsistemas protegidos de confianza se les concede este privilegio. Derecho de usuario: actuar como parte del sistema operativo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | Necesario para realizar una serie de funciones relacionadas con la seguridad, como el control y la visualización de los mensajes de auditoría. Este privilegio identifica su titular como operador de seguridad. Derecho de usuario: administrar la auditoría y el registro de seguridad. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | Se requiere para tomar posesión de un objeto sin que se le conceda acceso discrecional. Este privilegio permite que el valor de propietario se establezca únicamente en los valores que el titular puede asignar legítimamente como propietario de un objeto. Derecho de usuario: tomar posesión de archivos u otros objetos. <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | Necesario para cargar o descargar un controlador de dispositivo. Derecho de usuario: cargar y descargar controladores de dispositivo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | Necesario para recopilar información de generación de perfiles para todo el sistema. Derecho de usuario: generar perfiles del rendimiento del sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | Necesario para modificar la hora del sistema. Derecho de usuario: cambiar la hora del sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | Necesario para recopilar información de generación de perfiles para un único proceso. Derecho de usuario: generar perfiles de un solo proceso. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | Necesario para aumentar la prioridad base de un proceso. Derecho de usuario: aumentar la prioridad de programación. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | Se requiere para crear un archivo de paginación. Derecho de usuario: crear un archivo de paginación. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | Requerido para crear un objeto permanente. Derecho de usuario: crear objetos compartidos permanentes. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | Requerido para realizar operaciones de copia de seguridad. Este privilegio hace que el sistema conceda todo el control de acceso de lectura a cualquier archivo, independientemente de la lista de control de acceso (ACL) especificada para el archivo. Cualquier solicitud de acceso que no sea de lectura todavía se evalúa con la ACL. Este privilegio es necesario para RegSaveKey y RegSaveKeyExfunctions. Se conceden los siguientes derechos de acceso si se mantiene este privilegio: \_ control de lectura, \_ seguridad del sistema \_ de acceso, \_ \_ lectura genérica de archivo, recorrido de archivos \_ . Derecho de usuario: copia de seguridad de archivos y directorios. <br/>                                                                                                                                     |
| SeRestorePrivilege              | Necesario para realizar operaciones de restauración. Este privilegio hace que el sistema conceda todo el control de acceso de escritura a cualquier archivo, independientemente de la ACL especificada para el archivo. Cualquier solicitud de acceso que no sea de escritura todavía se evalúa con la ACL. Además, este privilegio le permite establecer cualquier identificador de seguridad (SID) de usuario o grupo válido como propietario de un archivo. Este privilegio es necesario para la función RegLoadKey. Se conceden los siguientes derechos de acceso si se mantiene este privilegio: escribir \_ DAC, escribir \_ propietario \_ , \_ seguridad del sistema de acceso, escribir archivo \_ genérico, archivo Agregar archivo \_ \_ \_ , \_ agregar \_ subdirectorio de archivo, eliminar. Derecho de usuario: restaurar archivos y directorios. <br/> |
| SeShutdownPrivilege             | Necesario para apagar un sistema local. Derecho de usuario: Apague el sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | Necesario para depurar y ajustar la memoria de un proceso que pertenece a otra cuenta. Derecho de usuario: depurar programas. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | Necesario para generar entradas del registro de auditoría. Conceda este privilegio a los servidores seguros. Derecho de usuario: generar auditorías de seguridad. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | Necesario para modificar la memoria RAM no volátil de los sistemas que utilizan este tipo de memoria para almacenar información de configuración. Derecho de usuario: modifique los valores de entorno de firmware. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | Requerido para recibir notificaciones de cambios en archivos o directorios. Este privilegio también hace que el sistema omita todas las comprobaciones de acceso transversal. Está habilitada de forma predeterminada para todos los usuarios. Derecho de usuario: Omitir comprobación de recorrido. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | Necesario para apagar un sistema mediante una solicitud de red. Derecho de usuario: forzar el cierre desde un sistema remoto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | Necesario para desacoplar un equipo portátil. Derecho de usuario: quitar el equipo de la estación de acoplamiento. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | Necesario para que un controlador de dominio use los servicios de sincronización de directorios LDAP. Este privilegio permite al titular leer todos los objetos y propiedades del directorio, independientemente de la protección de los objetos y las propiedades. De forma predeterminada, se asigna a las cuentas de administrador y LocalSystem en los controladores de dominio. Derecho de usuario: sincronizar los datos del servicio de directorio. <br/>                                                                                                                                                                                                                                                                                |
| SeEnableDelegationPrivilege     | Obligatorio para marcar las cuentas de usuario y de equipo como de confianza para la delegación. Derecho de usuario: permitir que las cuentas de equipo y de usuario sean de confianza para la delegación. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | Necesario para habilitar los privilegios de administración de volúmenes. Derecho de usuario: administre los archivos de un volumen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | Requerido para suplantar. Derecho de usuario: suplantar a un cliente tras la autenticación. Windows XP/2000: no se admite este privilegio. <br/> Tenga en cuenta que este valor se admite a partir de Windows Server 2003, Windows XP con SP2 y Windows 2000 con SP4.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | Se requiere para crear objetos de asignación de archivo con nombre en el espacio de nombres global durante Terminal Services sesiones. Este privilegio está habilitado de forma predeterminada para los administradores, los servicios y la cuenta de sistema local. Derecho de usuario: crear objetos globales. Windows XP/2000: no se admite este privilegio. <br/> Tenga en cuenta que este valor se admite a partir de Windows Server 2003, Windows XP con SP2 y Windows 2000 con SP4.<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | Necesario para tener acceso al administrador de credenciales como un llamador de confianza. Derecho de usuario: acceder al administrador de credenciales como un llamador de confianza. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | Necesario para modificar el nivel de integridad obligatorio de un objeto. Derecho de usuario: modifique una etiqueta de objeto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | Necesario para asignar más memoria a las aplicaciones que se ejecutan en el contexto de los usuarios. Derecho de usuario: aumentar un espacio de trabajo del proceso. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | Necesario para ajustar la zona horaria asociada con el reloj interno del equipo. Derecho de usuario: cambie la zona horaria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | Se requiere para crear un vínculo simbólico. Derecho de usuario: crear vínculos simbólicos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





