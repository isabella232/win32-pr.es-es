---
description: Las instancias de la interfaz IVssBackupComponents mantienen el documento de componentes de copia de seguridad.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Contenido del documento de componentes de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c844f2e9e106817c8201822d000c2f6cb94c0fa272bb5b165d98e4cc48b1c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248345"
---
# <a name="backup-components-document-contents"></a>Contenido del documento de componentes de copia de seguridad

Las instancias de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) mantienen el documento de componentes de copia de seguridad. Esta interfaz también contiene numerosos métodos para controlar las operaciones de copia de seguridad, manipular instantáneas y consultar el estado del sistema. Sin embargo, no toda la información del documento es accesible directamente a través de esta interfaz.

El documento Componentes de copia de seguridad consta de varios conjuntos de datos:

-   Información sobre qué componentes se incluyeron explícitamente en una operación de copia de seguridad o restauración
-   Representación del componente almacenado y la información del sistema de escritura
-   Información de estado sobre la operación de copia de seguridad y recuperación

Aunque la información del componente está disponible tanto para el solicitante como para el escritor, solo el escritor tiene acceso a la información de estado.

## <a name="component-inclusion-information"></a>Información de inclusión de componentes

El documento Componentes de copia de seguridad contiene una lista de esos componentes incluidos explícitamente en la copia de seguridad y restauración por parte del solicitante. La lista contiene lo siguiente:

-   Componentes seleccionables [*incluidos explícitamente.*](vssgloss-s.md)

    La inclusión de estos archivos en las operaciones de copia de seguridad se indica mediante [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) y en las operaciones de restauración por [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   No se puede seleccionar para los subcomponentes de copia de seguridad sin un elemento seleccionable para el antecesor del componente de copia de seguridad.

    Todos estos componentes deben incluirse si algún componente del sistema de escritura se va a incluir en la operación. La inclusión de estos archivos en las operaciones de copia de seguridad se indica mediante [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) y en las operaciones de restauración por [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Componentes agregados implícitamente a la copia de [](vssgloss-s.md) seguridad [*(subcomponentes*](vssgloss-s.md)) que se pueden seleccionar para la restauración y se agregan explícitamente a la restauración.

    Estos componentes pueden ser seleccionables o no seleccionables, pero tienen un antecesor seleccionable que se usó para seleccionarlos implícitamente para la copia de seguridad. [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)los agrega al documento componentes de copia de seguridad.

Las identidades de los componentes incluidos implícitamente en la restauración no se almacenan en el documento Componentes de copia de seguridad.

VSS tiene acceso a información sobre la inclusión de componentes: los escritores sin componentes incluidos explícitamente en una restauración o copia de seguridad no reciben ningún evento VSS después de la generación de los eventos [*PrepareForBackup*](vssgloss-p.md) o [*PreRestore.*](vssgloss-p.md)

Los escritores no pueden consultar directamente esta información. Esto no es una limitación significativa porque, por diseño, los escritores de VSS individuales no deben requerir información detallada sobre el estado de otros escritores en el sistema y, como se indicó anteriormente, aquellos sin componentes incluidos no tendrán que participar en la operación de VSS.

Un solicitante puede determinar qué componentes se han incluido explícitamente en una operación.

El [**método IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) devuelve el número de escritores con información de componentes almacenada en el documento componentes de copia de seguridad (y no el número de componentes del documento).

El solicitante indexa a través de la información de escritor almacenada mediante [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), que devuelve instancias de la [**interfaz IVssWriterComponentsExt.**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) La **interfaz IVssWriterComponentsExt** permite al [](vssgloss-w.md) solicitante obtener [](vssgloss-w.md) la clase de escritor y la instancia de escritor de los escritores participantes, así como obtener acceso a información sobre los de sus componentes almacenados en el documento Componentes de copia de seguridad.

## <a name="information-on-included-components"></a>Información sobre los componentes incluidos

Representación del documento componentes de copia de seguridad de los datos del componente (que no incluye información de especificación de ruta de acceso y archivo), a la que se accede a través de instancias de la [**interfaz IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Los solicitantes y escritores obtienen acceso a las instancias de la [**interfaz IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) de maneras diferentes.

Un solicitante examina los datos de componentes en un sistema de escritura por sistema de escritura mediante instancias de la [**interfaz IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) devueltas por [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Además de la información de identificación del escritor, la interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) proporciona una matriz de instancias de la interfaz [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) una para cada uno de los escritores seleccionados incluidos componentes.

Como se indicó en Ciclo de vida de documentos de componentes de copia de seguridad [,](backup-components-document-life-cycle.md)los escritores pueden obtener acceso a la misma información a través de la interfaz [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) al controlar el evento PrepareForBackup, PrepareForSnapshot, PostSnapshot, BackupComplete, PreRestore o PostRestore.

[**IVssComponent permite**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que tanto el escritor como los solicitantes obtengan la siguiente información:

-   Nombre, tipo y ruta de acceso lógica de un componente [*(*](vssgloss-l.md) [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**GetComponentType**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Cómo se debe restaurar un componente según lo indicado por el destino [*de restauración*](vssgloss-r.md) ([**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Si se usó una ubicación alternativa para restaurar un archivo ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Nueva información de destino, si existe ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Mensajes de error previos y posteriores a la restauración ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Si se [*ha seleccionado un componente seleccionable para copia*](vssgloss-s.md) de seguridad que define un conjunto de componentes para la restauración ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Si una copia de seguridad o una restauración se [**realizaron correctamente ( GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Cualquier opción de copia de seguridad o restauración específica del escritor que [**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) o [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions))
-   Cualquier metadato de copia de seguridad o restauración específico del escritor ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Información de marca de tiempo ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Información sobre los subcomponentes de copia de seguridad incluidos explícitamente en una restauración ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

A diferencia de los solicitantes, los escritores pueden cambiar cierta información en el documento Componentes de copia de seguridad a través de [**la interfaz IVssComponent:**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

-   Cómo se debe restaurar un componente según lo indicado por el destino de restauración ([**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Metadatos de copia de seguridad y restauración específicos del escritor ([**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Información de marca de tiempo ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Mensajes de error previos y posteriores a la restauración ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Información de estado del solicitante

Los solicitantes insertan información sobre el estado de una operación de copia de seguridad o restauración en el documento Componentes de copia de seguridad mediante la [**interfaz IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) Las aplicaciones de escritor pueden consultar esta información a través de la [**clase CVssWriter.**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter)

La información de estado almacenada en el documento Componentes de copia de seguridad incluye lo siguiente:

Información general sobre la copia de seguridad

-   Tipo de copia de seguridad general (incremental, diferencial o completa)<dl> <dt>

Establecido por solicitantes mediante [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperada por escritores mediante [ **CVssWriter::GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Establecido por solicitantes mediante [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperada por escritores mediante [ **CVssWriter::AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Establecido por solicitantes mediante [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperada por escritores mediante [ **CVssWriter::IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Establecido por solicitantes mediante [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por escritores mediante [ **CVssWriter::IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Información general sobre la restauración

-   El tipo de restauración general (si la restauración se hace mediante copia o importación)<dl> <dt>

Establecido por solicitantes mediante [ **IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Recuperado por escritores mediante [ **CVssWriter::GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Información sobre los archivos de soporte técnico

-   Ubicación de los archivos de intervalos usados por un componente específico en operaciones de archivos parciales<dl> <dt>

Establecido por solicitantes mediante [ **IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Recuperada por escritores (o solicitantes) mediante [ **IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Estado de la información

-   Indicar si se ha realizado correctamente una copia de seguridad de uno de los componentes de un escritor determinado<dl> <dt>

Establecido por solicitantes mediante [ **IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Recuperada por escritores y solicitantes mediante [ **IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Establecido por solicitantes mediante [ **IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Recuperado por escritores y solicitantes mediante [ **IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Writer-Settable información

-   Especificación de copia de seguridad adicional para uno de los componentes de un escritor determinado<dl> <dt>

Establecido por escritores mediante [ **IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Recuperada por escritores y solicitantes mediante [ **IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Establecido por escritores mediante [ **IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Recuperada por escritores y solicitantes mediante [ **IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Establecido por escritores mediante [ **IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Recuperada por escritores y solicitantes mediante [ **IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a><dl> <dt>

Almacenado y establecido por los solicitantes de un componente específico mediante [ **IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Recuperada por escritores y solicitantes mediante [ **IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Establecido por escritores mediante [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) o [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Recuperada por escritores y solicitantes mediante [**IVssComponent::GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) o [**IVssComponent::GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)
</dt> </dl>

 

 
