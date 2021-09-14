---
title: Enumeración de tareas
description: Programador de tareas 1.0 proporciona un objeto de enumeración para enumerar las tareas en la carpeta Tareas programadas.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- enumeración de tareas Programador de tareas
- enumeración de tareas Programador de tareas , descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068664"
---
# <a name="enumerating-tasks"></a>Enumeración de tareas

Programador de tareas 1.0 proporciona un objeto de enumeración para enumerar las tareas en la [*carpeta Tareas programadas*](s.md).

> [!Note]  
> Para un equipo de Windows Server 2003, Windows XP o Windows 2000 para crear, supervisar o controlar tareas en un equipo de Windows Vista, se deben completar ciertas operaciones en el equipo Windows Vista. Para obtener más información, consulte [Tareas](tasks.md).

 

## <a name="using-the-enumeration-object"></a>Usar el objeto de enumeración

La [**interfaz IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) de este objeto proporciona métodos para enumerar las tareas de la carpeta , restablecer la secuencia de enumeración al principio de la lista, omitir tareas y realizar una copia del objeto de enumeración actual para su uso posterior.

Para obtener información sobre cómo enumerar las tareas en la carpeta Scheduled tasks, vea [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).

Para obtener información sobre cómo restablecer la enumeración al principio de la lista, vea [**IEnumWorkItems::Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).

Para obtener información sobre cómo omitir tareas, [**vea IEnumWorkItems::Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).

Para obtener información sobre cómo realizar una copia del objeto de enumeración actual, vea [**IEnumWorkItems::Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).

Para obtener un ejemplo de enumeración de las tareas en la carpeta Scheduled Tasks, vea [Enumerating Tasks Example](enumerating-tasks-example.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Programador de tareas información de la tarea 1.0](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




