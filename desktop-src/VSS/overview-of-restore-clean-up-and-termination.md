---
description: Después de una restauración, los escritores comprueban el estado de la operación para que puedan usar los datos restaurados y tratar los errores.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Introducción a la limpieza y terminación de restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8ad0b7d40f3c0e5322810f96bb120f28effe4ec3f0d4e278af924962713b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122037"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Introducción a la limpieza y terminación de restauración

Después de una restauración, los escritores comprueban el estado de la operación para que puedan usar los datos restaurados y tratar los errores. El solicitante debe esperar a que finalice esta actividad. Para obtener más información, vea [Información general sobre el procesamiento de una restauración en VSS.](overview-of-processing-a-restore-under-vss.md)

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios después de que se haya realizado una operación de restauración.



| Acción del solicitante                                                                                                                                                                                                                                                                                                                                                              | Evento                                                           | Acción del escritor                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El solicitante indica el final de la restauración (vea [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*PostRestore*](vssgloss-p.md) | El escritor realiza la limpieza posterior a la restauración y controla los errores de restauración y los archivos que se han restaurado en ubicaciones no estándar (vea [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| El solicitante espera a los escritores para controlar el [**evento PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) con [**IVssAsync.**](/windows/desktop/api/Vss/nn-vss-ivssasync) También debe comprobar el estado del escritor (vea [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | None                                                            | None                                                                                                                                                                                                                                               |
| El solicitante libera la [**interfaz IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)                                                                                                                                                                                                                                                                                    | None                                                            | None                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>Acciones del solicitante durante la limpieza y finalización

En este punto, un solicitante indica el final de sus actividades de restauración de archivos mediante la generación de un [*evento PostRestore*](vssgloss-p.md) mediante una llamada a [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Las acciones del solicitante se limitan a esperar a los escritores, que pueden necesitar realizar una limpieza final y controlar los errores de restauración, y liberar la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) después de que todos los escritores han devuelto de controlar el [*evento PostRestore.*](vssgloss-p.md)

## <a name="writer-actions-during-cleanup-and-termination"></a>Acciones de escritura durante la limpieza y finalización

El [*evento PostRestore*](vssgloss-p.md) se controla mediante el método virtual [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). La implementación predeterminada simplemente devuelve **true** sin realizar ninguna acción. Si un escritor necesita tener más control de la situación posterior a la restauración, puede invalidar este método.

Además de cualquier limpieza normal (como quitar archivos temporales) que un escritor puede realizar en [**CVssWriter::OnPostRestore,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)puede controlar el éxito o error de las operaciones de restauración.

La forma en que controla los errores de restauración, los archivos restaurados en una ubicación alternativa y la necesidad de restauraciones futuras están completamente a discreción del escritor. Las acciones típicas pueden incluir la comparación de archivos en ubicaciones alternativas o nuevas con los archivos actualmente en uso, la combinación de datos de varios archivos o el inicio de nuevas sesiones conectadas a los nuevos archivos de datos. VSS proporciona los siguientes mecanismos para admitirlo componente a componente:

-   Se puede encontrar un error o un error al restaurar cualquier componente [**con IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)indicará el uso de asignaciones de ubicación alternativas en la restauración de archivos.
-   Determinar si una restauración es incremental y requerirá más restauraciones se realiza mediante una llamada a [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores). Los escritores que necesitan una restauración completa de sus datos no deben reiniciarse hasta que este método devuelva false.
-   Los escritores pueden determinar si el solicitante ha necesitado restaurar archivos en una ubicación no especificada previamente mediante [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

(Para obtener más información sobre cómo restaurar archivos en ubicaciones no predeterminadas, vea Ubicaciones de copia de seguridad y restauración [no predeterminadas).](non-default-backup-and-restore-locations.md)

Al igual que con cualquier método [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) la información [](vssgloss-e.md) devuelta por una instancia [](vssgloss-i.md) determinada se aplica a los componentes incluidos explícitamente para la copia de seguridad y a cualquiera de sus incluidos implícitamente para los subcomponentes de copia de seguridad, incluidos los subcomponentes incluidos explícitamente para la restauración por el solicitante mediante [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) (consulte Working with Selectability for Restore and [Subcomponents](working-with-selectability-for-restore-and-subcomponents.md) para obtener más información).

Dado que los escritores requerirán acceso al documento componentes de copia de seguridad, es importante que el solicitante no libere la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) hasta que los escritores terminen de procesarse.

 

 



