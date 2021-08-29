---
description: Después de realizar las acciones descritas en Información general de inicialización de restauración e Información general sobre la preparación para la restauración, el solicitante tiene información suficiente para empezar a restaurar archivos.
ms.assetid: 15df39fa-1eb1-4e96-9e26-14470f391de4
title: Información general sobre la restauración real de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2cc1b74f7beae7f5686dc36ce741428cad97ae62c62c8895122ec8a639e46f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998245"
---
# <a name="overview-of-actual-file-restoration"></a>Información general sobre la restauración real de archivos

Después de realizar las acciones descritas en [Información](overview-of-restore-initialization.md) general de inicialización de restauración e Información general sobre la preparación para la restauración [,](overview-of-preparing-for-restore.md)el solicitante tiene información suficiente para empezar a restaurar archivos. La restauración de archivos no implica interacciones de escritor ni la generación de eventos. Para obtener más información, vea [Información general sobre el procesamiento de una restauración en VSS.](overview-of-processing-a-restore-under-vss.md)

En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para restaurar archivos.



| Acción del solicitante                                                                                                                                                                                                                                                                                                          | Evento | Acción del escritor |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------|
| Generar una lista de conjunto de restauración para archivos en medios de copia de seguridad.                                                                                                                                                                                                                                                                 | None  | None          |
| Controlar [*destinos dirigidos*](vssgloss-d.md) [*o restauración parcial*](vssgloss-p.md) de archivos (vea [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget), [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)). | None  | None          |
| Si es necesario, ignore todas las ubicaciones de restauración especificadas y restaure a una nueva ubicación especificada en una llamada anterior a [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).                                                                                                                       | None  | None          |
| Si la restauración es incremental y se necesitan más restauraciones, indique (vea [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) y Copias de seguridad [incrementales y diferenciales).](incremental-and-differential-backups.md)                                                     | None  | None          |
| Para obtener información sobre si un escritor ha modificado el contenido del documento componentes de copia de seguridad, llame a [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). Por ejemplo, el escritor podría haber cambiado el destino de restauración.                                                                 | None  | None          |



 

## <a name="requester-actions-during-restoring-files"></a>Acciones del solicitante durante la restauración de archivos

Para la mayoría de los archivos del medio de copia de seguridad, el solicitante debe determinar sus ubicaciones originales y las nuevas ubicaciones o asignaciones de ubicaciones alternativas que se les apliquen. (Vea [Generar un conjunto de restauración para](generating-a-restore-set.md) obtener una explicación de los procedimientos recomendados para determinar qué archivos restaurar y dónde restaurarlos).

Además, algunos archivos pueden tener [*destinos dirigidos*](vssgloss-d.md) o admitir la [*restauración parcial de*](vssgloss-p.md) archivos. El número de estos archivos se puede encontrar llamando a [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent::GetPartialFileCount,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)y se puede encontrar información sobre las instrucciones de restauración detalladas llamando a [**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) e [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). (Los archivos parciales y dirigidos pueden formar parte de componentes agregados implícita o explícitamente a la copia de seguridad original; vea Trabajar con selectibilidad para la restauración y [subcomponentes](working-with-selectability-for-restore-and-subcomponents.md) para obtener más información).

El éxito o el error de una restauración se indica componente a componente mediante [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). La necesidad de realizar más operaciones de restauración (en el caso de restauraciones incrementales o diferenciales) también se indica componente a componente mediante [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

En general, VSS no especifica un mecanismo para recuperar datos de un medio de almacenamiento, una opción de medio de almacenamiento o cómo determinar qué archivos se deben restaurar donde.

Sin embargo, para determinados escritores, la restauración de archivos puede implicar el uso de una interfaz y un procedimiento personalizados documentados. Windows escritores del sistema, que actualmente requieren este tipo de compatibilidad, se documentan en [Casos de uso especiales de VSS](special-vss-usage-cases.md).

En general, se recomienda que los archivos de cada componente de cada instancia de escritor [*se*](vssgloss-w.md) procese como una unidad. Esto requiere lo siguiente:

-   Asociación de cada archivo que se va a restaurar con el componente que lo administra. Esto requiere el uso de documentos de metadatos del escritor.
-   Obtener la información de destino de restauración correcta. Esto requiere información del documento componentes de copia de seguridad.

 

 



