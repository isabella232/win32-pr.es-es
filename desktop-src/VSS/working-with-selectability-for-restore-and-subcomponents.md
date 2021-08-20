---
description: La capacidad de selección para la restauración permite al solicitante determinar cuándo se puede restaurar individualmente un componente.
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: Trabajar con selectability for restore y subcomponentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1186c9517af8e7e7b914b9508e10a2b4c8d1961afdbf6d68c2dadcede58c4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937386"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>Trabajar con selectability for restore y subcomponentes

La capacidad de selección para la restauración permite al solicitante determinar cuándo se puede restaurar individualmente un componente. Un componente que se ha incluido para la copia de seguridad puede aparecer de una de estas dos maneras:

-   Es posible que un componente se [*haya incluido explícitamente*](vssgloss-e.md) en la copia de seguridad. Estos componentes tienen una instancia [**de IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente en el documento Componentes de copia de seguridad. Estos componentes se incluyen en una restauración [**mediante IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).
-   Es posible que un componente se haya [*incluido implícitamente*](vssgloss-i.md) en la copia de seguridad. Estos componentes no tienen una instancia [**de IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente en el documento Componentes de copia de seguridad; sin embargo, siempre habrá una instancia **de IVssComponent** para algún componente antecesor en el documento. Estos componentes se incluyen en una restauración mediante [**IVssBackupComponents::AddRestoreSubcomponent.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)

Cualquier componente que se haya incluido explícitamente en la copia de seguridad siempre se puede seleccionar individualmente para la restauración, independientemente de su valor de capacidad de selección para la restauración. El solicitante llama a [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), pasando el identificador del escritor, la ruta de acceso lógica y el nombre del componente específico. Los componentes que se han incluido implícitamente en la copia de seguridad se restaurarán cuando se restaure un antecesor incluido explícitamente. Los componentes incluidos implícitamente solo se pueden seleccionar individualmente para la restauración si están marcados como seleccionables para la restauración. El solicitante llama primero **a IVssBackupComponents::SetSelectedForRestore** en el componente antecesor incluido explícitamente más cercano y, a continuación, llama a [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) en el componente antecesor para seleccionar el componente incluido implícitamente para la restauración. Una vez hecho esto, solo se restaurará el componente seleccionado implícitamente; no se restaurarán todos los demás componentes del conjunto de componentes.

A diferencia de la capacidad de selección para la copia de seguridad, que siempre se debe establecer explícitamente cuando se agrega un componente con [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), la capacidad de selección para la restauración tiene un valor predeterminado de false, que se puede invalidar.

Dado que los componentes de nivel superior (componentes con una ruta de acceso lógica vacía) solo se pueden incluir explícitamente en una copia de seguridad, la capacidad de selección para la restauración no tiene ningún significado para estos componentes.

 

 



