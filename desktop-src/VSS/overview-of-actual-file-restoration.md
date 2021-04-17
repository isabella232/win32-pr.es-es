---
description: Después de realizar las acciones descritas en información general sobre la inicialización de restauración y la introducción a la preparación de la restauración, el solicitante tiene suficiente información para empezar a restaurar los archivos.
ms.assetid: 15df39fa-1eb1-4e96-9e26-14470f391de4
title: Información general de la restauración de archivos real
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6527a10d0880b1e599377abb797449816019ab89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696994"
---
# <a name="overview-of-actual-file-restoration"></a>Información general de la restauración de archivos real

Después de realizar las acciones descritas en [información general sobre la inicialización de restauración](overview-of-restore-initialization.md) y la introducción a la preparación de la [restauración](overview-of-preparing-for-restore.md), el solicitante tiene suficiente información para empezar a restaurar los archivos. La restauración de archivos no implica interacciones del escritor ni la generación de eventos. Para obtener más información, vea [información general sobre el procesamiento de una restauración en VSS](overview-of-processing-a-restore-under-vss.md).

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para restaurar archivos.



| Acción del solicitante                                                                                                                                                                                                                                                                                                          | Evento | Acción del escritor |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------|
| Generar una lista de conjuntos de restauración para archivos en medios de copia de seguridad.                                                                                                                                                                                                                                                                 | None  | None          |
| Controlar los [*destinos dirigidos*](vssgloss-d.md) o la restauración [*parcial de archivos*](vssgloss-p.md) (vea [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget), [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)). | None  | None          |
| Si es necesario, omita todas las ubicaciones de restauración especificadas y restáurela en una nueva ubicación especificada en una llamada anterior a [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).                                                                                                                       | None  | None          |
| Si la restauración es incremental y se necesitan restauraciones adicionales, indique (consulte [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) y [copias de seguridad incrementales y diferenciales](incremental-and-differential-backups.md)).                                                     | None  | None          |
| Para saber si un escritor ha modificado el contenido del documento de componentes de copia de seguridad, llame a [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). Por ejemplo, el escritor podría haber cambiado el destino de restauración.                                                                 | None  | None          |



 

## <a name="requester-actions-during-restoring-files"></a>Acciones del solicitante durante la restauración de archivos

Para la mayoría de los archivos del medio de copia de seguridad, el solicitante debe determinar sus ubicaciones originales y todas las ubicaciones nuevas o asignaciones de ubicación alternativas que se les apliquen. (Vea [generar un conjunto de restauración](generating-a-restore-set.md) para obtener una explicación de los procedimientos recomendados para determinar qué archivos se van a restaurar y dónde restaurarlos).

Además, algunos archivos pueden tener [*destinos dirigidos*](vssgloss-d.md) o admitir la restauración [*parcial de archivos*](vssgloss-p.md) . El número de estos archivos se puede encontrar mediante una llamada a [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) y [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount), y se puede encontrar información sobre las instrucciones de restauración detalladas llamando a [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) y [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). (Los archivos parciales y dirigidos pueden formar parte de los componentes agregados implícita o explícitamente a la copia de seguridad original. para obtener más información, vea [trabajar con la selección para restaurar y subcomponentes](working-with-selectability-for-restore-and-subcomponents.md) .)

El éxito o el fracaso de una restauración se indica en función de cada componente mediante [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). La necesidad de operaciones de restauración adicionales (en el caso de las restauraciones incrementales o diferenciales) también se indica de forma individual componente a componente mediante [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

En general, VSS no especifica un mecanismo para recuperar datos de un medio de almacenamiento, una opción de medio de almacenamiento o cómo determinar qué archivos deben restaurarse donde.

Sin embargo, para determinados escritores, la restauración de archivos puede implicar el uso de una interfaz y un procedimiento personalizados documentados. Los sistemas de escritura del sistema de Windows, que actualmente requieren dicha compatibilidad, están documentados en [casos especiales de uso de VSS](special-vss-usage-cases.md).

En general, se recomienda que los archivos de cada componente de cada [*instancia del escritor*](vssgloss-w.md) se procesen como una unidad. Esto requiere lo siguiente:

-   Asociar cada archivo que se va a restaurar con el componente que lo administra. Esto requiere el uso de documentos de metadatos de escritor.
-   Obtención de la información de destino de restauración correcta. Esto requiere información del documento componentes de copia de seguridad.

 

 



