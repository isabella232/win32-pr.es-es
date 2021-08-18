---
description: Un conjunto de restauración es una lista de todos los archivos que se van a restaurar y las ubicaciones en las que se restaurarán.
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: Generar un conjunto de restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85dd620869614420e5073f47ef4ac8732b1e2c0d0d218ea0e94ae690cb9f773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958455"
---
# <a name="generating-a-restore-set"></a>Generar un conjunto de restauración

Un conjunto de restauración es una lista de todos los archivos que se van a restaurar y las ubicaciones en las que se restaurarán.

Al igual que al generar la lista de archivos de copia de seguridad (consulte Generación [](vssgloss-w.md) de un conjunto de copia de seguridad [),](generating-a-backup-set.md)un algoritmo para determinar qué archivos restaurar y dónde restaurarlos debe continuar con la instancia de escritura por instancia de escritor y en función de componente por componente para cada instancia de escritor.

Es necesario asociar cada archivo del medio de copia de seguridad con el componente que lo administra. También es necesario obtener el método de restauración del [](vssgloss-r.md) componente de [*administración,*](vssgloss-r.md)la información de destino de restauración del archivo y sus asignaciones de ubicación [*alternativas*](vssgloss-a.md) (si las hubiera).

Algunos archivos también pueden requerir operaciones [*de archivos parciales*](vssgloss-p.md) o [*destinos dirigidos para*](vssgloss-d.md) la restauración.

Mediante el examen [](vssgloss-s.md) de la capacidad de selección de los componentes para las rutas de acceso lógicas y de copia de seguridad [*(consulte*](vssgloss-l.md) Trabajar con la [selectibilidad](working-with-selectability-and-logical-paths.md)y las rutas de acceso lógicas), un solicitante puede determinar la estructura de componentes de la operación de copia de seguridad que se va a restaurar.

Con la estructura de componentes de la copia de [](vssgloss-f.md) seguridad establecida, el solicitante puede obtener la información del conjunto de archivos de cada componente (especificación de archivo, ruta de acceso y marca de recursividad). A continuación, un solicitante puede generar un conjunto de restauración.

Los archivos que requieren [](vssgloss-d.md) archivos parciales [*o*](vssgloss-p.md)destinos dirigidos proporcionan sus propias instrucciones de restauración detalladas (consulte Ubicaciones de copia de seguridad y restauración no predeterminadas), [](non-default-backup-and-restore-locations.md)que luego se pueden agregar al conjunto de restauración.

Un mecanismo típico para generar un conjunto de restauración [](vssgloss-d.md) para archivos que no están implicados en operaciones de archivos parciales o destinos dirigidos puede continuar haciendo lo siguiente:

1.  Obtenga una lista de archivos en el medio de copia de seguridad, incluidas sus rutas de acceso originales.

2.  Identifique la [*clase y el*](vssgloss-w.md) componente de escritor para cada archivo en el medio de copia de seguridad haciendo lo siguiente:

    -   Para cada sistema de escritura, obtenga información de componentes ([**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) mediante una llamada [**a IVssExgvWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) en todos sus componentes.
    -   Para cada componente, obtenga información del descriptor de archivo [**(IVssWMFiledesc)**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)para cada conjunto de archivos que contiene el componente (en función de los tipos de datos que contiene el componente llamando a [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent::GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)y [**IVssWMComponent::GetDatabaseLogFile).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)
    -   Compare la información de nombre y ruta de acceso del archivo con la devuelta por la información de ruta de acceso contenida en el descriptor de archivo para cada conjunto de archivos de un componente (devuelto por [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)y [**IVssWMFiledesc::GetRecursive)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)con la información de ruta de acceso de los archivos almacenados para determinar si el archivo forma parte del componente.
        > [!Note]  
        > Debe omitir cualquier información de ubicación alternativa en el descriptor de archivo recuperado de un componente encontrado en un documento de metadatos del escritor almacenado (es decir, [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) no devuelve **NULL).** Esta ubicación alternativa es la ruta [*de acceso alternativa*](vssgloss-a.md), que solo se usa durante la copia de seguridad.

         

3.  Obtenga información de asignación alternativa para cada archivo en el medio de copia de seguridad:

    -   Las asignaciones de archivos alternativas se almacenan en el sistema de escritura, no en el nivel de componente, y se obtienen del objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) devuelto por [**IVssExgvWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).
    -   Puede determinar si un archivo determinado tiene una asignación de ubicación alternativa comprobando la ruta de acceso y el nombre del archivo con la ruta de acceso y la especificación de archivo contenidas en la asignación de ubicación alternativa devuelta por [**IVssExwriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), a través de [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e [**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive). (Si se usó una ruta de acceso alternativa durante la copia de seguridad, esa información debe omitirse durante esta comprobación al procesar una restauración).
    -   Si un archivo y un descriptor de archivo de asignaciones de ubicación alternativa coinciden, se usa el método [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) del objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) devuelto por [**IVssExineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) para buscar la ubicación alternativa en la que puede restaurar el archivo.
    -   La asignación de ubicación alternativa obtenida de esta manera no coincidirá necesariamente con la devuelta del documento componentes de copia de seguridad por [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). El [**valor IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) no está en pantalla solo si se usa la asignación de ubicación alternativa para un archivo.

4.  Con esta información de archivo y componente, se puede consultar el documento componentes de copia de seguridad para obtener información sobre los destinos de restauración, las opciones y las nuevas ubicaciones de restauración de cada archivo. Esta información se puede combinar con la lista de archivos, componentes y ubicaciones alternativas.

5.  Los archivos no protegidos por escritores se pueden seleccionar de forma coherente con las operaciones de restauración tradicionales.

En este momento, un solicitante debe tener una lista de todos los archivos que necesita restaurar, junto con instrucciones sobre cómo restaurarlos, y puede empezar a restaurar archivos en función de:

-   Si las asignaciones de ubicación alternativas o la ubicación del archivo original se van a usar como destino de la restauración dependerán de la presencia o ausencia de un archivo en esa ubicación de destino y de la configuración de componentes de [**VSS \_ RESTORE \_ TARGET**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) y [**VSS \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) (vea Ubicaciones de copia de seguridad y restauración no [predeterminadas).](non-default-backup-and-restore-locations.md)
-   Si un intento de restauración se realiza correctamente dependerá de problemas como los permisos de acceso del destino, si los archivos de destino están bloqueados y otros problemas convencionales relacionados con la restauración de archivos.
-   La restauración correcta o con errores de un componente determinado para una instancia de escritor determinada debe conservarse en el documento componentes de copia de seguridad mediante una llamada a [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). Esto hará que los escritores puedan acceder a la información cuando procese el evento PostRestore.
-   Si se restaura un archivo en una asignación de ubicación alternativa, el solicitante debe llamar a [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping). Esto permitirá a los escritores determinar si sus archivos se han restaurado en ubicaciones alternativas a través de [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Los solicitantes pueden encontrar conveniente restaurar archivos en ubicaciones completamente nuevas. Esto es aceptable, pero el solicitante debe indicarlo al escritor mediante el método [**IVssBackupComponents::AddNewTarget.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

 

 



