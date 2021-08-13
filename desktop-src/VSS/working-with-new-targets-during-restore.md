---
description: Es posible que un solicitante tenga que restaurar los archivos en una ubicación indicada por algo distinto de la ruta de acceso predeterminada de un conjunto de archivos o su asignación de ubicación alternativa.
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: Trabajar con nuevos destinos durante la restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f7b9a614b043a423dd90868b0a66b505ee194ef968daed4952b0ba60fec6b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590469"
---
# <a name="working-with-new-targets-during-restore"></a>Trabajar con nuevos destinos durante la restauración

Es posible que un solicitante tenga que restaurar los archivos en una ubicación indicada por algo distinto de la ruta de acceso predeterminada de un conjunto de archivos o su [*asignación de ubicación alternativa.*](vssgloss-a.md) Hay muchas razones por las que esto podría ocurrir, por ejemplo, que no se pudo acceder al destino de restauración o que un usuario solicitante solicita intencionadamente que los archivos se restaures en una ubicación desconocida previamente. En este caso, el solicitante usa el nuevo mecanismo de destino para indicar a los escritores que ha restaurado un archivo en un área diferente del disco.

No todos los escritores admiten que un solicitante cambie el destino de restauración de un archivo. Un solicitante debe comprobar la compatibilidad con el escritor comprobando la máscara de esquema de copia de seguridad del escritor (devuelta por [**IVssExgvWriterMetadata::GetBackupSchema)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)y comprobando que contiene la marca VSS \_ BS \_ WRITER SUPPORTS NEW \_ \_ \_ TARGET.

El solicitante indica este tipo de restauración a través [**del método IVssBackupComponents::AddNewTarget.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) Además de especificar una especificación de archivo y un destino de restauración original y un nuevo destino de restauración, el solicitante especifica la información del componente: una ruta de acceso lógica y un nombre de componente.

La información del componente que se usa depende de si el componente [](vssgloss-e.md) que administra el archivo con un nuevo destino agregado se incluyó explícitamente o se incluyó [*implícitamente*](vssgloss-i.md) en la copia de seguridad.

Si el componente de administración se incluyó explícitamente, se usa su información. Si el componente de administración se incluyó implícitamente, es un subcomponente en un conjunto de componentes. En este caso, se usa la información del componente de definición del conjunto de componentes.

Al controlar el [**evento PostRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) los escritores deben comprobar si alguno de sus archivos se restauró en una nueva ubicación. Esto se puede hacer mediante los [**métodos IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) [**e IVssComponent::GetNewTarget.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

La instancia de la [**interfaz IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que se usa depende de si el componente de administración del archivo se agregó explícita o implícitamente a la copia de seguridad.

 

 



