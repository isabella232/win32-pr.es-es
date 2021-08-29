---
description: El Windows de seguridad le permite controlar el acceso al administrador de control de servicios (SCM) y a los objetos de servicio.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Seguridad del servicio y derechos de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1674ae1170066daca7f4998fb6fd777ffc2dbec856ff1177fefd860daadb5e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888714"
---
# <a name="service-security-and-access-rights"></a>Seguridad del servicio y derechos de acceso

El Windows de seguridad le permite controlar el acceso al administrador de control de servicios (SCM) y a los objetos de servicio. En las secciones siguientes se proporciona información detallada:

-   [Derechos de acceso del Administrador de control de servicios](#access-rights-for-the-service-control-manager)
-   [Derechos de acceso para un servicio](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a>Derechos de acceso del Administrador de control de servicios

Estos son los derechos de acceso específicos para el SCM.



| Derecho de acceso                                   | Descripción                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SC \_ ADMINISTRADOR \_ DE \_ TODO ACCESO** (0xF003F)         | Incluye **STANDARD \_ RIGHTS \_ REQUIRED**, además de todos los derechos de acceso de esta tabla.                                                                                                                                                                                                                                                                                 |
| **SC \_ MANAGER \_ CREATE \_ SERVICE** (0x0002)      | Necesario para llamar a la [**función CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para crear un objeto de servicio y agregarlo a la base de datos.                                                                                                                                                                                                                                              |
| **SC \_ MANAGER \_ CONNECT** (0x0001)              | Necesario para conectarse al administrador de control de servicios.                                                                                                                                                                                                                                                                                                                      |
| **SC \_ SERVICIO \_ ENUMERATE \_ DE MANAGER** (0x0004)   | Se requiere para llamar [**a las funciones EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) o [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para enumerar los servicios que se encuentran en la base de datos.<br/> Es necesario llamar a [**la función NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para recibir una notificación cuando se crea o elimina cualquier servicio.<br/> |
| **SC \_ BLOQUEO \_ DE ADMINISTRADOR** (0x0008)                 | Necesario para llamar a la [**función LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) para adquirir un bloqueo en la base de datos.                                                                                                                                                                                                                                                      |
| **SC \_ MANAGER \_ MODIFY BOOT CONFIG \_ \_ (CONFIGURACIÓN** 0X0020) | Necesario para llamar a [**la función NotifyBootConfigStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                                                                                                                                                                                                                                                                                  |
| **SC \_ ESTADO \_ DEL BLOQUEO DE CONSULTA \_ \_ DEL** ADMINISTRADOR (0x0010)  | Necesario para llamar a la [**función QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) para recuperar la información de estado de bloqueo de la base de datos.                                                                                                                                                                                                                         |



 

Estos son los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para el SCM.



<table>
<thead>
<tr class="header">
<th>Derecho de acceso</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SC_MANAGER_CREATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_LOCK</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_ALL</strong></td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Un proceso con los derechos de acceso correctos puede abrir un identificador para el SCM que se puede usar en las funciones [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)y [**QueryServiceLockStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) Solo los procesos con privilegios de administrador pueden abrir identificadores en el SCM que pueden usar las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**LockServiceDatabase.**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)

El sistema crea el descriptor de seguridad para el SCM. Para obtener o establecer el descriptor de seguridad para el SCM, use las funciones [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) y [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) con un identificador para el objeto SCManager.

**Windows Server 2003 y Windows XP:** A diferencia de la mayoría de los demás objetos protegibles, no se puede modificar el descriptor de seguridad del SCM. Este comportamiento ha cambiado a partir de Windows Server 2003 con Service Pack 1 (SP1).

Se conceden los siguientes derechos de acceso.



<table>
<thead>
<tr class="header">
<th>Cuenta</th>
<th>Derechos de acceso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Usuarios autenticados remotos</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Usuarios autenticados locales (incluidos LocalService y NetworkService)</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem (Sistema local)</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administradores</td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Tenga en cuenta que los usuarios remotos autenticados a través de la red pero que no han iniciado sesión de forma interactiva pueden conectarse al SCM, pero no realizar operaciones que requieran otros derechos de acceso. Para realizar estas operaciones, el usuario debe iniciar sesión de forma interactiva o el servicio debe usar una de las cuentas de servicio.

**Windows Server 2003 y Windows XP:** A los usuarios autenticados remotos se les conceden los derechos de acceso **SC \_ MANAGER \_ CONNECT,** **SC MANAGER \_ \_ ENUMERATE \_ SERVICE**, **SC MANAGER QUERY LOCK \_ \_ \_ \_ STATUS** y **STANDARD RIGHTS \_ \_ READ.** Estos derechos de acceso están restringidos como se describe en la tabla anterior a partir de Windows Server 2003 con SP1

Cuando un proceso usa la [**función OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para abrir un identificador en una base de datos de servicios instalados, puede solicitar derechos de acceso. El sistema realiza una comprobación de seguridad en el descriptor de seguridad del SCM antes de conceder los derechos de acceso solicitados.

## <a name="access-rights-for-a-service"></a>Derechos de acceso para un servicio

Estos son los derechos de acceso específicos para un servicio.



| Derecho de acceso                                | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SERVICE \_ ALL \_ ACCESS** (0xF01FF)          | Incluye **STANDARD RIGHTS REQUIRED \_ \_ además** de todos los derechos de acceso de esta tabla.                                                                                                                                                                                                                                                                                              |
| **SERVICIO \_ CAMBIAR \_ CONFIGURACIÓN** (0x0002)        | Necesario para llamar a [**las funciones ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) para cambiar la configuración del servicio. Dado que esto concede al autor de la llamada el derecho a cambiar el archivo ejecutable que ejecuta el sistema, solo se debe conceder a los administradores.                                                              |
| **SERVICIO \_ ENUMERAR \_ DEPENDIENTES** (0x0008) | Necesario para llamar a [**la función EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar todos los servicios dependientes del servicio.                                                                                                                                                                                                                                         |
| **SERVICE \_ INTERROGATE** (0x0080)           | Es necesario llamar a la [**función ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para pedir al servicio que informe de su estado inmediatamente.                                                                                                                                                                                                                                                          |
| **SERVICIO \_ PAUSE \_ CONTINUE** (0x0040)       | Necesario para llamar a la [**función ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para pausar o continuar el servicio.                                                                                                                                                                                                                                                                             |
| **SERVICE \_ CONFIGURACIÓN \_ DE CONSULTA** (0x0001)         | Necesario para llamar a [**las funciones QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) y [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para consultar la configuración del servicio.                                                                                                                                                                                                           |
| **SERVICIO \_ ESTADO \_ DE CONSULTA** (0x0004)         | Es necesario llamar a [**la función QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) o [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) para preguntar al administrador de control de servicios sobre el estado del servicio.<br/> Necesario para llamar a la [**función NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para recibir una notificación cuando un servicio cambia de estado.<br/> |
| **SERVICE \_ START** (0x0010)                 | Necesario para llamar a [**la función StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) para iniciar el servicio.                                                                                                                                                                                                                                                                                             |
| **SERVICE \_ STOP** (0x0020)                  | Necesario para llamar a [**la función ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para detener el servicio.                                                                                                                                                                                                                                                                                          |
| **SERVICIO \_ \_CONTROL DEFINIDO POR EL \_ USUARIO**(0x0100) | Necesario para llamar a [**la función ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para especificar un código de control definido por el usuario.                                                                                                                                                                                                                                                                       |



 

Estos son los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) para un servicio.



| Derecho de acceso                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEGURIDAD \_ DEL SISTEMA DE \_ ACCESO** | Necesario para llamar a [**la función QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) [**o SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para acceder a sacl. La manera adecuada de obtener este acceso es habilitar el privilegio **SE SECURITY \_ \_ NAME** en el token de acceso actual del autor de la llamada, abrir el identificador para acceder a **ACCESS SYSTEM \_ \_ SECURITY** y, a continuación, deshabilitar el privilegio.[](/windows/desktop/SecAuthZ/privileges) |
| **DELETE**   (0x10000)       | Necesario para llamar a [**la función DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para eliminar el servicio.                                                                                                                                                                                                                                                                                                                                                  |
| **READ \_ CONTROL**  (0x20000)    | Necesario para llamar a [**la función QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) para consultar el descriptor de seguridad del objeto de servicio.                                                                                                                                                                                                                                                                                  |
| **ESCRITURA \_ DAC**  (0x40000)    | Necesario para llamar a [**la función SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar el **miembro Dacl** del descriptor de seguridad del objeto de servicio.                                                                                                                                                                                                                                                                   |
| **ESCRITURA \_ OWNER** (0x80000)   | Es necesario llamar a [**la función SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar los miembros **Owner** y **Group** del descriptor de seguridad del objeto de servicio.                                                                                                                                                                                                                                                   |



 

Estos son los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para un servicio.



<table>
<thead>
<tr class="header">
<th>Derecho de acceso</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SERVICE_CHANGE_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

El SCM crea el descriptor de seguridad de un objeto de servicio cuando el servicio se instala mediante la [**función CreateService.**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) El descriptor de seguridad predeterminado de un objeto de servicio concede el acceso siguiente.



<table>
<thead>
<tr class="header">
<th>Cuenta</th>
<th>Derechos de acceso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Usuarios autenticados remotos</td>
<td>No se concede de forma predeterminada. <strong>Windows Server 2003 con SP1: SERVICE_USER_DEFINED_CONTROL</strong><br/> <strong>Windows Server 2003 y Windows XP:</strong> Los derechos de acceso de los usuarios autenticados de forma remota son los mismos que para los usuarios autenticados locales.<br/></td>
</tr>
<tr class="even">
<td>Usuarios autenticados locales (incluidos LocalService y NetworkService)</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem (Sistema local)</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administradores</td>
<td><dl> <strong>DELETE</strong><br />
<strong>READ_CONTROL</strong><br />
<strong>SERVICE_ALL_ACCESS</strong><br />
<strong>WRITE_DAC</strong><br />
<strong>WRITE_OWNER</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Para realizar cualquier operación, el usuario debe iniciar sesión de forma interactiva o el servicio debe usar una de las cuentas de servicio.

Para obtener o establecer el descriptor de seguridad para un objeto de servicio, use las [**funciones QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) [**y SetServiceObjectSecurity.**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) Para obtener más información, [vea Modificar la DACL para un servicio](modifying-the-dacl-for-a-service.md).

Cuando un proceso usa la [**función OpenService,**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad para el objeto de servicio.

Conceder determinados derechos de acceso a usuarios que no son de confianza (como **SERVICE \_ CHANGE \_ CONFIG** o **SERVICE \_ STOP)** puede permitirles interferir con la ejecución del servicio y, posiblemente, permitirles ejecutar aplicaciones en la cuenta LocalSystem.

Cuando se llama a la función [**EnumServicesStatusEx,**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) si el autor de la llamada no tiene el derecho de acceso **SERVICE QUERY \_ \_ STATUS** a un servicio, el servicio se omite en modo silencioso de la lista de servicios devueltos al cliente.

 

