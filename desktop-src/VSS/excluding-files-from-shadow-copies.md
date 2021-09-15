---
description: En Windows Vista y Windows Server 2008 y versiones posteriores, el desarrollador de una aplicación o un escritor de VSS puede optar por excluir determinados archivos de instantáneas.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Exclusión de archivos de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473375"
---
# <a name="excluding-files-from-shadow-copies"></a>Exclusión de archivos de instantáneas

En Windows Vista y Windows Server 2008 y versiones posteriores, el desarrollador de una aplicación o un escritor de VSS puede optar por excluir determinados archivos de instantáneas.

El impacto en el rendimiento y el uso del área de almacenamiento de instantáneas (también denominado "área de diferencia") de un archivo en una instantánea están directamente relacionados con la cantidad de cambios en el contenido del archivo después de crear la instantánea. Además, la exclusión de archivos de instantáneas puede ralentizar la creación de instantáneas.

Por estos motivos, un archivo debe excluirse de las instantáneas solo si es grande, experimenta un cambio significativo entre una instantánea y la siguiente, y no es necesario realizar una copia de seguridad.

Solo debe excluir los archivos que pertenecen a la aplicación.

Si la marca \_ VSS VOLSNAP \_ ATTR \_ NO AUTORECOVERY está establecida en el contexto de la instantánea, significa que la recuperación automática está deshabilitada y no se puede excluir ningún archivo de la \_ instantánea. Para obtener más información, vea la [**\_ enumeración ATRIBUTOS \_ DE INSTANTÁNEAS DE VOLUMEN \_ \_ DE VSS.**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>Uso del método AddExcludeFilesFromSnapshot

Un vss writer puede excluir archivos de una instantánea de la siguiente manera:

1.  Llame al [**método IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) para notificar los archivos que se excluirán.
2.  En el método [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) del escritor, elimine los archivos de la instantánea.

## <a name="using-the-filesnottosnapshot-registry-key"></a>Uso de la clave del Registro FilesNotToSnapshot

> [!Note]  
> La clave del registro **FilesNotToSnapshot** está pensada para que solo las aplicaciones la usen. Los usuarios que intenten usarla tendrán limitaciones como las siguientes:
>
> -   No puede eliminar archivos de una instantánea creada en Windows Server mediante la característica Versiones anteriores.
> -   No puede eliminar archivos de las instantáneas para carpetas compartidas.
> -   Puede eliminar archivos de una instantánea creada mediante la utilidad [DiskShadow,](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) pero no puede eliminar archivos de una instantánea creada mediante la utilidad [Vssadmin.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11))
> -   Los archivos se eliminan de una instantánea en función de la mejor opción. Como resultado, no se garantiza que se eliminen.

 

Una aplicación VSS puede eliminar archivos de una instantánea durante la creación de instantáneas mediante la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToSnapshot**

Esta clave del Registro tiene valores REG \_ MULTI SZ para cada aplicación \_ cuyos archivos se pueden excluir. Los archivos se especifican mediante rutas de acceso completas, que pueden contener el carácter \* comodín.

En todos los casos, la entrada se omite si no hay archivos que coincidan con la cadena de ruta de acceso.

Después de agregar un archivo al valor de clave del Registro adecuado, el escritor de optimización de instantáneas lo elimina de la instantánea durante la creación en función del mejor esfuerzo posible.

Si no se puede especificar una ruta de acceso completa, también se puede implicar una ruta de acceso mediante la variable $UserProfile$ o $AllVolumes$. Por ejemplo:

-   $UserProfile$ Directory \\ \\ Subdirectory \\ FileName.\*
-   $AllVolumes$ \\ TemporaryFiles \\ \* .\*

Para que la ruta de acceso sea recursiva, anexe "/s" al final. Por ejemplo:

-   $UserProfile$ \\ Directory \\ Subdirectory \\ FileName. \* /s
-   $AllVolumes$ \\ TemporaryFiles \\ \* . \* /s

La variable $UserProfile$ hace que la cadena de ruta de acceso se aplique a todos los perfiles de usuario del equipo. Los perfiles de usuario se enumeran examinando la siguiente clave del Registro:

**HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ ProfileList**

La variable $AllVolumes$ hace que la cadena de ruta de acceso se aplique a todas las instantáneas del equipo. Por ejemplo, suponga que la ruta de acceso es "$AllVolumes$ \\ TemporaryFiles \\ \* . \* /s", y el equipo tiene tres volúmenes: C:, D:, y E:. Si C: y E: contienen la ruta de acceso " TemporaryFiles " y el volumen D: contiene solo la ruta de acceso D: Datos , el árbol de directorio C: TemporaryFiles se elimina de las instantáneas de C:, y el árbol de \\ \\ \\ \\ \\ \\ directorioS: \\ TemporaryFiles se elimina de las instantáneas \\ de E:.

Los administradores pueden deshabilitar la expansión de la variable $UserProfile$ mediante la siguiente clave del Registro:

**HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Services \\ vss \\ Configuración**

En esta clave del Registro, especifique DisableUserProfileExpansion como nombre del valor, REG DWORD para el tipo de valor y un valor distinto de cero para los datos \_ de valor.

## <a name="about-the-filesnottobackup-registry-key"></a>Acerca de la clave del Registro FilesNotToBackup

La **clave del Registro FilesNotToBackup** se puede usar para especificar los nombres de los archivos y directorios que las aplicaciones de copia de seguridad no deben realizar copias de seguridad ni restaurar. Sin embargo, no excluye esos archivos de las instantáneas. Para obtener más información sobre esta clave del Registro, vea Claves y valores del Registro [para copias de seguridad y restauración.](../backup/registry-keys-for-backup-and-restore.md)

 

 
