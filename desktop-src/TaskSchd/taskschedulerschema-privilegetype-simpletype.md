---
title: tipo simple privilegeType
description: Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a cuentas de usuario y grupo. Los privilegios de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- tipo simple privilegeType Programador de tareas
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4502c22e31ca131dabd6d776337c3693a4d4bf4d7753734cf0e6291cf234fbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002293"
---
# <a name="privilegetype-simple-type"></a>tipo simple privilegeType

Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a cuentas de usuario y grupo. Los privilegios de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.

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

El **tipo simple privilegeType** define los siguientes valores.



| Value                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | Necesario para crear un token principal. Derecho de usuario: cree un objeto de token.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | Necesario para asignar el token principal de un proceso. Derecho de usuario: reemplace un token de nivel de proceso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | Necesario para bloquear páginas físicas en memoria. Derecho de usuario: bloquear páginas en memoria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | Necesario para aumentar la cuota asignada a un proceso. Derecho de usuario: ajuste las cuotas de memoria de un proceso. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeUnsolicitedInputPrivilege     | Necesario para leer la entrada no solicitada desde un dispositivo terminal. Derecho de usuario: no aplicable. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | Necesario para crear una cuenta de equipo. Derecho de usuario: agregue estaciones de trabajo al dominio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege                  | Este privilegio identifica a su titular como parte de la base de equipos de confianza. A algunos subsistemas protegidos de confianza se les concede este privilegio. Derecho de usuario: actúa como parte del sistema operativo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | Necesario para realizar una serie de funciones relacionadas con la seguridad, como controlar y ver mensajes de auditoría. Este privilegio identifica a su titular como operador de seguridad. Derecho de usuario: administre la auditoría y el registro de seguridad. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | Necesario para tomar posesión de un objeto sin que se le conceda acceso discrecional. Este privilegio permite establecer el valor de propietario solo en los valores que el titular puede asignar legítimamente como propietario de un objeto. Derecho de usuario: tome posesión de archivos u otros objetos. <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | Necesario para cargar o descargar un controlador de dispositivo. Derecho de usuario: cargue y descargue los controladores de dispositivo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | Necesario para recopilar información de generación de perfiles para todo el sistema. Derecho de usuario: rendimiento del sistema de perfiles. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | Necesario para modificar la hora del sistema. Derecho de usuario: cambie la hora del sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | Necesario para recopilar información de generación de perfiles para un único proceso. Derecho de usuario: perfil de proceso único. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | Necesario para aumentar la prioridad base de un proceso. Derecho de usuario: aumente la prioridad de programación. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | Necesario para crear un archivo de paginación. Derecho de usuario: cree un archivo de paginación. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | Necesario para crear un objeto permanente. Derecho de usuario: cree objetos compartidos permanentes. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | Necesario para realizar operaciones de copia de seguridad. Este privilegio hace que el sistema conceda todo el control de acceso de lectura a cualquier archivo, independientemente de la lista de control de acceso (ACL) especificada para el archivo. Cualquier solicitud de acceso que no sea de lectura se sigue evaluando con la ACL. RegSaveKey y RegSaveKeyExfunctions requieren este privilegio. Si se mantiene este privilegio, se conceden los siguientes derechos de acceso: CONTROL DE LECTURA, SEGURIDAD DEL SISTEMA DE ACCESO, LECTURA GENÉRICA DE \_ \_ \_ \_ \_ ARCHIVOS, RECORRIDO \_ DE ARCHIVOS. Derecho de usuario: haga una copia de seguridad de archivos y directorios. <br/>                                                                                                                                     |
| SeRestorePrivilege              | Necesario para realizar operaciones de restauración. Este privilegio hace que el sistema conceda todo el control de acceso de escritura a cualquier archivo, independientemente de la ACL especificada para el archivo. Cualquier solicitud de acceso que no sea de escritura se sigue evaluando con la ACL. Además, este privilegio le permite establecer cualquier identificador de seguridad de usuario o grupo (SID) válido como propietario de un archivo. La función RegLoadKey requiere este privilegio. Si se mantiene este privilegio, se conceden los siguientes derechos de acceso: \_ WRITE DAC, WRITE \_ OWNER, ACCESS \_ SYSTEM \_ SECURITY, FILE GENERIC \_ \_ WRITE, FILE ADD \_ \_ FILE, FILE ADD \_ \_ SUBDIRECTORY y DELETE. Derecho de usuario: restaure archivos y directorios. <br/> |
| SeShutdownPrivilege             | Necesario para apagar un sistema local. Derecho de usuario: apague el sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | Necesario para depurar y ajustar la memoria de un proceso propiedad de otra cuenta. Derecho de usuario: depurar programas. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | Necesario para generar entradas de registro de auditoría. Dé este privilegio a los servidores seguros. Derecho de usuario: genere auditorías de seguridad. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | Necesario para modificar la RAM no volátil de los sistemas que usan este tipo de memoria para almacenar información de configuración. Derecho de usuario: modifique los valores del entorno de firmware. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | Necesario para recibir notificaciones de cambios en archivos o directorios. Este privilegio también hace que el sistema omita todas las comprobaciones de acceso transversal. Está habilitada de forma predeterminada para todos los usuarios. Derecho de usuario: omitir la comprobación de recorrido. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | Necesario para apagar un sistema mediante una solicitud de red. Derecho de usuario: forzar el apagado desde un sistema remoto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | Necesario para desacoplar un equipo portátil. Derecho de usuario: quite el equipo de la estación de acoplamiento. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | Necesario para que un controlador de dominio use los servicios de sincronización de directorios LDAP. Este privilegio permite al titular leer todos los objetos y propiedades del directorio, independientemente de la protección de los objetos y propiedades. De forma predeterminada, se asigna a las cuentas Administrador y LocalSystem en controladores de dominio. Derecho de usuario: sincronice los datos del servicio de directorio. <br/>                                                                                                                                                                                                                                                                                |
| SeEnableDelegationPrivilege     | Se requiere para marcar las cuentas de usuario y equipo como de confianza para la delegación. Derecho de usuario: permite que las cuentas de equipo y usuario sean de confianza para la delegación. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | Necesario para habilitar los privilegios de administración de volúmenes. Derecho de usuario: administre los archivos de un volumen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | Necesario para suplantar. Derecho de usuario: suplantar un cliente después de la autenticación. Windows XP/2000: este privilegio no se admite. <br/> Tenga en cuenta que este valor se admite a partir de Windows Server 2003, Windows XP con SP2 y Windows 2000 con SP4.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | Necesario para crear objetos de asignación de archivos con nombre en el espacio de nombres global durante las sesiones de Terminal Services. Este privilegio está habilitado de forma predeterminada para administradores, servicios y la cuenta del sistema local. Derecho de usuario: cree objetos globales. Windows XP/2000: este privilegio no se admite. <br/> Tenga en cuenta que este valor se admite a partir de Windows Server 2003, Windows XP con SP2 y Windows 2000 con SP4.<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | Necesario para acceder a Administrador de credenciales como llamador de confianza. Derecho de usuario: acceda Administrador de credenciales como llamador de confianza. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | Necesario para modificar el nivel de integridad obligatorio de un objeto. Derecho de usuario: modifique una etiqueta de objeto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | Necesario para asignar más memoria a las aplicaciones que se ejecutan en el contexto de los usuarios. Derecho de usuario: aumente un conjunto de trabajo de proceso. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | Necesario para ajustar la zona horaria asociada al reloj interno del equipo. Derecho de usuario: cambie la zona horaria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | Necesario para crear un vínculo simbólico. Derecho de usuario: cree vínculos simbólicos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





