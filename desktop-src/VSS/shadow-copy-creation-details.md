---
description: En general, la forma en que se crea una instantánea depende del tipo de instantánea que se va a crear, su contexto y el rol que se asigna a los escritores en la operación de instantánea.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Detalles de creación de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d8f506ef8d5c7acff86cb6a2fa890b3773423fddf339ea4911a0299963224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998135"
---
# <a name="shadow-copy-creation-details"></a>Detalles de creación de instantáneas

En general, la forma en que se crea una instantánea depende del tipo de instantánea que se va a crear, su contexto y el rol que se asigna a los escritores en la operación de instantánea. (Vea [Configuraciones de contexto de instantáneas](shadow-copy-context-configurations.md) para obtener más información).

El contexto de la instantánea se establece mediante una llamada [**al método IVssBackupComponents::SetContext.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) Antes de llamar al método [**IVssBackupComponents::D oSnapshotSet para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) crear una instantánea, los solicitantes deben llamar a los [**métodos IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) en el orden especificado en las secciones siguientes.

## <a name="prerequisites-for-all-shadow-copies"></a>Requisitos previos para todas las instantáneas

Independientemente del nivel de participación del escritor, la creación de cualquier instantánea siempre requerirá que el solicitante se inicialice con llamadas a [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) e [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Si no se realiza esta llamada, el método [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) devolverá un error.

## <a name="shadow-copies-with-writer-participation"></a>Instantáneas con participación del escritor

Si el contexto de instantánea especifica la participación del escritor (es decir, se llama a [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) con **VSS \_ CTX \_ BACKUP** o **VSS \_ CTX \_ APP \_ ROLLBACK**):

-   Los solicitantes siempre deben llamar a [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) cuando el contexto de instantánea admite la participación del escritor. Si el contexto de instantánea admite la participación del escritor y no se llama a **IVssBackupComponents::GatherWriterMetadata** antes de [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), se devolverá un error.
-   Si un solicitante desea seleccionar componentes de escritor específicos, debe llamar a [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) antes de llamar a [**StartSnapshotSet para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) crear el conjunto de instantáneas.
-   [**Se debe llamar a StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para crear el conjunto de instantáneas.
-   Los solicitantes pueden agregar uno o varios volúmenes al conjunto de instantáneas llamando a [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). Es posible que algunos componentes de escritor no especifiquen volúmenes afectados. En este caso, es aceptable que un conjunto de instantáneas esté vacío (es decir, que no contenga volúmenes).
-   Para garantizar la coherencia de los metadatos del escritor, un solicitante siempre debe llamar a [**IVssBackupComponents::P repareForBackup incluso**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) si no se selecciona ningún componente. Esto hace que VSS genere un evento **PrepareForBackup,** en el que VSS llama al método [**CVssWriter::OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) para cada escritor participante.
-   VSS generará los eventos [*PrepareForSnapshot*](vssgloss-p.md) y [*Freeze*](vssgloss-f.md) antes de crear la instantánea en respuesta a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Los escritores controlarán los eventos [**con CVssWriter::OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) y [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   VSS generará eventos [*Thaw*](vssgloss-t.md) y [*eventos PostSnapshot*](vssgloss-p.md) después de crear una instantánea en respuesta a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Los escritores controlarán los eventos [**con CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) y [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot).

## <a name="shadow-copies-without-writer-participation"></a>Instantáneas sin participación del escritor

No se recomienda crear instantáneas sin la participación del escritor para las aplicaciones de copia de seguridad estándar (vea Copias de [seguridad sin participación del escritor).](backups-without-writer-participation.md)

Hay usos, como copias de seguridad rápidas de un disco para proporcionar una red de seguridad contra daños accidentales en los archivos, que se pueden realizar sin la participación explícita del escritor. Esta instantánea tendría un contexto de COPIA DE SEGURIDAD DE RECURSO COMPARTIDO DE ARCHIVOS **DE VSS \_ CTX \_ \_ \_** o **\_ \_ \_ ROLLBACK de NAS de VSS CTX.**

Para este tipo de instantánea, tenga en cuenta lo siguiente:

-   Los solicitantes todavía deben llamar a los métodos necesarios [enumerados en Requisitos previos para todas las instantáneas.](#prerequisites-for-all-shadow-copies)
-   Los solicitantes pueden [**llamar a IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), pero esto no es necesario.
-   Si los [**solicitantes llaman a IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent), [**IVssBackupComponents::P repareForBackup o**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete), se devolverá un error.
-   Los proveedores no generarán [*eventos PrepareForSnapshot,*](vssgloss-p.md) [*Freeze,*](vssgloss-f.md) [*Thaw*](vssgloss-t.md) [*o PostSnapshot*](vssgloss-p.md) para este tipo de instantánea.

 

 



