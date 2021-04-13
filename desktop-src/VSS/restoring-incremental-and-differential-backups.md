---
description: La restauración de una copia de seguridad incremental o diferencial en VSS no es significativamente diferente de cualquier otra operación de restauración de VSS.
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: Restaurar copias de seguridad incrementales y diferenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 639919ea24f12fbc036116bd89b1630321cbae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544963"
---
# <a name="restoring-incremental-and-differential-backups"></a>Restaurar copias de seguridad incrementales y diferenciales

La restauración de una copia de seguridad incremental o diferencial en VSS no es significativamente diferente de cualquier otra operación de restauración de VSS.

Un escritor puede modificar destinos de restauración o solicitar destinatarios dirigidos, y un solicitante debe administrar asignaciones de ubicaciones alternativas y nuevos destinos, al igual que con cualquier otra restauración. Sin embargo, hay dos aspectos importantes que se deben tener en cuenta en el control de la restauración de una copia de seguridad incremental o diferencial: restauraciones adicionales y marcas de copia de seguridad.

## <a name="additional-restores"></a>Restauraciones adicionales

El primer problema es el de las restauraciones adicionales. Es posible que un operador de copia de seguridad tenga que ejecutar varias operaciones de restauración mediante un medio de copia de seguridad incremental inicial y posterior o diferencial como origen.

Algunos escritores, normalmente como parte de su control de un evento [*Postrestore*](vssgloss-p.md) mediante [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), usan archivos restaurados para realizar actualizaciones de los datos que se encuentran actualmente en el disco. En el caso de algunos de estos escritores, es ineficaz (o peligroso) actualizar repetidamente los datos en disco de los archivos restaurados.

Por lo tanto, es importante que las aplicaciones de copia de seguridad indiquen Cuándo un componente o un conjunto de componentes pueden requerir restauraciones posteriores llamando a [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

Un escritor llamaría a [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) para determinar si el operador de copia de seguridad planeó más restauraciones del componente o del conjunto de componentes.

Si el solicitante no hubiera llamado a [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores), [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) devuelve false y el escritor puede realizar cualquier procesamiento posterior a la restauración que necesite.

Si se ha llamado a [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) , [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) devuelve **true** y un escritor debe decidir cómo controlar las operaciones posteriores a la restauración; por ejemplo, el escritor puede optar por no actualizar sus datos en el disco.

## <a name="backup-stamps"></a>Marcas de copia de seguridad

Como parte de la operación de copia de seguridad completa anterior, un escritor puede haber almacenado un sello de copia de seguridad en el documento componentes de copia de seguridad del solicitante.

El sello de copia de seguridad se almacena como una cadena, y su formato y la información no son ininteligibles para el solicitante. Por lo tanto, el solicitante no puede hacer uso directo de la información de marca de copia de seguridad.

En su lugar, su tarea consiste en que esa información esté disponible para el escritor, llamando al método [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) antes de la generación de un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para una copia de seguridad incremental.

El solicitante realiza esta función componente por componente. Un solicitante examina la información de marca de copia de seguridad del conjunto de componentes o componentes almacenados mediante [**IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).

Si la información de marca de copia de seguridad es adecuada para el tipo de restauración que está llevando a cabo el solicitante, la pone a disposición de la marca de tiempo de la última copia de seguridad de un componente con el método [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) .

Un escritor recupera la información de marca de la copia de seguridad mediante [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Un escritor de esta clase generó el sello de copia de seguridad inicial, por lo que el escritor puede descodificar esta marca y usar la información. En función de esto, mientras se controla un evento de [**prerestauración**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , un escritor puede optar por realizar acciones como cambiar destinos de restauración o solicitar destinatarios dirigidos.

 

 



