---
description: Es posible que una aplicación de copia de seguridad (solicitante) finalice y no genere un evento BackupComplete.
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: Control de eventos BackupShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e60a063a11f0a492407daed31ace4a62aec2a13fe824e110de272d58b84bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998255"
---
# <a name="handling-backupshutdown-events"></a>Control de eventos BackupShutdown

Es posible que una aplicación de copia de seguridad (solicitante) finalice y no genere un [*evento BackupComplete.*](vssgloss-b.md) La aplicación de copia de seguridad podría bloquearse o finalizarse (desde la Administrador de tareas, por ejemplo) y no poder llamar a [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

Por lo tanto, la infraestructura de VSS (en lugar del solicitante) genera un evento [*BackupShutdown*](vssgloss-b.md) cada vez que se libera una instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) que participa en una copia de seguridad, ya sea por el solicitante o por el sistema.

Si una copia de seguridad continúa correctamente, un escritor recibirá un evento BackupComplete seguido de un evento BackupShutdown.

Si la operación se anula (el solicitante genera un evento [*Abort*](vssgloss-a.md) llamando a [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) o produce un error repentinamente, un escritor puede recibir solo un evento BackupShutdown y es posible que no reciba otros eventos que realicen operaciones de limpieza. Un escritor debe determinar si un evento BackupShutdown sigue una secuencia adecuada de eventos o representa un error inesperado de las operaciones de copia de seguridad.

El controlador de eventos BackupShutdown, [**CVssWriter::OnBackupShutdown,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)recibe el identificador de VSS (GUID) del conjunto de instantáneas de la operación de copia de seguridad que se \_ está cerrando. El escritor puede usarlo para determinar qué operación de copia de seguridad se está cerrando, si ha almacenado el identificador del conjunto de instantáneas durante su secuencia de copia de seguridad (por ejemplo, desde [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze), [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)o [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) mediante [**CVssWriter::GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid).

Sin embargo, un escritor no debe llamar [**a CVssWriter::GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) desde [**CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown). Además, **no se puede llamar a CVssWriter::GetCurrentSnapshotSetId** después de que [**CVssWriter::OnPostSnapshot devuelva**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) .

Es posible que el escritor esté implicado en varias operaciones de copia de seguridad y, si se llama a un evento BackupShutdown debido a un apagado brusco de un solicitante, el identificador de VSS devuelto podría ser el de otra operación de copia de seguridad en la que participaba el \_ escritor.

 

 



