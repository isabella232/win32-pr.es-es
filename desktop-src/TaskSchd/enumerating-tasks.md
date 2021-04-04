---
title: Enumerar tareas
description: Programador de tareas 1,0 proporciona un objeto de enumeración para enumerar las tareas de la carpeta tareas programadas.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- enumerar tareas Programador de tareas
- enumerar tareas Programador de tareas, descritas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076017"
---
# <a name="enumerating-tasks"></a>Enumerar tareas

Programador de tareas 1,0 proporciona un objeto de enumeración para enumerar las tareas de la [*carpeta tareas programadas*](s.md).

> [!Note]  
> Para un equipo con Windows Server 2003, Windows XP o Windows 2000 para crear, supervisar o controlar tareas en un equipo con Windows Vista, se deben completar ciertas operaciones en el equipo de Windows Vista. Para obtener más información, consulte [Tareas](tasks.md).

 

## <a name="using-the-enumeration-object"></a>Usar el objeto de enumeración

La interfaz [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) de este objeto proporciona métodos para enumerar las tareas de la carpeta, restablecer la secuencia de enumeración al principio de la lista, omitir las tareas y realizar una copia del objeto de enumeración actual para su uso posterior.

Para obtener información sobre cómo enumerar las tareas en la carpeta tareas programadas, vea [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).

Para obtener información sobre cómo restablecer la enumeración al principio de la lista, vea [**IEnumWorkItems:: RESET**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).

Para obtener información sobre cómo omitir las tareas, vea [**IEnumWorkItems:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).

Para obtener información sobre cómo crear una copia del objeto de enumeración actual, vea [**IEnumWorkItems:: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).

Para obtener un ejemplo de cómo enumerar las tareas de la carpeta tareas programadas, vea [ejemplo de enumeración de tareas](enumerating-tasks-example.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Programador de tareas información de la tarea 1,0](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




