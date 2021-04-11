---
description: En Windows Vista y Windows Server 2008 y versiones posteriores, el desarrollador de una VSS Writer o aplicación puede optar por excluir determinados archivos de las instantáneas.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Excluir archivos de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279127"
---
# <a name="excluding-files-from-shadow-copies"></a>Excluir archivos de instantáneas

En Windows Vista y Windows Server 2008 y versiones posteriores, el desarrollador de una VSS Writer o aplicación puede optar por excluir determinados archivos de las instantáneas.

El área de almacenamiento de instantáneas y el impacto en el rendimiento (también denominado "área de diferenciación") de un archivo en una instantánea se relacionan directamente con la cantidad de cambios en el contenido del archivo una vez creada la instantánea. Además, la exclusión de archivos de instantáneas puede ralentizar la creación de la instantánea.

Por estos motivos, se debe excluir un archivo de las instantáneas solo si es grande, se producirá un cambio significativo entre una instantánea y la siguiente, y no es necesario hacer una copia de seguridad de ella.

Solo debe excluir los archivos que pertenezcan a la aplicación.

Si la \_ marca VSS VOLSNAP \_ ATTR \_ no \_ se ha establecido el marcador de Autorrecuperación en el contexto de instantáneas, significa que la recuperación automática está deshabilitada y que no se puede excluir ningún archivo de la instantánea. Para obtener más información, consulte la enumeración de [**\_ \_ \_ \_ atributos de instantáneas de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) .

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>Usar el método AddExcludeFilesFromSnapshot

Un VSS Writer puede excluir archivos de una instantánea de la siguiente manera:

1.  Llame al método [**IVssCreateWriterMetadataEx:: AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) para notificar los archivos que se van a excluir.
2.  En el método [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) del escritor, elimine los archivos de la instantánea.

## <a name="using-the-filesnottosnapshot-registry-key"></a>Uso de la clave del registro FilesNotToSnapshot

> [!Note]  
> La clave del registro **FilesNotToSnapshot** está pensada para que solo las aplicaciones la usen. Los usuarios que intenten usarla tendrán limitaciones como las siguientes:
>
> -   No puede eliminar archivos de una instantánea creada en Windows Server mediante la característica Versiones anteriores.
> -   No puede eliminar archivos de las instantáneas para carpetas compartidas.
> -   Puede eliminar archivos de una instantánea que se haya creado con la utilidad [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) , pero no puede eliminar archivos de una instantánea creada con la utilidad [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .
> -   Los archivos se eliminan de una instantánea en función de la mejor opción. Como resultado, no se garantiza que se eliminen.

 

Una aplicación VSS puede eliminar archivos de una instantánea durante la creación de instantáneas mediante la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ BackupRestore \\ FilesNotToSnapshot**

Esta clave del registro tiene \_ \_ valores de reg multi SZ para cada aplicación cuyos archivos se pueden excluir. Los archivos se especifican mediante rutas de acceso completas, que pueden contener el \* carácter comodín.

En todos los casos, la entrada se omite si no hay archivos que coincidan con la cadena de ruta de acceso.

Después de agregar un archivo al valor de clave del registro adecuado, se elimina de la instantánea durante la creación del escritor de optimización de instantáneas de la mejor manera posible.

Si no se puede especificar una ruta de acceso completa, una ruta de acceso también puede estar implícita mediante la $UserProfile $ o la variable $AllVolumes $. Por ejemplo:

-   $UserProfile \\ nombre de \\ archivo del subdirectorio $ Directory \\ .\*
-   $AllVolumes $ \\ TemporaryFiles \\ \* .\*

Para que la ruta de acceso sea recursiva, anexe "/s" al final. Por ejemplo:

-   $UserProfile $ \\ Directory \\ subdirectorio \\ nombreDeArchivo. \* /s
-   $AllVolumes $ \\ TemporaryFiles \\ \* . \* /s

La variable $UserProfile $ hace que la cadena de ruta de acceso se aplique a todos los perfiles de usuario del equipo. Los perfiles de usuario se enumeran examinando la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ProfileList**

La variable $AllVolumes $ hace que la cadena de ruta de acceso se aplique a todas las instantáneas del equipo. Por ejemplo, supongamos que la ruta de acceso es "$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s ", y el equipo tiene tres volúmenes: C:, D: y E:. Si C: y E: contienen la ruta de acceso " \\ TemporaryFiles \\ " y el volumen d: contiene solo la ruta de acceso d: \\ Data \\ , el árbol de directorio c: \\ TemporaryFiles \\ se elimina de las instantáneas de C: y el árbol de directorios E: \\ TemporaryFiles \\ se elimina de las instantáneas de E:.

Los administradores pueden deshabilitar la expansión de la variable $UserProfile $ mediante la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ configuración de VSS \\**

En esta clave del registro, especifique DisableUserProfileExpansion para el nombre del valor, REG \_ DWORD para el tipo de valor y un valor distinto de cero para los datos del valor.

## <a name="about-the-filesnottobackup-registry-key"></a>Acerca de la clave del registro FilesNotToBackup

La clave del registro **FilesNotToBackup** se puede usar para especificar los nombres de los archivos y directorios en los que las aplicaciones de copia de seguridad no deben realizar copias de seguridad ni restaurar. Sin embargo, no excluye esos archivos de las instantáneas. Para obtener más información acerca de esta clave del registro, consulte [claves y valores del registro para copias de seguridad y restauración](../backup/registry-keys-for-backup-and-restore.md).

 

 
