---
description: 'Los eventos de anulación se pueden generar durante una operación de copia de seguridad en cualquiera de los siguientes casos:'
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Anular operaciones VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e4b82ba4227dfeb02e3da91c9bc1e77f10f492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652723"
---
# <a name="aborting-vss-operations"></a>Anular operaciones VSS

Los eventos de [*anulación*](vssgloss-a.md) se pueden generar durante una operación de copia de seguridad en cualquiera de los siguientes casos:

-   Un solicitante genera explícitamente un [*evento de anulación*](vssgloss-a.md) mediante una llamada a [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).
-   Los controladores de eventos [*Freeze*](vssgloss-f.md) y [*accongele de*](vssgloss-t.md) un escritor ([**CVssWriter:: alfreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) y [**CVssWriter:: alreanudar**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) devuelven **false** o no se pueden completar en la ventana de tiempo especificada en [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize).
-   Existe un error del proveedor o VSS durante la creación de una instantánea después del evento [*PrepareForSnapshot*](vssgloss-p.md) .

Las anulaciones no se admiten para las operaciones de restauración.

## <a name="requester-handling-and-creation-of-abort-events"></a>Control del solicitante y creación de eventos de anulación

Una instancia de la interfaz [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) solo se puede usar para una copia de seguridad, por lo que si se produce un error en el procesamiento de una copia de seguridad, suele ser mejor liberar la instancia actual y volver a empezar.

Un solicitante debe indicar explícitamente que se está anulando una operación de copia de seguridad (mediante [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) solo después de la preparación real de una copia de seguridad, que implique escritores, o de la creación de una instantánea.

De hecho, esto significa que cada vez que un solicitante necesita detener una operación de copia de seguridad después de generar un evento [*PrepareForBackup*](vssgloss-p.md) llamando a [**Ivssbackupcomponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), debe llamar a [**ivssbackupcomponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) y esperar su devolución antes de liberar la instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) actual.

Por ejemplo, si un escritor impidió una operación de copia de seguridad, un solicitante debería usar [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) para notificar a todos los demás escritores que la operación de copia de seguridad no se completará.

Antes de llamar a [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), o si se produce un error en la llamada a **PrepareForBackup** , un solicitante puede liberar la instancia actual de la interfaz [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) sin necesidad de generar un evento de anulación.

Por ejemplo, si se usa la instancia actual de [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) simplemente para obtener información llamando a [**IVSSBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) y generando un evento de [*identificación*](vssgloss-i.md) , una vez que se ha devuelto la información, la instancia de **IVSSBackupComponents** solo se puede liberar.

Un solicitante genera una serie de eventos ([*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*reanudación*](vssgloss-t.md)y [*postsnapshot*](vssgloss-p.md)) cuando llama a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Al controlar los eventos Freeze y accongelate, un escritor puede producir un error y generar un evento de anulación por sí mismo. Si no se controlan los eventos PrepareForSnapshot y postsnapshot, no se genera un evento de anulación.

No siempre es posible que un solicitante sepa si se generó un evento de anulación cuando [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) indica un error. Por lo tanto, un solicitante que necesita finalizar una operación de copia de seguridad porque el estado de **IVssBackupComponents::D osnapshotset** indica que un problema debe seguir llamando a [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).

Si un solicitante ha llamado a [**ivssbackupcomponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup), no es necesario llamar a [**Ivssbackupcomponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) antes de liberar una instancia de [**ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

## <a name="writer-handling-and-creation-of-abort-events"></a>Control del escritor y creación de eventos de anulación

Como se indicó anteriormente, un escritor puede recibir un evento de anulación de un solicitante o el proveedor se puede desencadenar uno mismo. Además, es posible que un escritor reciba varios eventos de anulación en determinadas circunstancias. Los desarrolladores del escritor deben codificar cualquier implementación de [**CVssWriter:: onabort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) con esto en mente.

Al controlar un evento de anulación, un escritor debe intentar restaurar el proceso que administra en su estado de ejecución normal, así como realizar cualquier control de errores y registro.

Esto puede significar que una implementación de [**CVssWriter:: onabort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) podría tener que realizar muchas, si no todas, de las mismas tareas que el controlador de eventos procongelate ([**CVssWriter:: alreanudate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) y el controlador de eventos postsnapshot ([**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)), y se puede llamar a estos controladores desde **CVssWriter:: onabort**.

 

 



