---
description: Un solicitante debe tener un conocimiento bien definido sobre el estado del escritor que participa con él durante la creación de la instantánea y durante las operaciones de copia de seguridad y restauración.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Determinar el estado del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279921"
---
# <a name="determining-writer-status"></a>Determinar el estado del escritor

Un solicitante debe tener un conocimiento bien definido sobre el estado del escritor que participa con él durante la creación de la instantánea y durante las operaciones de copia de seguridad y restauración. Para ello, se recomienda:

-   Los solicitantes usan [**ivssbackupcomponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)y [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).
-   Como se describe en [información general sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md) y la [Introducción al procesamiento de una restauración en VSS](overview-of-processing-a-restore-under-vss.md), estos métodos son muy útiles cuando se llama en una secuencia de copia de seguridad o restauración bien definida. Normalmente, esto significa que los escritores deben consultarse después de que un solicitante haya completado una de sus tareas y haya generado un evento de VSS.

    Al procesar una copia de seguridad, un solicitante debe consultar a un escritor después de la finalización de los métodos siguientes. Los solicitantes deben llamar a [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) después de llamar a [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) para que la sesión del escritor se establezca en un estado completado.

    > [!Note]  
    > Esto solo es necesario en Windows Server 2008 con Service Pack 2 (SP2) y versiones anteriores.

     

    <dl> <dt>

[**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

Durante las operaciones de restauración, un solicitante debe consultar un escritor después de completar estos métodos:
<dl> <dt>

[**IVssBackupComponents::P volver a restaurar**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   Las llamadas a [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) que no forman parte de una secuencia de copia de seguridad o restauración bien definida no proporcionan una imagen confiable del estado del escritor, ya que podrían reflejar condiciones que no indican un error en la operación actual, como:
    -   Un error en la creación de una instantánea anterior
    -   Error en una operación de copia de seguridad o restauración temprana
    -   Un escritor que no responde actualmente está procesando un evento

Por lo tanto, los desarrolladores no deben confiar en el estado del escritor devuelto por los procesos que otros, o bien, intentar supervisar el progreso de una instancia de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) con otro (posiblemente en un subproceso independiente).

Tenga en cuenta que, en el caso de las operaciones de copia de seguridad, donde es necesario examinar los documentos de metadatos del escritor de escritores, no es necesario realizar una llamada del solicitante a [**ivssbackupcomponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) y [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) después de la generación y el control del evento de [*identificación*](vssgloss-i.md) provocado por [**ivssbackupcomponents:: GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

[**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) solo informa del estado de los escritores cuyos metadatos se proporcionaron a VSS por los escritores ' [*identifique*](vssgloss-i.md) los controladores de eventos, [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (y devueltos al solicitante mediante [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) y [**ivssbackupcomponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).

Si se produce un error en la implementación de [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) , los metadatos del escritor no formarán parte de la lista de documentos de metadatos del escritor proporcionados a VSS, no habrá información de estado disponible y la llamada sería redundante.

En el caso de las operaciones de restauración, en las que el solicitante no necesita examinar los documentos de metadatos del escritor que ejecutan escritores, llamar a [**ivssbackupcomponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) y [**Ivssbackupcomponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) puede ser una forma más eficaz de determinar qué escritores se están ejecutando.

 

 



