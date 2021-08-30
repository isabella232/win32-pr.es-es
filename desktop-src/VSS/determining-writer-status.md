---
description: Un solicitante debe tener un conocimiento bien definido sobre el estado del escritor que participa con él durante la creación de instantáneas y durante las operaciones de copia de seguridad y restauración.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Determinar el estado del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16c22364ed0f8eea6f73280e33083da3dcb06205d9a36a348644aa18d159f3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032755"
---
# <a name="determining-writer-status"></a>Determinar el estado del escritor

Un solicitante debe tener un conocimiento bien definido sobre el estado del escritor que participa con él durante la creación de instantáneas y durante las operaciones de copia de seguridad y restauración. Para ello, se recomienda:

-   Los solicitantes usan [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).
-   Como se describe en Información general sobre el procesamiento de una copia de seguridad en [VSS](overview-of-processing-a-backup-under-vss.md) e Información general sobre el procesamiento de una restauración en [VSS,](overview-of-processing-a-restore-under-vss.md)estos métodos son más útiles cuando se llama en una secuencia de copia de seguridad o restauración bien definida. Normalmente, esto significa que se deben consultar los escritores después de que un solicitante haya completado una de sus tareas y generado un evento de VSS.

    Al procesar una copia de seguridad, un solicitante debe consultar a un escritor después de la finalización de los métodos siguientes. Los solicitantes deben llamar [**a GatherWriterStatus después**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) de llamar a [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) para que la sesión de escritor se establezca en un estado completado.

    > [!Note]  
    > Esto solo es necesario en Windows Server 2008 con Service Pack 2 (SP2) y versiones anteriores.

     

    <dl> <dt>

[**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

Durante las operaciones de restauración, un solicitante debe consultar un escritor después de completar estos métodos:
<dl> <dt>

[**IVssBackupComponents::P restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   Las llamadas a [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) que no forman parte de una secuencia de copia de seguridad o restauración bien definida no proporcionan una imagen confiable del estado del escritor, ya que podrían reflejar condiciones que no indican un error en la operación actual, como:
    -   Error de una creación de instantáneas anterior
    -   Error en una operación de copia de seguridad o restauración anticipada
    -   Un escritor que no responde procesa actualmente un evento

Por lo tanto, los desarrolladores no deben basarse en el estado del escritor devuelto por otros procesos, por ejemplo, el solicitante o intentar supervisar el progreso de una instancia de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) con otra (posiblemente en un subproceso independiente).

Tenga en cuenta que para las operaciones de copia de seguridad, donde es necesario examinar los documentos de metadatos del escritor de los escritores, no es necesario llamar al solicitante a [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) después de la generación y el control del evento [*Identify*](vssgloss-i.md) causado [**por IVssBackupComponents::GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

[**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) solo notifica el estado de los escritores cuyos metadatos se proporcionaron a VSS mediante los controladores de eventos [*Identify*](vssgloss-i.md) de los escritores, [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (y devueltos al solicitante por [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).

Si se produce un error en la implementación de un escritor de [**CVssWriter::OnIdentify,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) los metadatos de ese escritor no formarán parte de la lista de documentos de metadatos del escritor proporcionados a VSS, no habrá información de estado disponible y la llamada sería redundante.

Para las operaciones de restauración, donde el solicitante no necesita examinar los documentos de metadatos del escritor de los escritores en ejecución, llamar a [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) puede ser una manera más eficaz de determinar qué escritores se están ejecutando.

 

 



