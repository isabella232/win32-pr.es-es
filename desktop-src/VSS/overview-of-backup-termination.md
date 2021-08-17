---
description: En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para que finalice una operación de copia de seguridad. Para obtener más información, vea Información general sobre el procesamiento de una copia de seguridad en VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Información general sobre la terminación de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fd57822a62cf3fa39cee2b17d79ae2545afa07bd722d26cacda68cba3b6695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937973"
---
# <a name="overview-of-backup-termination"></a>Información general sobre la terminación de copia de seguridad

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para que finalice una operación de copia de seguridad. Para obtener más información, vea [Información general sobre el procesamiento de una copia de seguridad en VSS.](overview-of-processing-a-backup-under-vss.md)



| Acción del solicitante                                                                                                                                                                                                              | Evento                                                                 | Acción del escritor                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El solicitante finaliza la instantánea liberando la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o llamando a [**IVssBackupComponents::D eleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). | None                                                                  | None                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) se publica mediante una [**llamada a IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | El escritor controla el evento con [**CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), lo que le permite limpiar cualquier estado relacionado con el conjunto de instantáneas. Si se produjo un error en la operación de copia de seguridad (es decir, no generó un evento [**BackupComplete),**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) es posible que el escritor también tenga que realizar el control de errores. Consulte [Control de eventos backupShutdown](handling-backupshutdown-events.md) para obtener más información. |



 

Dado que no se puede reutilizar una interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y el destructor de la interfaz finaliza las instantáneas, normalmente no hay ninguna razón para llamar a [**IVssBackupComponents::D eleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). Este método está diseñado para usarse junto con el control de errores y la anulación de copias de seguridad (vea [Aborting VSS Operations](aborting-vss-operations.md)).

 

 
