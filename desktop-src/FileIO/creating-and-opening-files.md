---
description: Consideraciones para crear o abrir un archivo mediante la función CreateFile.
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Crear y abrir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e80449942fbceb39c37604bf6d8b5410d171d195
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469932"
---
# <a name="creating-and-opening-files"></a>Crear y abrir archivos

La [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) puede crear un archivo o abrir uno existente. Debe especificar el nombre de archivo, las instrucciones de creación y otros atributos. Cuando una aplicación crea un nuevo archivo, el sistema operativo lo agrega al directorio especificado.

El sistema operativo asigna un identificador único, denominado identificador *,* a cada archivo que se abre o se crea mediante [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Una aplicación puede usar este identificador con funciones que leen, escriben y describen el archivo. Es válido hasta que se cierran todas las referencias a ese identificador. Cuando se inicia una aplicación, hereda todos los identificadores abiertos del proceso que la inició si los identificadores se crearon como heredables.

Una aplicación debe comprobar el valor del identificador devuelto por [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) antes de intentar usar el identificador para acceder al archivo. Si se produce un error, el valor del identificador será **INVALID \_ HANDLE \_ VALUE** y la aplicación puede usar la [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener información de error extendida.

Cuando una aplicación usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), debe usar el parámetro *dwDesiredAccess* para especificar si pretende leer desde el archivo, escribir en el archivo, leer y escribir, o ninguno de ellos. Esto se conoce como solicitud de un *modo de acceso*. La aplicación también debe usar el parámetro *dwCreationDisposition* para especificar qué acción realizar si el archivo ya existe, conocido como disposición *de creación*. Por ejemplo, una aplicación puede llamar a **CreateFile** con *dwCreationDisposition* establecido en **CREATE \_ ALWAYS** para crear siempre un archivo nuevo, incluso si ya existe un archivo con el mismo nombre (sobrescribiendo así el archivo existente). Si esto se realiza correctamente o no, depende de factores como los atributos del archivo anterior y la configuración de seguridad (consulte las secciones siguientes para obtener más información).

Una aplicación también usa [**CreateFile para**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) especificar si desea compartir el archivo para leer, escribir, ambos o ninguno. Esto se conoce como modo *de uso compartido.* Un archivo abierto que no se comparte *(dwShareMode* establecido en cero) no se puede abrir de nuevo, ya sea por la aplicación que lo abrió o por otra aplicación, hasta que se haya cerrado su identificador. Esto también se conoce como acceso exclusivo.

Cuando un proceso usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para intentar abrir un archivo que ya se ha abierto en modo de uso compartido *(dwShareMode* establecido en un valor distinto de cero válido), el sistema compara los modos de acceso y uso compartido solicitados con los especificados cuando se abrió el archivo. Si especifica un modo de acceso o uso compartido que entra en conflicto con los modos especificados en la llamada anterior, **CreateFile produce un** error.

En la tabla siguiente se muestran las combinaciones válidas de dos llamadas a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mediante varios modos de acceso y modos de uso compartido *(dwDesiredAccess* y *dwShareMode* respectivamente). No importa en qué orden se realizan las **llamadas a CreateFile.** Sin embargo, las operaciones de E/S de archivos posteriores en cada identificador de archivo seguirán estando restringidas por los modos de acceso y uso compartido actuales asociados a ese identificador de archivo concreto.




| Primera llamada a <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a> | Segundas llamadas válidas <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>a CreateFile</strong></a> | 
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 




 

Además de los atributos de archivo estándar, también puede especificar atributos de seguridad incluyendo un puntero a una estructura [**ATRIBUTOS \_ DE**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) SEGURIDAD como cuarto parámetro [**de CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Sin embargo, el sistema de archivos subyacente debe admitir la seguridad para que esto tenga algún efecto (por ejemplo, el sistema de archivos NTFS lo admite, pero los distintos sistemas de archivos FAT no lo hacen). Para obtener más información sobre los atributos de seguridad, [vea Access Control](/windows/desktop/SecAuthZ/access-control).

Una aplicación que crea un nuevo archivo puede proporcionar un identificador opcional a un archivo de plantilla, desde el que [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) toma atributos de archivo y atributos extendidos para la creación del nuevo archivo.

## <a name="createfile-scenarios"></a>Escenarios de CreateFile

Hay varios escenarios fundamentales para iniciar el acceso a un archivo mediante la [**función CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Se resumen como:

-   Crear un nuevo archivo cuando aún no existe un archivo con ese nombre.
-   Crear un nuevo archivo incluso si ya existe un archivo con el mismo nombre, borrar sus datos e iniciar vacío.
-   Abrir un archivo existente solo si existe y solo intacto.
-   Abrir un archivo existente solo si existe, truncando para que esté vacío.
-   Abrir un archivo siempre: tal y como está si existe, creando uno nuevo si no existe.

Estos escenarios se controlan mediante el uso adecuado del *parámetro dwCreationDisposition.* A continuación se muestra un desglose de cómo se asignan estos escenarios a los valores de este parámetro y lo que ocurre cuando se usan.

Al crear o abrir un archivo nuevo cuando aún no existe un archivo con ese nombre *(dwCreationDisposition* establecido en **CREATE \_ NEW,** **CREATE \_ ALWAYS** o **OPEN \_ ALWAYS),** la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) realiza las siguientes acciones:

-   Combina los atributos y marcas de archivo especificados por *dwFlagsAndAttributes* con **FILE ATTRIBUTE \_ \_ ARCHIVE.**
-   Establece la longitud del archivo en cero.
-   Copia los atributos extendidos proporcionados por el archivo de plantilla en el nuevo archivo si se especifica el parámetro *hTemplateFile* (esto invalida todas las marcas **\_ FILE ATTRIBUTE \_ \*** especificadas anteriormente).
-   Establece la marca inherit especificada por el miembro **bInheritHandle** y el descriptor de seguridad especificados por el miembro **lpSecurityDescriptor** del parámetro *lpSecurityAttributes* (estructura [**SECURITY \_ ATTRIBUTES),**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) si se proporciona.

Al crear un nuevo archivo incluso si ya existe un archivo con el mismo nombre *(dwCreationDisposition* establecido en **CREATE \_ ALWAYS),** la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) realiza las siguientes acciones:

-   Comprueba los atributos de archivo actuales y la configuración de seguridad para el acceso de escritura, lo que da error si se deniega.
-   Combina los atributos y marcas de archivo especificados por *dwFlagsAndAttributes* con **FILE ATTRIBUTE \_ \_ ARCHIVE** y los atributos de archivo existentes.
-   Establece la longitud del archivo en cero (es decir, los datos que había en el archivo ya no están disponibles y el archivo está vacío).
-   Copia los atributos extendidos proporcionados por el archivo de plantilla en el nuevo archivo si se especifica el parámetro *hTemplateFile* (esto invalida todas las marcas **\_ FILE ATTRIBUTE \_ \*** especificadas anteriormente).
-   Establece la marca inherit especificada por el miembro **bInheritHandle** del parámetro *lpSecurityAttributes* [**(estructura SECURITY \_ ATTRIBUTES)**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) si se proporciona, pero omite el miembro **lpSecurityDescriptor** de la estructura **SECURITY \_ ATTRIBUTES.**
-   Si se realiza correctamente (es decir, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) devuelve un identificador válido), la llamada a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) producirá el código **ERROR ALREADY \_ \_ EXISTS**, aunque para este caso de uso concreto no sea realmente un error como tal (si se pretende crear un archivo "nuevo" (vacío) en lugar del existente).

Al abrir un archivo existente *(dwCreationDisposition* establecido en **OPEN \_ EXISTING,** **OPEN \_ ALWAYS** o **TRUNCATE \_ EXISTING),** la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) realiza las siguientes acciones:

-   Comprueba los atributos de archivo actuales y la configuración de seguridad para el acceso solicitado, lo que da error si se deniega.
-   Combina las marcas de archivo **(FILE \_ FLAG \_ \** _) especificadas por _dwFlagsAndAttributes* con los atributos de \_ \_ \** archivo existentes y omite los atributos de archivo (**FILE ATTRIBUTE _) especificados por _dwFlagsAndAttributes*.
-   Establece la longitud del archivo en cero solo si *dwCreationDisposition* está establecido en **TRUNCATE \_ EXISTING**; de lo contrario, se mantiene la longitud del archivo actual y el archivo se abre tal y como está.
-   Omite el *parámetro hTemplateFile.*
-   Establece la marca inherit especificada por el miembro **bInheritHandle** del parámetro *lpSecurityAttributes* [**(estructura SECURITY \_ ATTRIBUTES)**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) si se proporciona, pero omite el miembro **lpSecurityDescriptor** de la estructura **SECURITY \_ ATTRIBUTES.**

## <a name="file-attributes-and-directories"></a>Atributos y directorios de archivo

Los atributos de archivo forman parte de los metadatos asociados a un archivo o directorio, cada uno con su propio propósito y reglas sobre cómo se pueden establecer y cambiar. Algunos de estos atributos solo se aplican a los archivos y otros solo a los directorios. Por ejemplo, el atributo **FILE \_ ATTRIBUTE \_ DIRECTORY** solo se aplica a directorios: el sistema de archivos lo usa para determinar si un objeto del disco es un directorio, pero no se puede cambiar para un objeto del sistema de archivos existente.

Algunos atributos de archivo se pueden establecer para un directorio, pero solo tienen significado para los archivos creados en ese directorio, que actúan como atributos predeterminados. Por ejemplo, **FILE \_ ATTRIBUTE \_ COMPRESSED** se puede establecer en un objeto de directorio, pero como el propio objeto de directorio no contiene datos reales, no está realmente comprimido; sin embargo, los directorios marcados con este atributo le piden al sistema de archivos que comprima los nuevos archivos agregados a ese directorio. Cualquier atributo de archivo que se pueda establecer en un directorio y que también se establecerá para los nuevos archivos agregados a ese directorio se conoce como *atributo heredado.*

La [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) proporciona un parámetro para establecer determinados atributos de archivo cuando se crea un archivo. En general, estos atributos son los más comunes para que una aplicación los use en el momento de la creación del archivo, pero no todos los atributos de archivo posibles están disponibles para **CreateFile.** Algunos atributos de archivo requieren el uso de otras funciones, como [**SetFileAttributes,**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)o [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) después de que el archivo ya exista. En el caso de **FILE \_ ATTRIBUTE \_ DIRECTORY,** la [**función CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) es necesaria en el momento de la creación porque **CreateFile** no puede crear directorios. Los otros atributos de archivo que requieren un control especial son **FILE \_ ATTRIBUTE \_ REPARSE \_ POINT** y **FILE ATTRIBUTE \_ \_ SPARSE \_ FILE**, que **requieren DeviceIoControl**. Para obtener más información, [**vea SetFileAttributes.**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)

Como se indicó anteriormente, la herencia de atributos de archivo se produce cuando se crea un archivo con atributos de archivo leídos de los atributos de directorio donde se ubicará el archivo. En la tabla siguiente se resumen estos atributos heredados y cómo se relacionan con las [**funcionalidades de CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)



| Estado del atributo de directorio                                      | [**Funcionalidad de invalidación**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) de herencia de CreateFile para nuevos archivos      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **FILE \_ CONJUNTO \_ DE ATRIBUTOS COMPRIMIDOS.**<br/>                | Sin control. Use [**DeviceIoControl para**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) borrar.<br/>    |
| **FILE \_ ATTRIBUTE \_ COMPRESSED** no establecido.<br/>            | Sin control. Use [**DeviceIoControl para**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) establecer.<br/>      |
| **FILE \_ CONJUNTO \_ DE ATRIBUTOS CIFRADOS.**<br/>                 | Sin control. Use [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| **FILE \_ ATTRIBUTE \_ ENCRYPTED** no establecido.<br/>             | Se puede establecer mediante [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).<br/>                       |
| **FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED** SET.<br/>     | Sin control. Use [**SetFileAttributes para**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) borrar.<br/> |
| **FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED** no establecido.<br/> | Sin control. Use [**SetFileAttributes para**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) establecer.<br/>   |



 

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

 

