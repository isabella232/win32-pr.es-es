---
description: Consideraciones para crear o abrir un archivo mediante la función CreateFile.
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Crear y abrir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1430675862b10f9e9221d968242481525dc7632f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668380"
---
# <a name="creating-and-opening-files"></a>Crear y abrir archivos

La función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) puede crear un archivo nuevo o abrir uno existente. Debe especificar el nombre de archivo, las instrucciones de creación y otros atributos. Cuando una aplicación crea un archivo nuevo, el sistema operativo lo agrega al directorio especificado.

El sistema operativo asigna un identificador único, denominado *identificador*, a cada archivo que se abre o se crea mediante [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Una aplicación puede usar este identificador con funciones que leen, escriben y describen el archivo. Es válido hasta que se cierren todas las referencias a ese controlador. Cuando se inicia una aplicación, hereda todos los identificadores abiertos del proceso que lo inició si los identificadores se crearon como heredables.

Una aplicación debe comprobar el valor del identificador devuelto por [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) antes de intentar utilizar el identificador para tener acceso al archivo. Si se produce un error, el valor del identificador será un **\_ \_ valor de identificador no válido** y la aplicación puede usar la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener información de error extendida.

Cuando una aplicación usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), debe usar el parámetro *dwDesiredAccess* para especificar si se va a leer desde el archivo, escribir en el archivo, tanto de lectura como de escritura o de ninguna de las dos. Esto se conoce como solicitar un *modo de acceso*. La aplicación también debe usar el parámetro *dwCreationDisposition* para especificar la acción que se realizará si el archivo ya existe, lo que se conoce como *disposición de creación*. Por ejemplo, una aplicación puede llamar a **CreateFile** con *DwCreationDisposition* establecido en **crear \_ siempre** para crear siempre un nuevo archivo, incluso si ya existe un archivo con el mismo nombre (con lo que se sobrescribe el archivo existente). Si esto se realiza correctamente o no depende de factores como los atributos y la configuración de seguridad del archivo anterior (consulte las secciones siguientes para obtener más información).

Una aplicación también usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para especificar si desea compartir el archivo para lectura, escritura, ambos o ninguno. Esto se conoce como el *modo de uso compartido*. Un archivo abierto que no se comparte (*dwShareMode* se establece en cero) no se puede volver a abrir, ya sea por la aplicación que lo abrió o por otra aplicación, hasta que se haya cerrado su identificador. Esto también se conoce como acceso exclusivo.

Cuando un proceso usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para intentar abrir un archivo que ya se ha abierto en modo de uso compartido (*dwShareMode* establecido en un valor distinto de cero válido), el sistema compara los modos de acceso y uso compartido solicitados con los especificados al abrir el archivo. Si especifica un modo de acceso o de uso compartido que entra en conflicto con los modos especificados en la llamada anterior, se produce un error en **CreateFile** .

En la tabla siguiente se muestran las combinaciones válidas de dos llamadas a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con varios modos de acceso y modos de uso compartido (*dwDesiredAccess*, *dwShareMode* , respectivamente). No importa en qué orden se realizan las llamadas a **CreateFile** . Sin embargo, las operaciones de e/s de archivos subsiguientes en cada identificador de archivo seguirán estando restringidas por los modos de acceso y uso compartido actuales asociados a ese identificador de archivo en particular.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Primera llamada a <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></th>
<th>Dos llamadas válidas a <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

Además de los atributos de archivo estándar, también puede especificar atributos de seguridad incluyendo un puntero a una estructura [**de \_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) como el cuarto parámetro de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Sin embargo, el sistema de archivos subyacente debe ser compatible con la seguridad para que esto tenga algún efecto (por ejemplo, el sistema de archivos NTFS lo admite pero no los distintos sistemas de archivos FAT). Para obtener más información sobre los atributos de seguridad, vea [Access Control](/windows/desktop/SecAuthZ/access-control).

Una aplicación que crea un nuevo archivo puede proporcionar un identificador opcional a un archivo de plantilla, desde el que [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) toma los atributos de archivo y los atributos extendidos para la creación del nuevo archivo.

## <a name="createfile-scenarios"></a>Escenarios de CreateFile

Hay varios escenarios fundamentales para iniciar el acceso a un archivo mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Se resumen como:

-   Crear un nuevo archivo cuando no existe un archivo con ese nombre.
-   Crear un nuevo archivo incluso si ya existe un archivo con el mismo nombre, borrar sus datos e iniciarlos vacíos.
-   Abrir un archivo existente solo si existe y solo está intacto.
-   Abrir un archivo existente solo si existe y truncarlo para que esté vacío.
-   Abrir un archivo siempre: tal y como está, si existe, se crea uno nuevo si no existe.

Estos escenarios se controlan mediante el uso correcto del parámetro *dwCreationDisposition* . A continuación se muestra un desglose de cómo se asignan estos escenarios a los valores para este parámetro y qué ocurre cuando se usan.

Al crear o abrir un archivo nuevo cuando no existe un archivo con ese nombre (*dwCreationDisposition* establecido en **crear \_ nuevo**, **crear \_ siempre** o **abrir \_ siempre**), la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) realiza las acciones siguientes:

-   Combina los atributos y marcas de archivo especificados por *dwFlagsAndAttributes* con el **archivo de \_ atributos \_ File**.
-   Establece la longitud del archivo en cero.
-   Copia los atributos extendidos proporcionados por el archivo de plantilla en el nuevo archivo si se especifica el parámetro *hTemplateFile* (esto invalida todos los **\_ atributos \_ \* de archivo* _ Flags especificados anteriormente).
-   Establece la marca de herencia especificada por el miembro _ *bInheritHandle** y el descriptor de seguridad especificado por el miembro **LpSecurityDescriptor** del parámetro *lpSecurityAttributes* (estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), si se proporciona.

Al crear un nuevo archivo incluso si ya existe un archivo con el mismo nombre (*dwCreationDisposition* establecido en **crear \_ siempre**), la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) realiza las siguientes acciones:

-   Comprueba los atributos de archivo actuales y la configuración de seguridad para el acceso de escritura, con error si se deniega.
-   Combina los atributos y marcas de archivo especificados por *dwFlagsAndAttributes* con el archivo de atributos de **archivo \_ \_** y los atributos de archivo existentes.
-   Establece la longitud del archivo en cero (es decir, los datos que estaban en el archivo ya no están disponibles y el archivo está vacío).
-   Copia los atributos extendidos proporcionados por el archivo de plantilla en el nuevo archivo si se especifica el parámetro *hTemplateFile* (esto invalida todos los **\_ atributos \_ \* de archivo* _ Flags especificados anteriormente).
-   Establece la marca de herencia especificada por el miembro _ *bInheritHandle** del parámetro *lpSecurityAttributes* (estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ) si se proporciona, pero omite el miembro **lpSecurityDescriptor** de la estructura de **\_ atributos de seguridad** .
-   Si, de lo contrario, se realiza correctamente (es decir, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) devuelve un identificador válido), la llamada a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) producirá el error de código **\_ ya \_ existente**, aunque en este caso de uso concreto no es realmente un error como tal (si pretende crear un archivo "nuevo" (vacío) en lugar del existente).

Al abrir un archivo existente (*dwCreationDisposition* establecido en **abrir \_ existente**, **abrir \_ siempre** o **truncar \_ existente**), la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) realiza las siguientes acciones:

-   Comprueba los atributos de archivo actuales y la configuración de seguridad para el acceso solicitado, con error si se deniega.
-   Combina las marcas de archivo (**\_ marca \_ \* de archivo* _) especificadas por _dwFlagsAndAttributes * con los atributos de archivo existentes y omite todos los atributos de archivo (* * \_ atributo \_ \* de archivo* _) especificados por _dwFlagsAndAttributes *.
-   Establece la longitud del archivo en cero solo si *dwCreationDisposition* está establecido en **TRUNCATE \_ Existing**, de lo contrario, se mantiene la longitud actual del archivo y el archivo se abre tal cual.
-   Omite el parámetro *hTemplateFile* .
-   Establece la marca de herencia especificada por el miembro **bInheritHandle** del parámetro *lpSecurityAttributes* (estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ) si se proporciona, pero omite el miembro **lpSecurityDescriptor** de la estructura de **\_ atributos de seguridad** .

## <a name="file-attributes-and-directories"></a>Atributos y directorios de archivo

Los atributos de archivo forman parte de los metadatos asociados a un archivo o directorio, cada uno con su propio propósito y reglas sobre cómo se puede establecer y cambiar. Algunos de estos atributos solo se aplican a archivos y otros solo a directorios. Por ejemplo, el atributo de **archivo \_ \_ Directorio de atributo** solo se aplica a los directorios: el sistema de archivos lo usa para determinar si un objeto en el disco es un directorio, pero no se puede cambiar para un objeto de sistema de archivos existente.

Algunos atributos de archivo se pueden establecer para un directorio, pero solo tienen significado para los archivos creados en ese directorio, actuando como atributos predeterminados. Por ejemplo, se puede establecer el **atributo de archivo \_ \_ comprimido** en un objeto de directorio, pero como el propio objeto de directorio no contiene datos reales, no está realmente comprimido; sin embargo, los directorios marcados con este atributo indican al sistema de archivos que debe comprimir los archivos nuevos agregados a ese directorio. Cualquier atributo de archivo que se pueda establecer en un directorio y también se establecerá para los nuevos archivos agregados a ese directorio se conoce como un *atributo heredado*.

La función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) proporciona un parámetro para establecer ciertos atributos de archivo cuando se crea un archivo. En general, estos atributos son los más comunes para que una aplicación los use en el momento de la creación del archivo, pero no todos los atributos de archivo posibles están disponibles para **CreateFile**. Algunos atributos de archivo requieren el uso de otras funciones, como [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa), [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)o [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) después de que el archivo ya exista. En el caso del **\_ \_ Directorio de atributos de archivo**, la función [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) es necesaria en el momento de la creación porque **CreateFile** no puede crear directorios. Los otros atributos de archivo que requieren un tratamiento especial son el **\_ \_ \_ punto de reanálisis del atributo de archivo** y el **\_ \_ \_ archivo disperso del atributo de archivo**, que requieren **DeviceIoControl**. Para obtener más información, vea [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).

Como se indicó anteriormente, la herencia de atributos de archivo se produce cuando se crea un archivo con atributos de archivo leídos de los atributos de directorio donde se ubicará el archivo. En la tabla siguiente se resumen estos atributos heredados y cómo se relacionan con las capacidades de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .



| Estado del atributo de directorio                                      | Funcionalidad de invalidación de herencia [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para nuevos archivos      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Archivo \_ de Conjunto de atributos \_ comprimidos** .<br/>                | Sin control. Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para borrar.<br/>    |
| **Archivo \_ de ATRIBUTO \_ comprimido** no establecido.<br/>            | Sin control. Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para establecer.<br/>      |
| **Archivo \_ de Conjunto de atributos \_ cifrados** .<br/>                 | Sin control. Use [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| **Archivo \_ de ATRIBUTO \_ cifrado** no establecido.<br/>             | Se puede establecer mediante [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).<br/>                       |
| **Archivo \_ de El atributo no tiene un conjunto \_ \_ \_ indizado de contenido** .<br/>     | Sin control. Use [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) para borrar.<br/> |
| **Archivo \_ de No se ha establecido el atributo \_ no \_ contenido \_ indizado** .<br/> | Sin control. Use [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) para establecer.<br/>   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de acceso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Constantes de atributo de archivo**](file-attribute-constants.md)
</dt> <dt>

[Compresión y descompresión de archivos](file-compression-and-decompression.md)
</dt> <dt>

[Cifrado de archivos](file-encryption.md)
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[Identificadores y objetos](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[Controlar la herencia](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[Apertura de un archivo para lectura o escritura](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

