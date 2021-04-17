---
description: Un conjunto de restauración es una lista de todos los archivos que se van a restaurar y las ubicaciones en las que se restaurarán.
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: Generar un conjunto de restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3447ba6d258a5f22fff958761abc7ac0e4f27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697019"
---
# <a name="generating-a-restore-set"></a>Generar un conjunto de restauración

Un conjunto de restauración es una lista de todos los archivos que se van a restaurar y las ubicaciones en las que se restaurarán.

Al igual que al generar la lista de archivos de copia de seguridad (vea [generar un conjunto de copia de seguridad](generating-a-backup-set.md)), un algoritmo para determinar qué archivos se van a restaurar y dónde restaurarlos debe continuar la [*instancia*](vssgloss-w.md) del escritor por instancia de escritor y en función componente por componente para cada instancia del escritor.

Es necesario asociar cada archivo en el medio de copia de seguridad con el componente que lo administra. También es necesario obtener el [*método restore*](vssgloss-r.md)del componente de administración, así como la información de [*destino de restauración*](vssgloss-r.md) del archivo y sus asignaciones de [*Ubicación alternativas*](vssgloss-a.md) (si existen).

Algunos archivos también pueden requerir operaciones de [*archivos parciales*](vssgloss-p.md) o [*destinos dirigidos*](vssgloss-d.md) para la restauración.

Mediante el examen de la capacidad de selección de los componentes para las rutas de acceso [*lógicas*](vssgloss-l.md) y [*de copia de seguridad*](vssgloss-s.md) (vea [trabajar con las rutas de acceso lógicas y de selección](working-with-selectability-and-logical-paths.md)), un solicitante puede determinar la estructura de componentes de la operación de copia de seguridad que se va a restaurar.

Con la estructura de componentes de la copia de seguridad establecida, el solicitante puede obtener la información del [*conjunto de archivos*](vssgloss-f.md) de cada componente (especificación de archivo, ruta de acceso y marca de recursividad). Después, un solicitante puede generar un conjunto de restauración.

Los archivos que requieren [*archivos parciales*](vssgloss-p.md)o [*destinos dirigidos*](vssgloss-d.md) proporcionan sus propias instrucciones de restauración detalladas (vea [ubicaciones de copia de seguridad y restauración no predeterminadas](non-default-backup-and-restore-locations.md)), que se pueden agregar al conjunto de restauración.

Un mecanismo típico para generar un conjunto de restauración para los archivos que no están relacionados con las operaciones de archivos parciales o los [*destinos dirigidos*](vssgloss-d.md) puede continuar haciendo lo siguiente:

1.  Obtenga una lista de archivos en el medio de copia de seguridad, incluidas sus rutas de acceso originales.

2.  Para identificar la clase y el componente del [*escritor*](vssgloss-w.md) de cada archivo en el medio de copia de seguridad, haga lo siguiente:

    -   Para cada escritor, obtenga información de componentes ([**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) llamando a [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) en todos sus componentes.
    -   Para cada componente, obtenga información del descriptor de archivo ([**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) para cada conjunto de archivos que contiene el componente (en función de los tipos de datos que contiene el componente mediante una llamada a [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)y [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).
    -   Compare la información de nombre y ruta de acceso del archivo con la que devuelve la información de ruta de acceso contenida en el descriptor de archivo para cada conjunto de archivos de un componente (devuelto por [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)y [**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)) en la información de ruta de acceso de los archivos almacenados para determinar si el archivo forma parte del componente.
        > [!Note]  
        > Debe omitir cualquier información de ubicación alternativa en el descriptor de archivo recuperado de un componente que se encuentra en un documento de metadatos de escritor almacenado (es decir, [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) no devuelve **null**). Esta ubicación alternativa es la [*ruta de acceso alternativa*](vssgloss-a.md), que solo se usa durante la copia de seguridad.

         

3.  Obtenga información de asignación alternativa para cada archivo en el medio de copia de seguridad:

    -   Las asignaciones de archivos alternativas se almacenan en el escritor, no en el nivel de componente, y se obtienen del objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) devuelto por [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).
    -   Puede determinar si un archivo determinado tiene una asignación de ubicación alternativa comprobando la ruta de acceso y el nombre del archivo con la ruta de acceso y la especificación del archivo contenidos en la asignación de ubicación alternativa devuelta por [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), a través de [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)y [**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive). (Si se usó una ruta de acceso alternativa durante la copia de seguridad, esta información debe omitirse durante esta comprobación en el procesamiento de una restauración).
    -   Si un archivo y una ubicación alternativa asignan los descriptores de archivo, use el método [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) del objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) devuelto por [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) para buscar la ubicación alternativa en la que puede restaurar el archivo.
    -   La asignación de ubicación alternativa obtenida de esta manera no coincidirá necesariamente con la que devolvió el documento componentes de copia de seguridad de [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). El valor [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) no está en blanco solo si se usa la asignación de ubicación alternativa para un archivo.

4.  Con esta información de archivos y componentes, se puede consultar el documento componentes de copia de seguridad para obtener información acerca de destinos de restauración, opciones y nuevas ubicaciones de restauración para cada archivo. Esta información puede combinarse con la lista de archivos, componentes y ubicaciones alternativas.

5.  Los archivos que no están protegidos por escritores se pueden seleccionar de una manera coherente con las operaciones de restauración tradicionales.

En este momento, un solicitante debe tener una lista de todos los archivos que necesita restaurar, junto con instrucciones sobre cómo restaurarlos, y puede empezar a restaurar archivos en función de:

-   Si las asignaciones de ubicación alternativas o la ubicación del archivo original se va a usar como destino para la restauración dependerá de la presencia o ausencia de un archivo en esa ubicación de destino y de la configuración de componentes de [**VSS \_ restore \_ target**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) y [**VSS \_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) (vea [ubicaciones de copia de seguridad y restauración no predeterminadas](non-default-backup-and-restore-locations.md)).
-   Si un intento de restauración se realiza correctamente dependerá de problemas como los permisos de acceso del destino, si los archivos de destino están bloqueados y otros problemas convencionales implicados en la restauración de archivos.
-   El éxito o el error de la restauración de un componente determinado para una instancia del escritor determinada debe conservarse en el documento componentes de copia de seguridad llamando a [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). Esto hará que la información sea accesible para los escritores Cuando procese el evento postrestore.
-   Si un archivo se restaura en una asignación de ubicación alternativa, el solicitante debe llamar a [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping). Esto permitirá que los escritores determinen si sus archivos se han restaurado en ubicaciones alternativas a través de [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Los solicitantes pueden ser deseables para restaurar archivos en ubicaciones completamente nuevas. Esto es aceptable, pero el solicitante debe indicar Esto al escritor mediante el método [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) .

 

 



