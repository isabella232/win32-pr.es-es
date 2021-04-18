---
description: Dado que los archivos son objetos protegibles, el acceso a ellos está regulado por el modelo de control de acceso que rige el acceso a todos los demás objetos protegibles en Windows.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Derechos de acceso y seguridad de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b161dd78c7585cf6de2781d7339787a22bde95dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666841"
---
# <a name="file-security-and-access-rights"></a>Derechos de acceso y seguridad de archivos

Dado que los archivos son [objetos protegibles](/windows/desktop/SecAuthZ/securable-objects), el acceso a ellos está regulado por el modelo de control de acceso que rige el acceso a todos los demás objetos protegibles en Windows. Para obtener una explicación detallada de este modelo, vea [Access Control](/windows/desktop/SecAuthZ/access-control).

Puede especificar un [descriptor de seguridad](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para un archivo o directorio cuando llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)o [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) . Si especifica **null** para el parámetro *lpSecurityAttributes* , el archivo o el directorio obtiene un descriptor de seguridad predeterminado. Las listas de control de acceso (ACL) del descriptor de seguridad predeterminado para un archivo o directorio se heredan de su directorio principal. Tenga en cuenta que se asigna un descriptor de seguridad predeterminado solo cuando se crea un archivo o un directorio recientemente, y no cuando se cambia el nombre o se mueve.

Para recuperar el descriptor de seguridad de un archivo o un objeto de directorio, llame a la función [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) o [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Para cambiar el descriptor de seguridad de un archivo o un objeto de directorio, llame a la función [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) o [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Los derechos de acceso válidos para archivos y directorios incluyen los derechos de acceso de **eliminación**, **\_ control de lectura**, **escritura de \_ DAC**, **\_ propietario de escritura** y **sincronizar** [estándar](/windows/desktop/SecAuthZ/standard-access-rights). La tabla de [**constantes de derechos de acceso a archivos**](file-access-rights-constants.md) enumera los derechos de acceso que son específicos de los archivos y directorios.

Aunque el derecho de acceso **SYNCHRONIZE** se define en la lista de [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) como el derecho a especificar un identificador de archivo en una de las funciones de espera, al usar operaciones asincrónicas de e/s de archivos, debe esperar en el controlador de eventos contenido en una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) correctamente configurada en lugar de usar el identificador de archivo con el derecho de acceso **SYNCHRONIZE** para la sincronización

A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para archivos y directorios.



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
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows compara los derechos de acceso solicitados y la información del token de acceso del subproceso con la información del descriptor de seguridad del objeto de archivo o directorio. Si la comparación no prohíbe que se concedan todos los derechos de acceso solicitados, se devuelve un identificador al objeto al subproceso y se conceden los derechos de acceso. Para obtener más información sobre este proceso, vea [interacción entre subprocesos y objetos protegibles](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects).

De forma predeterminada, la autorización para el acceso a un archivo o directorio lo controlan estrictamente las ACL en el descriptor de seguridad asociado a ese archivo o directorio. En concreto, el descriptor de seguridad de un directorio primario no se utiliza para controlar el acceso a cualquier archivo o directorio secundario. Se puede aplicar el [derecho de acceso a](/windows/desktop/SecAuthZ/access-rights-and-access-masks) **\_ recorrido de archivos** si se quita el [privilegio](/windows/desktop/SecAuthZ/privileges) **omitir \_ \_ comprobación de recorrido** de los usuarios. Esto no se recomienda en el caso general, ya que muchos programas no controlan correctamente los errores transversales del directorio. El uso principal del derecho de acceso de **\_ recorrido de archivos** en los directorios es habilitar la conformidad con determinados estándares POSIX de IEEE e ISO cuando la interoperabilidad con sistemas Unix es un requisito.

El modelo de seguridad de Windows proporciona una manera de que un directorio secundario herede o no se herede, una o varias de las ACE del descriptor de seguridad del directorio principal. Cada ACE contiene información que determina cómo se puede heredar y si tendrá efecto en el objeto de directorio heredado. Por ejemplo, algunas ACE heredadas controlan el acceso al objeto de directorio heredado, y se denominan *ACE efectivas*. Todas las demás ACE se denominan *ACE de solo herencia*.

El modelo de seguridad de Windows también aplica la herencia automática de ACE a objetos secundarios de acuerdo con las [reglas de herencia de ACE](/windows/desktop/SecAuthZ/ace-inheritance-rules). Esta herencia automática, junto con la información de herencia en cada ACE, determina cómo se pasan las restricciones de seguridad a la jerarquía de directorios.

Tenga en cuenta que no puede usar una ACE de acceso denegado para denegar solo el acceso de **\_ escritura** genérico o de solo **\_ lectura** a un archivo. Esto se debe a que, en el caso de los objetos de archivo, las asignaciones genéricas tanto para **\_ lectura** genérica como para **\_ escritura genérica** incluyen el derecho de acceso **SYNCHRONIZE** . Si una ACE deniega el acceso de **\_ escritura genérico** a un administrador de confianza y el administrador de confianza solicita acceso de **\_ lectura genérico** , se producirá un error en la solicitud porque la solicitud incluye implícitamente el acceso a la **sincronización** que la ACE deniega implícitamente y viceversa. En lugar de usar ACE de acceso denegado, use ACE con acceso permitido para permitir explícitamente los derechos de acceso permitidos.

Otro medio para administrar el acceso a los objetos de almacenamiento es el cifrado. La implementación del cifrado del sistema de archivos en Windows es el sistema de archivos cifrado o EFS. EFS solo cifra archivos y no directorios. La ventaja del cifrado es que proporciona protección adicional a los archivos que se aplican en los medios y no a través del sistema de archivos y la arquitectura estándar de control de acceso de Windows. Para obtener más información sobre el cifrado de archivos, vea [cifrado de archivos](file-encryption.md).

En la mayoría de los casos, la capacidad de leer y escribir la configuración de seguridad de un objeto de archivo o directorio está restringida a los procesos de modo kernel. Claramente, no desea que ningún proceso de usuario pueda cambiar la propiedad o la restricción de acceso en el archivo o directorio privado. Sin embargo, una aplicación de copia de seguridad no podría completar su trabajo de copia de seguridad del archivo si las restricciones de acceso que ha colocado en el archivo o directorio no permiten que el proceso de modo de usuario de la aplicación lo lea. Las aplicaciones de copia de seguridad deben poder invalidar la configuración de seguridad de los objetos de archivo y directorio para garantizar una copia de seguridad completa. Del mismo modo, si una aplicación de copia de seguridad intenta escribir una copia de seguridad del archivo a través de la copia residente en disco y deniega explícitamente privilegios de escritura al proceso de la aplicación de copia de seguridad, la operación de restauración no se puede completar. En este caso, la aplicación de copia de seguridad debe ser capaz de invalidar la configuración de control de acceso del archivo.

Los privilegios de acceso de nombre de **\_ copia de seguridad \_** y **\_ restauración \_** de se han creado específicamente para proporcionar esta capacidad para realizar copias de seguridad de aplicaciones. Si estos privilegios se han concedido y habilitado en el token de acceso del proceso de la aplicación de copia de seguridad, puede llamar a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir el archivo o directorio de la copia de seguridad, especificando el derecho de acceso de **\_ control de lectura** estándar como el valor del parámetro *dwDesiredAccess* . Sin embargo, para identificar el proceso de llamada como un proceso de copia de seguridad, la llamada a **CreateFile** debe incluir la marca de **semántica de copia de \_ \_ seguridad \_ del marcador de archivo** en el parámetro *dwFlagsAndAttributes* . La sintaxis completa de la llamada de función es la siguiente:


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Esto permitirá al proceso de la aplicación de copia de seguridad abrir el archivo e invalidar la comprobación de seguridad estándar. Para restaurar el archivo, la aplicación de copia de seguridad usaría la siguiente sintaxis de llamada [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) al abrir el archivo que se va a escribir.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Hay situaciones en las que una aplicación de copia de seguridad debe poder cambiar la configuración del control de acceso de un archivo o directorio. Un ejemplo es cuando la configuración de control de acceso de la copia residente en disco de un archivo o directorio es diferente de la copia de seguridad. Esto ocurrirá si se cambiara esta configuración después de que se realizara la copia de seguridad del archivo o directorio, o si estuviera dañado.

La marca de semántica de copia de seguridad del marcador de archivo especificada en la llamada a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) proporciona al proceso de la aplicación de copia de seguridad permiso para leer la configuración de control de acceso del archivo o directorio. **\_ \_ \_** Con este permiso, el proceso de la aplicación de copia de seguridad puede llamar a [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) y [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) para leer y restablecer la configuración de control de acceso.

Si una aplicación de copia de seguridad debe tener acceso a la [configuración de control de acceso](/windows/desktop/SecAuthZ/access-control-lists)de nivel de sistema, la marca de **\_ \_ seguridad del sistema de acceso** debe especificarse en el valor del parámetro *dwDesiredAccess* pasado a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

Las aplicaciones de copia de seguridad llaman a [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) para leer los archivos y directorios especificados para la operación de restauración y [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) para escribirlos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
