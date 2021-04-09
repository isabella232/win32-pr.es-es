---
description: Después de una restauración, los escritores comprueban el estado de la operación para que puedan hacer uso de los datos restaurados y tratar con errores.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Información general sobre la limpieza y la finalización de la restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 391e029cdb109589b42240b5482f6aba2ff43555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082482"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Información general sobre la limpieza y la finalización de la restauración

Después de una restauración, los escritores comprueban el estado de la operación para que puedan hacer uso de los datos restaurados y tratar con errores. El solicitante debe esperar a que se complete la actividad. Para obtener más información, vea [información general sobre el procesamiento de una restauración en VSS](overview-of-processing-a-restore-under-vss.md).

En la tabla siguiente se muestra la secuencia de acciones y eventos que son necesarios una vez que se realiza una operación de restauración.



| Acción del solicitante                                                                                                                                                                                                                                                                                                                                                              | Evento                                                           | Acción del escritor                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El solicitante indica el final de la restauración (consulte [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*Postrestore*](vssgloss-p.md) | El escritor realiza la limpieza posterior a la restauración y controla los errores de restauración y los archivos que se han restaurado en ubicaciones no estándar (vea [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| El solicitante espera en los escritores para controlar el evento [**Postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) con [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync). También debe comprobar el estado del escritor (consulte [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | None                                                            | None                                                                                                                                                                                                                                               |
| El solicitante libera la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .                                                                                                                                                                                                                                                                                    | None                                                            | None                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>Acciones del solicitante durante la limpieza y la finalización

En este momento, un solicitante indica el final de sus actividades de restauración de archivos generando un evento [*Postrestore*](vssgloss-p.md) mediante una llamada a [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Las acciones del solicitante se limitan a esperar en los escritores, lo que puede necesitar realizar una limpieza final y controlar los errores de restauración, y liberar la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) después de que todos los escritores hayan devuelto el control del evento [*postrestore*](vssgloss-p.md) .

## <a name="writer-actions-during-cleanup-and-termination"></a>Acciones del escritor durante la limpieza y la finalización

El evento [*Postrestore*](vssgloss-p.md) se controla mediante el método virtual [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). La implementación predeterminada simplemente devuelve **true** sin realizar ninguna acción. Si un escritor necesita ejercer más control sobre la situación posterior a la restauración, puede invalidar este método.

Además de cualquier limpieza normal (por ejemplo, la eliminación de archivos temporales) que puede realizar un escritor en [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), puede controlar el éxito o el fracaso de las operaciones de restauración.

La forma en que trata los errores de restauración, los archivos restaurados en una ubicación alternativa y la necesidad de futuras restauraciones se producen por completo en la discreción del escritor. Las acciones típicas pueden incluir la comparación de archivos en ubicaciones alternativas o nuevas con archivos actualmente en uso, la combinación de datos de varios archivos o el inicio de nuevas sesiones conectadas a los nuevos archivos de datos. VSS proporciona los siguientes mecanismos para admitir este componente cada componente:

-   Se puede encontrar el éxito o el error en la restauración de cualquier componente con [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   El uso de asignaciones de ubicación alternativas en la restauración de archivos se indicará mediante [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Determinar si una restauración es incremental y necesitará más restauraciones mediante una llamada a [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores). Los escritores que necesiten una restauración completa de sus datos no deberían reiniciarse hasta que este método devuelva false.
-   Los escritores pueden determinar si el solicitante necesitaba restaurar archivos en una ubicación no especificada anteriormente mediante [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) y [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

(Para obtener más información sobre la restauración de archivos en ubicaciones no predeterminadas, vea [ubicaciones de copia de seguridad y restauración no predeterminadas](non-default-backup-and-restore-locations.md)).

Al igual que con cualquier método [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , la información devuelta por una instancia determinada se aplica a los componentes que se [*incluyen explícitamente*](vssgloss-e.md) para la copia de seguridad y cualquiera de sus elementos [*incluidos implícitamente*](vssgloss-i.md) para los subcomponentes de copia de seguridad, incluidos los [subcomponentes incluidos](working-with-selectability-for-restore-and-subcomponents.md) explícitamente para su restauración por parte del solicitante mediante [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)

Dado que los escritores necesitarán acceso al documento componentes de copia de seguridad, es importante que el solicitante no libere la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) hasta que los escritores hayan terminado de procesarse.

 

 



