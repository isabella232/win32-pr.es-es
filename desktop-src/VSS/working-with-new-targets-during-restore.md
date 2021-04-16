---
description: Es posible que un solicitante tenga que restaurar archivos en una ubicación indicada por algo distinto de la ruta de acceso predeterminada de un conjunto de archivos o su asignación de ubicación alternativa.
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: Trabajar con nuevos destinos durante la restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f20a6e8c27c186648d0f662921160ab5c76988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696431"
---
# <a name="working-with-new-targets-during-restore"></a>Trabajar con nuevos destinos durante la restauración

Es posible que un solicitante tenga que restaurar archivos en una ubicación indicada por algo distinto de la ruta de acceso predeterminada de un conjunto de archivos o su [*asignación de ubicación alternativa*](vssgloss-a.md). Hay muchas razones por las que esto puede ocurrir, por ejemplo, no se puede tener acceso a ningún destino de restauración, o un usuario solicitante solicita intencionadamente que los archivos se restauren en alguna ubicación desconocida previamente. En este caso, el solicitante usa el nuevo mecanismo de destino para indicar a los escritores que ha restaurado un archivo en un área diferente en el disco.

No todos los escritores admiten que un solicitante cambie el destino de restauración de un archivo. Un solicitante debe comprobar la compatibilidad del escritor comprobando la máscara del esquema de copia de seguridad del escritor (devuelta por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)) y comprobando que contiene el escritor de VSS \_ BS \_ \_ es compatible con la \_ nueva \_ marca de destino.

El solicitante indica una restauración de este tipo mediante el método [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) . Además de especificar una especificación de archivo y un destino de restauración nuevo y original, el solicitante especifica la información del componente, una ruta de acceso lógica y un nombre de componente.

La información del componente que se usa depende de si el componente que administra el archivo que tiene un nuevo destino agregado se [*incluyó explícitamente*](vssgloss-e.md) o se [*incluyó implícitamente*](vssgloss-i.md) en la copia de seguridad.

Si el componente de administración se incluyó explícitamente, se usa su información. Si el componente de administración se incluyó implícitamente, es un subcomponente de un conjunto de componentes. En este caso, se usa la información del componente de definición del conjunto de componentes.

Al controlar el evento [**Postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , los escritores deben comprobar si alguno de sus archivos se restauró en una nueva ubicación. Esto se puede hacer mediante los métodos [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) y [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) .

La instancia de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que se usa depende de si el componente de administración del archivo se ha agregado explícita o implícitamente a la copia de seguridad.

 

 



