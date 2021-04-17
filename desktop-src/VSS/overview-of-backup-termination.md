---
description: En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para finalizar una operación de copia de seguridad. Para obtener más información, vea información general sobre el procesamiento de una copia de seguridad en VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Información general sobre la terminación de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9268bd8fd4ec51be2ee7a891d4dffb3a5cb1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696992"
---
# <a name="overview-of-backup-termination"></a>Información general sobre la terminación de copia de seguridad

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para finalizar una operación de copia de seguridad. Para obtener más información, vea [información general sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md).



| Acción del solicitante                                                                                                                                                                                                              | Evento                                                                 | Acción del escritor                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El solicitante finaliza la instantánea liberando la interfaz [**ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o llamando a [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). | None                                                                  | None                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) se libera llamando a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | El escritor controla el evento con [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), que permite limpiar cualquier estado relacionado con el conjunto de instantáneas. Si se produjo un error en la operación de copia de seguridad, es decir, no generó un evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , es posible que el escritor también tenga que realizar el control de errores. Consulte [control de eventos BackupShutdown](handling-backupshutdown-events.md) para obtener más información. |



 

Dado que no se puede volver a usar una interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y el destructor de la interfaz finaliza las instantáneas, normalmente no hay ningún motivo para llamar a [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). Este método está diseñado para usarse junto con el control de errores y la anulación de las copias de seguridad (consulte [anulación de operaciones VSS](aborting-vss-operations.md)).

 

 
