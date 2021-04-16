---
description: La selección de la restauración permite que el solicitante determine Cuándo se puede restaurar un componente individualmente.
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: Trabajar con la selección para restaurar y subcomponentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d988f4c4e029c7dd8623ad22fcaee7662d33e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541707"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>Trabajar con la selección para restaurar y subcomponentes

La selección de la restauración permite que el solicitante determine Cuándo se puede restaurar un componente individualmente. Un componente que se ha incluido para la copia de seguridad puede aparecer de una de estas dos maneras:

-   Es posible que un componente se haya [*incluido explícitamente*](vssgloss-e.md) en la copia de seguridad. Estos componentes tienen una instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente en el documento componentes de copia de seguridad. Estos componentes se incluyen en una restauración mediante [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).
-   Es posible que un componente se haya [*incluido implícitamente*](vssgloss-i.md) en la copia de seguridad. Estos componentes no tienen una instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente en el documento componentes de copia de seguridad; sin embargo, siempre habrá una instancia de **IVssComponent** para algún componente antecesor del documento. Estos componentes se incluyen en una restauración mediante [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Cualquier componente que se haya incluido explícitamente en la copia de seguridad siempre se puede seleccionar individualmente para su restauración, independientemente de su valor de selección para restaurar. El solicitante llama a [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), pasando el identificador del escritor, la ruta de acceso lógica y el nombre del componente específico. Los componentes que se han incluido implícitamente en la copia de seguridad se restaurarán cuando se restaure un antecesor incluido explícitamente. Los componentes incluidos implícitamente pueden seleccionarse individualmente para la restauración solo si están marcados como seleccionables para la restauración. El solicitante llama primero a **ivssbackupcomponents:: SetSelectedForRestore** en el componente antecesor incluido explícitamente y, a continuación, llama a [**Ivssbackupcomponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) en el componente antecesor para seleccionar el componente incluido implícitamente para la restauración. Una vez hecho esto, solo se restaurará el componente seleccionado implícitamente; no se restaurarán todos los demás componentes del conjunto de componentes.

A diferencia de la selección de copias de seguridad, que siempre se debe establecer explícitamente cuando se agrega un componente con [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), la selección de la restauración tiene un valor predeterminado de false, que se puede invalidar.

Dado que los componentes de nivel superior (componentes con una ruta de acceso lógica vacía) solo se pueden incluir explícitamente en una copia de seguridad, la selección de la restauración no tiene ningún significado para estos componentes.

 

 



