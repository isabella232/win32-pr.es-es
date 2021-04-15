---
description: El modelo de seguridad de Windows permite controlar el acceso al administrador de control de servicios (SCM) y a los objetos de servicio.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Derechos de acceso y seguridad del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668466"
---
# <a name="service-security-and-access-rights"></a>Derechos de acceso y seguridad del servicio

El modelo de seguridad de Windows permite controlar el acceso al administrador de control de servicios (SCM) y a los objetos de servicio. En las secciones siguientes se proporciona información detallada:

-   [Derechos de acceso para el administrador de control de servicios](#access-rights-for-the-service-control-manager)
-   [Derechos de acceso para un servicio](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a>Derechos de acceso para el administrador de control de servicios

A continuación se muestran los derechos de acceso específicos para el SCM.



| Derecho de acceso                                   | Descripción                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SC \_ ADMINISTRADOR \_ todo \_ acceso** (0xF003F)         | Incluye **los \_ derechos estándar \_ necesarios**, además de todos los derechos de acceso de esta tabla.                                                                                                                                                                                                                                                                                 |
| **SC \_ \_Crear \_ servicio de administración** (0x0002)      | Necesario para llamar a la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para crear un objeto de servicio y agregarlo a la base de datos.                                                                                                                                                                                                                                              |
| **SC \_ \_Conexión de administrador** (0x0001)              | Necesario para conectarse al administrador de control de servicios.                                                                                                                                                                                                                                                                                                                      |
| **SC \_ \_Enumerar \_ servicio** (0x0004)   | Necesario para llamar a la función [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) o [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para enumerar los servicios que están en la base de datos.<br/> Necesario para llamar a la función [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para recibir una notificación cuando se crea o se elimina un servicio.<br/> |
| **SC \_ \_Bloqueo de administrador** (0x0008)                 | Necesario para llamar a la función [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) para adquirir un bloqueo en la base de datos.                                                                                                                                                                                                                                                      |
| **SC \_ ADMINISTRADOR \_ modificar \_ \_ configuración de arranque** (0x0020) | Necesario para llamar a la función [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .                                                                                                                                                                                                                                                                                  |
| **SC \_ \_Estado de \_ bloqueo \_ de consulta de administrador** (0x0010)  | Necesario para llamar a la función [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) para recuperar la información de estado de bloqueo de la base de datos.                                                                                                                                                                                                                         |



 

A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para el SCM.



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



 

Un proceso con los derechos de acceso correctos puede abrir un identificador del SCM que se puede usar en las funciones [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)y [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) . Solo los procesos con privilegios de administrador pueden abrir identificadores en el SCM que las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) pueden usar.

El sistema crea el descriptor de seguridad para el SCM. Para obtener o establecer el descriptor de seguridad para el SCM, utilice las funciones [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) y [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) con un identificador para el objeto SCManager.

**Windows Server 2003 y Windows XP:** A diferencia de la mayoría de los demás objetos protegibles, no se puede modificar el descriptor de seguridad para el SCM. Este comportamiento ha cambiado a partir de Windows Server 2003 con Service Pack 1 (SP1).

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
<td>Usuarios autenticados localmente (incluido LocalService y NetworkService)</td>
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



 

Tenga en cuenta que los usuarios remotos autenticados a través de la red, pero que no han iniciado sesión de forma interactiva, pueden conectarse al SCM pero no realizar operaciones que requieran otros derechos de acceso. Para realizar estas operaciones, el usuario debe haber iniciado sesión de forma interactiva o el servicio debe usar una de las cuentas de servicio.

**Windows Server 2003 y Windows XP:** A los usuarios autenticados remotos se les conceden los derechos de acceso de **\_ \_ lectura** de **SC \_ Manager \_**, SC Manager y el **\_ \_ \_ servicio de enumeración** de SC Manager. **\_ \_ \_ \_** Estos derechos de acceso están restringidos como se describe en la tabla anterior a partir de Windows Server 2003 con SP1.

Cuando un proceso utiliza la función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para abrir un identificador de una base de datos de servicios instalados, puede solicitar derechos de acceso. El sistema realiza una comprobación de seguridad en el descriptor de seguridad del SCM antes de conceder los derechos de acceso solicitados.

## <a name="access-rights-for-a-service"></a>Derechos de acceso para un servicio

A continuación se muestran los derechos de acceso específicos para un servicio.



| Derecho de acceso                                | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Servicio \_ de TODO el \_ acceso** (0xF01FF)          | Incluye **los \_ derechos estándar \_ necesarios** además de todos los derechos de acceso de esta tabla.                                                                                                                                                                                                                                                                                              |
| **Servicio \_ de CAMBIAR \_ configuración** (0x0002)        | Necesario para llamar a la función [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) para cambiar la configuración del servicio. Dado que esto concede al llamador el derecho de cambiar el archivo ejecutable que ejecuta el sistema, solo se debe conceder a los administradores.                                                              |
| **Servicio \_ de ENUMERAr \_ dependientes** (0x0008) | Necesario para llamar a la función [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar todos los servicios que dependen del servicio.                                                                                                                                                                                                                                         |
| **Servicio \_ de INTERROGAte** (0x0080)           | Necesario para llamar a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para pedir al servicio que informe de su estado inmediatamente.                                                                                                                                                                                                                                                          |
| **Servicio \_ de Pausar \_ continuar** (0x0040)       | Necesario para llamar a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para pausar o continuar el servicio.                                                                                                                                                                                                                                                                             |
| **Servicio \_ de \_Configuración de consulta** (0x0001)         | Necesario para llamar a las funciones [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) y [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para consultar la configuración del servicio.                                                                                                                                                                                                           |
| **Servicio \_ de \_Estado** de la consulta (0x0004)         | Necesario para llamar a la función [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) o [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) para solicitar al administrador de control de servicios el estado del servicio.<br/> Necesario para llamar a la función [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para recibir una notificación cuando un servicio cambia de estado.<br/> |
| **Servicio \_ de INICIAR** (0x0010)                 | Necesario para llamar a la función [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) para iniciar el servicio.                                                                                                                                                                                                                                                                                             |
| **Servicio \_ de DETENER** (0x0020)                  | Necesario para llamar a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para detener el servicio.                                                                                                                                                                                                                                                                                          |
| **Servicio \_ de \_ \_ Control definido por el usuario**(0x0100) | Necesario para llamar a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para especificar un código de control definido por el usuario.                                                                                                                                                                                                                                                                       |



 

A continuación se muestran los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) para un servicio.



| Derecho de acceso                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ACCESO a la \_ seguridad del sistema \_** | Necesario para llamar a la función [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) o [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para tener acceso a la SACL. La manera adecuada de obtener este acceso es habilitar el [**privilegio**](/windows/desktop/SecAuthZ/privileges) de **\_ \_ nombre de seguridad de se** en el token de acceso actual del autor de la llamada, abrir el identificador para tener acceso al acceso de **\_ \_ seguridad del sistema** y, a continuación, deshabilitar el privilegio. |
| **Eliminar**   (0x10000)       | Necesario para llamar a la función [**actividades**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para eliminar el servicio.                                                                                                                                                                                                                                                                                                                                                  |
| **Leer \_ CONTROL**  (0x20000)    | Necesario para llamar a la función [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) para consultar el descriptor de seguridad del objeto de servicio.                                                                                                                                                                                                                                                                                  |
| **Escribir \_ DAC**  (0x40000)    | Necesario para llamar a la función [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar el miembro **DACL** del descriptor de seguridad del objeto de servicio.                                                                                                                                                                                                                                                                   |
| **Escribir \_ PROPIETARIO** (0x80000)   | Necesario para llamar a la función [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar el **propietario** y los miembros del **Grupo** del descriptor de seguridad del objeto de servicio.                                                                                                                                                                                                                                                   |



 

A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para un servicio.



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



 

El SCM crea el descriptor de seguridad de un objeto de servicio cuando la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) instala el servicio. El descriptor de seguridad predeterminado de un objeto de servicio concede el siguiente acceso.



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
<td>No se concede de forma predeterminada. <strong>Windows Server 2003 con SP1: SERVICE_USER_DEFINED_CONTROL</strong><br/> <strong>Windows Server 2003 y Windows XP:</strong> Los derechos de acceso para los usuarios autenticados remotos son los mismos que para los usuarios autenticados localmente.<br/></td>
</tr>
<tr class="even">
<td>Usuarios autenticados localmente (incluido LocalService y NetworkService)</td>
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



 

Para realizar cualquier operación, el usuario debe haber iniciado sesión de forma interactiva o el servicio debe usar una de las cuentas de servicio.

Para obtener o establecer el descriptor de seguridad de un objeto de servicio, utilice las funciones [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) y [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Para obtener más información, consulte [modificar la DACL para un servicio](modifying-the-dacl-for-a-service.md).

Cuando un proceso utiliza la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto de servicio.

Conceder determinados derechos de acceso a los usuarios que no son de confianza (como la **\_ \_ configuración de cambio de servicio** o la **\_ detención del servicio**) pueden permitirles interferir en la ejecución del servicio y, posiblemente, permitirles ejecutar aplicaciones con la cuenta LocalSystem.

Cuando se llama a la [**función EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) , si el autor de la llamada no tiene el derecho de acceso de **\_ \_ Estado de consulta de servicio** a un servicio, el servicio se omite de forma silenciosa en la lista de servicios devueltos al cliente.

 

