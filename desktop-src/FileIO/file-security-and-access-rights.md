---
description: Dado que los archivos son objetos protegibles, el acceso a ellos está regulado por el modelo de control de acceso que rige el acceso a todos los demás objetos protegibles de Windows.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Derechos de acceso y seguridad de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f33df8117debef1d7f8349ae2fb479974e59ec582d7be758a753726706b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696255"
---
# <a name="file-security-and-access-rights"></a>Derechos de acceso y seguridad de archivos

Dado que los archivos [son objetos](/windows/desktop/SecAuthZ/securable-objects)protegibles, el acceso a ellos está regulado por el modelo de control de acceso que rige el acceso a todos los demás objetos protegibles de Windows. Para obtener una explicación detallada de este modelo, [vea Access Control](/windows/desktop/SecAuthZ/access-control).

Puede especificar un [descriptor de seguridad para](/windows/desktop/api/winnt/ns-winnt-security_descriptor) un archivo o directorio al llamar a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) [**o CreateDirectoryEx.**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) Si especifica **NULL para** el parámetro *lpSecurityAttributes,* el archivo o directorio obtiene un descriptor de seguridad predeterminado. Las listas de control de acceso (ACL) del descriptor de seguridad predeterminado para un archivo o directorio se heredan de su directorio primario. Tenga en cuenta que solo se asigna un descriptor de seguridad predeterminado cuando se acaba de crear un archivo o directorio, y no cuando se cambia el nombre o se mueve.

Para recuperar el descriptor de seguridad de un objeto de archivo o directorio, llame a la [**función GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) o [**GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) Para cambiar el descriptor de seguridad de un objeto de archivo o directorio, llame a la [**función SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) [**o SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Los derechos de acceso válidos para archivos y directorios incluyen los derechos de acceso estándar **DELETE**, **READ \_ CONTROL**, **WRITE \_ DAC,** **WRITE \_ OWNER** [y](/windows/desktop/SecAuthZ/standard-access-rights) **SYNCHRONIZE** . En la tabla [**de Constantes de derechos de**](file-access-rights-constants.md) acceso a archivos se enumeran los derechos de acceso específicos de los archivos y directorios.

Aunque el derecho de acceso [](/windows/desktop/SecAuthZ/standard-access-rights) **SYNCHRONIZE** se define dentro de la lista de derechos de acceso estándar como el derecho para especificar un identificador de archivo en una de las funciones de espera, al usar operaciones asincrónicas de E/S de archivos, debe esperar en el identificador de evento contenido en una estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) configurada correctamente en lugar de usar el identificador de archivo con el derecho de acceso **SYNCHRONIZE** para la sincronización.

Estos son los derechos [de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para archivos y directorios.



<table>
<thead>
<tr class="header">
<th>Derecho de acceso</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FILE_GENERIC_EXECUTE</strong></td>
<td><dl> <strong>FILE_EXECUTE</strong><br />
<strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>Sincronizar</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>Sincronizar</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>Sincronizar</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows compara los derechos de acceso solicitados y la información del token de acceso del subproceso con la información del descriptor de seguridad del objeto de archivo o directorio. Si la comparación no prohíbe que se concedan todos los derechos de acceso solicitados, se devuelve un identificador al objeto al subproceso y se conceden los derechos de acceso. Para obtener más información sobre este proceso, vea [Interacción entre subprocesos y objetos protegibles.](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects)

De forma predeterminada, la autorización de acceso a un archivo o directorio se controla estrictamente mediante las ACL del descriptor de seguridad asociado a ese archivo o directorio. En concreto, el descriptor de seguridad de un directorio primario no se usa para controlar el acceso a ningún archivo o directorio secundario. El derecho de [acceso](/windows/desktop/SecAuthZ/access-rights-and-access-masks) **FILE \_ TRAVERSE** se puede aplicar quitando el privilegio BYPASS TRAVERSE **\_ \_ CHECKING** [de](/windows/desktop/SecAuthZ/privileges) los usuarios. Esto no se recomienda en el caso general, ya que muchos programas no controlan correctamente los errores de recorrido del directorio. El uso principal del derecho de acceso **\_ FILE TRAVERSE** en los directorios es habilitar la conformidad con ciertos estándares IEEE e ISO POSIX cuando la interoperabilidad con sistemas Unix es un requisito.

El modelo de seguridad Windows proporciona una manera de que un directorio secundario herede o se le impida heredar una o varias de las ACE en el descriptor de seguridad del directorio primario. Cada ACE contiene información que determina cómo se puede heredar y si tendrá un efecto en el objeto de directorio de herencia. Por ejemplo, algunas ACE heredadas controlan el acceso al objeto de directorio heredado y se denominan *ACE eficaces.* Todas las demás ACE se *denominan ACE de solo herencia.*

El Windows de seguridad también aplica la herencia automática de ace a objetos secundarios de acuerdo con las reglas [de herencia ace](/windows/desktop/SecAuthZ/ace-inheritance-rules). Esta herencia automática, junto con la información de herencia de cada ACE, determina cómo se pasan las restricciones de seguridad a la jerarquía de directorios.

Tenga en cuenta que no puede usar una ACE con acceso denegado para denegar solo el acceso **DE \_** LECTURA GENÉRICA o solo EL ACCESO **DE \_ ESCRITURA** GENÉRICO a un archivo. Esto se debe a que, para los objetos de archivo, las asignaciones genéricas para **GENERIC \_ READ** o **GENERIC \_ WRITE** incluyen el derecho de acceso **SYNCHRONIZE.** Si una ACE deniega el acceso DE ESCRITURA **GENÉRICO \_** a un administrador de confianza y este solicita acceso DE LECTURA GENÉRICO, se producirá un error en la solicitud porque la solicitud incluye implícitamente el acceso **SYNCHRONIZE,** que la ACE deniega implícitamente, y viceversa. **\_** En lugar de usar las ACE con acceso denegado, use las ACE con acceso permitido para permitir explícitamente los derechos de acceso permitidos.

Otro medio de administrar el acceso a los objetos de almacenamiento es el cifrado. La implementación del cifrado del sistema de archivos Windows es el sistema de archivos cifrado o EFS. EFS cifra solo los archivos y no los directorios. La ventaja del cifrado es que proporciona protección adicional a los archivos que se aplican en los medios y no a través del sistema de archivos y la arquitectura de control de acceso Windows estándar. Para obtener más información sobre el cifrado de archivos, vea [Cifrado de archivos.](file-encryption.md)

En la mayoría de los casos, la capacidad de leer y escribir la configuración de seguridad de un archivo o un objeto de directorio está restringida a los procesos en modo kernel. Claramente, no desea que ningún proceso de usuario pueda cambiar la propiedad o la restricción de acceso en el archivo o directorio privado. Sin embargo, una aplicación de copia de seguridad no podría completar su trabajo de copia de seguridad del archivo si las restricciones de acceso que ha colocado en el archivo o directorio no permiten que el proceso de modo de usuario de la aplicación lo lea. Las aplicaciones de copia de seguridad deben ser capaces de invalidar la configuración de seguridad de los objetos de archivo y directorio para garantizar una copia de seguridad completa. Del mismo modo, si una aplicación de copia de seguridad intenta escribir una copia de seguridad del archivo en la copia residentes en disco y se deniegan explícitamente los privilegios de escritura al proceso de la aplicación de copia de seguridad, la operación de restauración no se puede completar. En este caso también, la aplicación de copia de seguridad debe ser capaz de invalidar la configuración de control de acceso del archivo.

Los **SE \_ de acceso BACKUP \_ NAME** **y SE restore \_ \_ NAME** se crearon específicamente para proporcionar esta capacidad para realizar copias de seguridad de las aplicaciones. Si estos privilegios se han concedido y habilitado en el token de acceso del proceso de la aplicación de copia de seguridad, puede llamar a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir el archivo o directorio para la copia de seguridad, especificando el derecho de acceso **READ \_ CONTROL** estándar como el valor del parámetro *dwDesiredAccess.* Sin embargo, para identificar el proceso de llamada como un proceso de copia de seguridad, la llamada a **CreateFile** debe incluir la marca **FILE FLAG BACKUP \_ \_ \_ SEMANTICS** en el *parámetro dwFlagsAndAttributes.* La sintaxis completa de la llamada de función es la siguiente:


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Esto permitirá que el proceso de la aplicación de copia de seguridad abra el archivo e invalide la comprobación de seguridad estándar. Para restaurar el archivo, la aplicación de copia de seguridad usaría la siguiente sintaxis de llamada [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) al abrir el archivo para que se escriba.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Hay situaciones en las que una aplicación de copia de seguridad debe poder cambiar la configuración de control de acceso de un archivo o directorio. Un ejemplo es cuando la configuración de control de acceso de la copia residentes en disco de un archivo o directorio es diferente de la copia de seguridad. Esto sucedería si esta configuración se cambiase después de que se realizara una copia de seguridad del archivo o directorio, o si estaba dañado.

La **marca FILE FLAG BACKUP \_ \_ \_ SEMANTICS** especificada en la llamada a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) proporciona al proceso de la aplicación de copia de seguridad permiso para leer la configuración de control de acceso del archivo o directorio. Con este permiso, el proceso de la aplicación de copia de seguridad puede llamar a [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) y [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) para leer y restablecer la configuración de control de acceso.

Si una aplicación de copia de seguridad debe tener acceso a la configuración de [control](/windows/desktop/SecAuthZ/access-control-lists)de acceso de nivel de sistema , la marca **ACCESS SYSTEM \_ \_ SECURITY** debe especificarse en el valor del parámetro *dwDesiredAccess* pasado a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

Las aplicaciones de copia [**de seguridad llaman a BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) para leer los archivos y directorios especificados para la operación de restauración, y [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) para escribirlos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
