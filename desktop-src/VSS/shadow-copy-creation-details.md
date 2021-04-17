---
description: En general, el modo en que se crea una instantánea depende del tipo de instantánea que se va a crear, su contexto y el rol que se concede a los escritores en la operación de instantánea.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Detalles de la creación de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9281b899593ca0751f1d549aed60305041b18c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696966"
---
# <a name="shadow-copy-creation-details"></a>Detalles de la creación de instantáneas

En general, el modo en que se crea una instantánea depende del tipo de instantánea que se va a crear, su contexto y el rol que se concede a los escritores en la operación de instantánea. (Vea [configuraciones de contexto](shadow-copy-context-configurations.md) de instantáneas para obtener más información).

El contexto de instantánea se establece mediante una llamada al método [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) . Antes de llamar al método [**ivssbackupcomponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) para crear una instantánea, los solicitantes deben llamar a los métodos [**ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) en el orden especificado en las secciones siguientes.

## <a name="prerequisites-for-all-shadow-copies"></a>Requisitos previos para todas las instantáneas

Independientemente del nivel de participación del escritor, la creación de cualquier instantánea siempre requerirá que el solicitante se inicialice con llamadas a [**ivssbackupcomponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) y [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Si no se realiza esta llamada, el método [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) devolverá un error.

## <a name="shadow-copies-with-writer-participation"></a>Instantáneas con participación del redactor

Si el contexto de instantáneas especifica la participación del escritor (es decir, se llama a [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) con la **copia de \_ \_ seguridad de VSS CTX** o la **\_ \_ \_ reversión de la aplicación VSS CTX**):

-   Los solicitantes siempre deben llamar a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) cuando el contexto de instantáneas admita la participación del escritor. Si el contexto de instantáneas admite la participación del escritor y **ivssbackupcomponents:: GatherWriterMetadata** no se llama antes que [**Ivssbackupcomponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), se devolverá un error.
-   Si un solicitante desea seleccionar componentes de escritor específicos, debe llamar a [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) antes de llamar a [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para crear el conjunto de instantáneas.
-   Se debe llamar a [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para crear el conjunto de instantáneas.
-   Los solicitantes pueden agregar uno o más volúmenes al conjunto de instantáneas llamando a [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). Es posible que algunos componentes del escritor no especifiquen los volúmenes afectados. En este caso, es aceptable que un conjunto de instantáneas esté vacío (es decir, que no contenga volúmenes).
-   Para garantizar la coherencia de los metadatos del escritor, un solicitante siempre debe llamar a [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) aunque no se seleccione ningún componente. Esto hace que VSS genere un evento **PrepareForBackup** , en el que VSS llama al método [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) para cada redactor participante.
-   VSS generará [*PrepareForSnapshot*](vssgloss-p.md) y [*congelará*](vssgloss-f.md) eventos antes de crear la instantánea en respuesta a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Los escritores controlarán los eventos con [**CVssWriter:: OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) y [**CVssWriter:: alfreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   VSS generará eventos de [*reanudación*](vssgloss-t.md) y de [*instantáneas*](vssgloss-p.md) después de crear una instantánea en respuesta a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Los escritores controlarán los eventos con [**CVssWriter:: Alreanudar**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) y [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot).

## <a name="shadow-copies-without-writer-participation"></a>Instantáneas sin participación del escritor

No se recomienda crear instantáneas sin la participación del escritor para las aplicaciones de copia de seguridad estándar (consulte [copias de seguridad sin participación del escritor](backups-without-writer-participation.md)).

Hay usos, como las copias de seguridad rápidas de un disco para proporcionar una red de seguridad contra daños accidentales de archivos, que se pueden realizar sin la participación explícita del escritor. Este tipo de instantánea tendría un contexto de la **copia de \_ \_ seguridad del \_ recurso \_ compartido de archivos de VSS CTX** o de la **\_ \_ \_ reversión de NAS de VSS CTX**.

Para este tipo de instantánea, tenga en cuenta lo siguiente:

-   Los solicitantes deben seguir llamando a los métodos necesarios que se enumeran en [requisitos previos para todas las instantáneas](#prerequisites-for-all-shadow-copies).
-   Los solicitantes pueden llamar a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), pero esto no es necesario.
-   Si los solicitantes llaman a [**ivssbackupcomponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent), [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)o [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete), se devolverá un error.
-   Los proveedores no generarán eventos [*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*reanudar*](vssgloss-t.md)o [*postsnapshot*](vssgloss-p.md) para este tipo de instantánea.

 

 



