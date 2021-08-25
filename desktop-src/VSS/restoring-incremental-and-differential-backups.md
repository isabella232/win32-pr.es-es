---
description: Restaurar una copia de seguridad incremental o diferencial en VSS no es significativamente diferente de cualquier otra operación de restauración de VSS.
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: Restaurar copias de seguridad incrementales y diferenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcc0c2df57e2f7c0f21436248ddaa46231c7bf6440c76a38f4d1c92ab2adf97f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864055"
---
# <a name="restoring-incremental-and-differential-backups"></a>Restaurar copias de seguridad incrementales y diferenciales

Restaurar una copia de seguridad incremental o diferencial en VSS no es significativamente diferente de cualquier otra operación de restauración de VSS.

Un escritor puede modificar los destinos de restauración o solicitar destinos dirigidos, y un solicitante debe controlar asignaciones de ubicación alternativas y nuevos destinos, al igual que con cualquier otra restauración. Sin embargo, hay dos problemas importantes que se deben tener en cuenta al controlar la restauración de una copia de seguridad incremental o diferencial: restauraciones adicionales y marcas de copia de seguridad.

## <a name="additional-restores"></a>Restauraciones adicionales

El primer problema es el de restauraciones adicionales. Un operador de copia de seguridad puede necesitar ejecutar varias operaciones de restauración mediante un medio de copia de seguridad incremental o diferencial inicial completo y posterior como origen.

Algunos escritores, normalmente como parte de su control de un evento [*PostRestore*](vssgloss-p.md) mediante [**CVssWriter::OnPostRestore,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)usan archivos restaurados para realizar actualizaciones de datos actualmente en disco. Para algunos de estos escritores, es ineficaz (o peligroso) actualizar repetidamente los datos en disco de archivos restaurados.

Por lo tanto, es importante que las aplicaciones de copia de seguridad indiquen cuándo un componente o conjunto de componentes puede requerir restauraciones posteriores mediante una llamada a [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

Un escritor llamaría a [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) para determinar si el operador de copia de seguridad planeaba más restauraciones del componente o conjunto de componentes.

Si el solicitante no ha llamado a [**IVssBackupComponents::SetAdditionalRestores,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) devuelve false y el escritor puede realizar cualquier procesamiento posterior a la restauración que necesite.

Si se ha llamado a [**IVssBackupComponents::SetAdditionalRestores,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) devuelve **true** y un escritor debe decidir cómo controlar las operaciones posteriores a la restauración; por ejemplo, el escritor puede decidir no actualizar sus datos en disco.

## <a name="backup-stamps"></a>Marcas de copia de seguridad

Como parte de la operación de copia de seguridad completa anterior, es posible que un escritor haya almacenado una marca de copia de seguridad en el documento componentes de copia de seguridad del solicitante.

La marca de copia de seguridad se almacena como una cadena y su formato e información no son inteligibles para el solicitante. Por lo tanto, el solicitante no puede hacer un uso directo de la información de la marca de copia de seguridad.

En su lugar, su tarea consiste en poner esa información a disposición del escritor, llamando al método [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) antes de generar un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para una copia de seguridad incremental.

El solicitante lo hace componente a componente. Un solicitante examina la información de la marca de copia de seguridad del conjunto de componentes o componentes [**almacenados mediante IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).

Si la información de la marca de copia de seguridad es adecuada para el tipo de restauración que está realizando el solicitante, la pone a disposición como marca de tiempo de la última copia de seguridad de un componente con el método [**IVssBackupComponents::SetPreviousBackupStamp.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)

Un escritor recupera la información de la marca de copia de seguridad [**mediante IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Un escritor de esta clase generó la marca de copia de seguridad inicial, por lo que el escritor puede descodificar esta marca y usar la información. En función de esto, al controlar un evento [**de PreRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) un escritor puede optar por realizar acciones como cambiar los destinos de restauración o solicitar destinos dirigidos.

 

 



