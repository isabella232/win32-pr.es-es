---
description: 'Los eventos de anulación se pueden generar durante una operación de copia de seguridad en cualquiera de los casos siguientes:'
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Anular operaciones de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e4b82ba4227dfeb02e3da91c9bc1e77f10f492
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473411"
---
# <a name="aborting-vss-operations"></a>Anular operaciones de VSS

[*Los eventos*](vssgloss-a.md) de anulación se pueden generar durante una operación de copia de seguridad en cualquiera de los casos siguientes:

-   Un solicitante genera explícitamente un evento [*Abort*](vssgloss-a.md) llamando a [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).
-   Los controladores de eventos [*Freeze*](vssgloss-f.md) y [*Thaw*](vssgloss-t.md) de un escritor ([**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) y [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) devuelven **false** o no se pueden completar en la ventana de tiempo especificada en [**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize).
-   Hay cualquier error del proveedor o VSS durante la creación de una instantánea después del [*evento PrepareForSnapshot.*](vssgloss-p.md)

No se admiten anulaciones para las operaciones de restauración.

## <a name="requester-handling-and-creation-of-abort-events"></a>Control y creación de eventos de anulación del solicitante

Una instancia de la interfaz [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) solo se puede usar para una copia de seguridad, por lo que si se produce un error al procesar una copia de seguridad, generalmente es mejor liberar la instancia actual e iniciar de nuevo.

Un solicitante debe indicar explícitamente que está anulando una operación de copia de seguridad (mediante [**IVssBackupComponents::AbortBackup)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)solo después de que se haya realizado la preparación real para una copia de seguridad, que implica escritores, o bien la creación de una instantánea.

De hecho, esto significa que cada vez que un solicitante necesita detener una operación de copia de seguridad después de generar un evento [*PrepareForBackup*](vssgloss-p.md) mediante una llamada a [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), debe llamar a [**IVssBackupComponents::AbortBackup y**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) esperar su devolución antes de liberar la instancia actual de [**IVSSBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

Por ejemplo, si un escritor vetó una operación de copia de seguridad, un solicitante debe usar [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) para notificar a todos los demás escritores que la operación de copia de seguridad no se completará.

Antes de llamar a [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)o si se produce un error en la llamada a **PrepareForBackup,** un solicitante puede liberar la instancia actual de la interfaz [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) sin necesidad de generar un evento Abort.

Por ejemplo, si la instancia actual de [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) se usa simplemente para obtener información llamando a [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) y generando un evento [*Identify,*](vssgloss-i.md) una vez que se ha devuelto información, la instancia de **IVSSBackupComponents** simplemente se puede liberar.

Un solicitante genera una serie de eventos [*(PrepareForSnapshot,*](vssgloss-p.md) [*Freeze*](vssgloss-f.md), [*Thaw*](vssgloss-t.md)y [*PostSnapshot*](vssgloss-p.md)) cuando llama a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Mientras se administran los eventos Freeze y Thaw, un escritor puede producir un error y puede generar un evento Abort por sí mismo. Si no se controlan los eventos PrepareForSnapshot y PostSnapshot, no se genera un evento Abort.

No siempre es posible que un solicitante sepa si se generó un evento Abort cuando [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) indica un error. Por lo tanto, un solicitante que necesita finalizar una operación de copia de seguridad porque el estado de **IVssBackupComponents::D oSnapshotSet** indica que un problema todavía debe llamar a [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).

Si un solicitante ha llamado a [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup), no es necesario llamar a [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) antes de liberar una instancia de [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

## <a name="writer-handling-and-creation-of-abort-events"></a>Control del escritor y creación de eventos de anulación

Como se indicó anteriormente, un escritor puede recibir un evento Abort de un solicitante o el proveedor puede desencadenar uno mismo. Además, es posible que un escritor reciba varios eventos Abort en determinadas circunstancias. Los desarrolladores de escritores deben codificar cualquier implementación [**de CVssWriter::OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) con esto en mente.

Al controlar un evento Abort, un escritor debe intentar restaurar el proceso que ha administrado a su estado de ejecución normal, así como realizar cualquier control de errores y registro.

Esto puede significar que una implementación de [**CVssWriter::OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) podría tener que realizar muchas, si no todas, de las mismas tareas que el controlador de eventos Thaw ([**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) y el controlador de eventos PostSnapshot ([**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)), y se puede llamar a estos controladores desde **CVssWriter::OnAbort**.

 

 



