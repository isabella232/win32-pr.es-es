---
description: Es posible que una aplicación de copia de seguridad (solicitante) finalice y no genere un evento BackupComplete.
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: Controlar eventos BackupShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939e8e64ca9ee463b0b8331e607f8068c3325d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697012"
---
# <a name="handling-backupshutdown-events"></a>Controlar eventos BackupShutdown

Es posible que una aplicación de copia de seguridad (solicitante) finalice y no genere un evento [*BackupComplete*](vssgloss-b.md) . La aplicación de copia de seguridad podría bloquearse o terminarse (desde el administrador de tareas, por ejemplo) y no poder llamar a [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

Por lo tanto, la infraestructura de VSS (en lugar del solicitante) genera un evento [*BackupShutdown*](vssgloss-b.md) cada vez que se libera una instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) que participa en una copia de seguridad, ya sea publicada por el solicitante o por el sistema.

Si una copia de seguridad se realiza correctamente, un escritor recibirá un evento BackupComplete seguido de un evento BackupShutdown.

Si la operación se anula (el solicitante genera un [*evento de anulación*](vssgloss-a.md) mediante una llamada a [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) o produce un error repentinamente, es posible que un escritor solo reciba un evento BackupShutdown y que no reciba otros eventos que realicen operaciones de limpieza. Es un escritor el que determina si un evento BackupShutdown sigue una secuencia de eventos adecuada o representa un error inesperado de las operaciones de copia de seguridad.

El controlador de eventos BackupShutdown, [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), recibe el \_ identificador de VSS (GUID) del conjunto de instantáneas de la operación de copia de seguridad que se está cerrando. El escritor puede usarlo para determinar qué operación de copia de seguridad se está cerrando, si ha almacenado el identificador del conjunto de instantáneas durante su secuencia de copia de seguridad (por ejemplo, desde dentro de [**CVssWriter:: alfreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze), [**CVssWriter::**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)UpDown o [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) mediante [**CVssWriter:: GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid).

Sin embargo, un escritor no debe llamar a [**CVssWriter:: GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) desde [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown). Además, no se puede llamar a **CVssWriter:: GetCurrentSnapshotSetId** después de que [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) devuelva.

Es posible que el escritor esté implicado en varias operaciones de copia de seguridad y, si se llama a un evento BackupShutdown debido a un apagado brusco de un solicitante, el \_ ID. de VSS devuelto podría ser el de otra operación de copia de seguridad en la que estaba participando el escritor.

 

 



