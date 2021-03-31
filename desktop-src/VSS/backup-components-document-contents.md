---
description: El documento componentes de copia de seguridad se mantiene mediante instancias de la interfaz IVssBackupComponents.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Contenido del documento componentes de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e12c88ebffa0037702e1f30dd818d4fd23fe4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913389"
---
# <a name="backup-components-document-contents"></a>Contenido del documento componentes de copia de seguridad

El documento componentes de copia de seguridad se mantiene mediante instancias de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Esta interfaz también contiene numerosos métodos para controlar las operaciones de copia de seguridad, manipular instantáneas y consultar el estado del sistema. Sin embargo, no toda la información del documento es directamente accesible a través de esta interfaz.

El documento componentes de copia de seguridad consta de varios conjuntos de datos:

-   Información acerca de los componentes que se incluyeron explícitamente en una operación de copia de seguridad o restauración
-   Representación de la información del componente y del escritor almacenados
-   Información de estado sobre la operación de copia de seguridad o recuperación

Mientras que la información del componente está disponible tanto para el solicitante como para el escritor, solo el escritor tiene acceso a la información de estado.

## <a name="component-inclusion-information"></a>Información de inclusión de componentes

El documento componentes de copia de seguridad contiene una lista de los componentes incluidos explícitamente en la copia de seguridad y la restauración del solicitante. La lista contiene lo siguiente:

-   [*Componentes seleccionables*](vssgloss-s.md)incluidos explícitamente.

    La inclusión de estos archivos en las operaciones de copia de seguridad se indica mediante [**ivssbackupcomponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) y en las operaciones de restauración de [**Ivssbackupcomponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   No seleccionable para subcomponentes de copia de seguridad sin un elemento seleccionable para el antecesor del componente de copia de seguridad.

    Todos estos componentes deben incluirse si los componentes del escritor se van a incluir en la operación. La inclusión de estos archivos en las operaciones de copia de seguridad se indica mediante [**ivssbackupcomponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) y en las operaciones de restauración de [**Ivssbackupcomponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Componentes agregados implícitamente a la copia de seguridad ([*subcomponentes*](vssgloss-s.md)) que se pueden [*seleccionar para la restauración*](vssgloss-s.md) y se agregan explícitamente a la restauración.

    Estos componentes pueden ser seleccionables o no seleccionables, pero tienen un antecesor seleccionable que se usó para seleccionarlos de forma implícita para la copia de seguridad. Se agregan al documento componentes de copia de seguridad mediante [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Las identidades de los componentes que se incluyen de forma implícita en la restauración no se almacenan en el documento componentes de copia de seguridad.

VSS tiene acceso a información sobre la inclusión de componentes: los escritores sin componentes incluidos explícitamente en una restauración o copia de seguridad no reciben ningún evento VSS después de la generación de los eventos [*PrepareForBackup*](vssgloss-p.md) o [*prerestore*](vssgloss-p.md) .

Los escritores no pueden consultar directamente esta información. Esta no es una limitación significativa porque, por diseño, los escritores de VSS individuales no deben requerir información detallada sobre el estado de otros escritores en el sistema y, como se indicó anteriormente, los que no tienen componentes incluidos no tendrán que participar en la operación de VSS.

Un solicitante puede determinar qué componentes se han incluido explícitamente en una operación.

El método [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) devuelve el número de escritores con información de componente almacenada en el documento componentes de copia de seguridad (y no el número de componentes del documento).

El solicitante indexa la información del escritor almacenado mediante [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), que devuelve instancias de la interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) . La interfaz **IVssWriterComponentsExt** permite al solicitante obtener la clase de [*escritor*](vssgloss-w.md) y la [*instancia del escritor*](vssgloss-w.md) de escritores participantes, así como obtener acceso a información sobre los componentes almacenados en el documento componentes de copia de seguridad.

## <a name="information-on-included-components"></a>Información sobre los componentes incluidos

La representación del documento de componentes de copia de seguridad de los datos del componente (que no incluye información de ruta de acceso y de especificación de archivo), a la que se accede a través de instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Los solicitantes y escritores obtienen acceso a las instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) de maneras diferentes.

Un solicitante examina los datos de componentes de un escritor mediante el uso de instancias de la interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) devuelta por [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Además de la información de identificación del escritor, la interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) proporciona una matriz de instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , una para cada uno de los componentes de escritores seleccionados incluidos.

Como se indicó en [ciclo de vida de documentos de componentes de copia de seguridad](backup-components-document-life-cycle.md), los escritores pueden obtener acceso a la misma información a través de la interfaz [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) al controlar el evento PrepareForBackup, PrepareForSnapshot, postsnapshot, BackupComplete, prerestore o postrestore.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permite que el escritor y los solicitantes obtengan la siguiente información:

-   El nombre de un componente, el tipo y la [*ruta de acceso lógica*](vssgloss-l.md) ([**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**GetComponentType**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Cómo se debe restaurar un componente según lo indicado por el [*destino de restauración*](vssgloss-r.md) ([**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Si se usó una ubicación alternativa en la restauración de un archivo ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Nueva información de destino, si existe ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Mensajes de error anteriores y posteriores a la restauración ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Si se ha seleccionado una [*selección para el componente de copia de seguridad*](vssgloss-s.md) que define un conjunto de componentes para la restauración ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Si una copia de seguridad o una restauración se realizó correctamente ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Todas las opciones de copia de seguridad o restauración específicas del escritor que se puedan haber establecido mediante [**ivssbackupcomponents:: SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) o [**Ivssbackupcomponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions))
-   Cualquier metadatos de copia de seguridad o restauración de metadatos específicos del escritor ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Información de marca de tiempo ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Información sobre los subcomponentes de copia de seguridad incluidos explícitamente en una restauración ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

A diferencia de los solicitantes, los escritores pueden cambiar cierta información en el documento componentes de copia de seguridad a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) :

-   Cómo se debe restaurar un componente según lo indicado por el destino de restauración ([**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Metadatos de copia de seguridad y restauración específicos del escritor ([**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Información de marca de tiempo ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Mensajes de error anteriores y posteriores a la restauración ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Información de estado del solicitante

Los solicitantes insertan información sobre el estado de una operación de copia de seguridad o restauración en el documento componentes de copia de seguridad mediante la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Las aplicaciones de escritura pueden consultar esta información a través de la clase [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) .

La información de estado almacenada en el documento componentes de copia de seguridad incluye lo siguiente:

Información general sobre la copia de seguridad

-   El tipo de copia de seguridad general (incremental, diferencial o completo)<dl> <dt>

Establecido por los solicitantes mediante [ **IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por escritores mediante [ **CVssWriter:: GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Establecido por los solicitantes mediante [ **IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por escritores mediante [ **CVssWriter:: AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Establecido por los solicitantes mediante [ **IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por escritores mediante [ **CVssWriter:: IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Establecido por los solicitantes mediante [ **IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por escritores mediante [ **CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Información general acerca de la restauración

-   El tipo de restauración general (ya sea por copia o importación)<dl> <dt>

Establecido por los solicitantes mediante [ **IVssBackupComponents:: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Recuperado por escritores mediante [ **CVssWriter:: GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Información sobre los archivos auxiliares

-   Ubicación de los archivos de intervalos utilizados por un componente específico en operaciones de archivos parciales.<dl> <dt>

Establecido por los solicitantes mediante [ **IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Recuperado por escritores (o solicitantes) mediante [ **IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Estado de la información

-   Indicar si se realizó correctamente una copia de seguridad de uno de los componentes de un escritor dado<dl> <dt>

Establecido por los solicitantes mediante [ **IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Recuperado por escritores y solicitantes mediante [ **IVssComponent:: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Establecido por los solicitantes mediante [ **IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Recuperado por escritores y solicitante mediante [ **IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Información de Writer-Settable

-   Especificación adicional de copia de seguridad para uno de los componentes de un escritor determinado<dl> <dt>

Establecido por escritores mediante [ **IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Recuperado por escritores y solicitantes mediante [ **IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Establecido por escritores mediante [ **IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Recuperado por escritores y solicitantes mediante [ **IVssComponent:: GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Establecido por escritores mediante [ **IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Recuperado por escritores y solicitantes mediante [ **IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a><dl> <dt>

Almacenada y establecida por solicitantes para un componente específico mediante [ **IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Recuperado por escritores y solicitantes mediante [ **IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Establecido por escritores mediante [**IVssComponent:: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) o [**IVssComponent:: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Recuperado por escritores y solicitantes mediante [**IVssComponent:: GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) o [**IVssComponent:: GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)
</dt> </dl>

 

 
