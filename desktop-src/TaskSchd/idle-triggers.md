---
title: Desencadenadores inactivos para Programador de tareas 1.0
description: Un desencadenador inactivo es un desencadenador basado en eventos que se desencadena un número específico de veces después de que el equipo se vuelve inactivo. Hay varias condiciones que definen cuándo un equipo se vuelve inactivo, como cuando no se produce ninguna entrada de teclado o mouse.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349b6ce078479df841773661bfe07b098f95d1124a68803b8b472b226d9b5df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760091"
---
# <a name="idle-triggers-for-task-scheduler-10"></a>Desencadenadores inactivos para Programador de tareas 1.0

Un desencadenador inactivo es un desencadenador basado en eventos que se desencadena un número específico de veces después de que el equipo se vuelve inactivo. Hay varias condiciones que definen cuándo un equipo se vuelve inactivo, como cuando no se produce ninguna entrada de teclado o mouse.

Los desencadenadores inactivos se crean especificando TASK \_ EVENT TRIGGER ON IDLE en el miembro TASK TRIGGER \_ \_ \_ [**\_ \_ TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) de la [**estructura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) El desencadenador de inactividad se desencadena cuando el sistema pasa a estar inactivo durante el tiempo especificado por el tiempo de espera de inactividad del elemento de trabajo.

> [!Note]  
> Cuando se especifica TASK EVENT TRIGGER ON IDLE, se omiten los miembros \_ \_ \_ \_ **wStartHour**, **wStartMinute**  [**\_**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) y Type de la estructura TASK TRIGGER.

 

Puede establecer el tiempo de espera de inactividad de un elemento de trabajo llamando al [**método IScheduledWorkItem::SetIdleWait.**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) Este método establece la cantidad de tiempo (en minutos) que el sistema debe permanecer inactivo antes de que se desencadene el desencadenador y se ejecute el elemento de trabajo.

Para recuperar el tiempo de inactividad de una tarea, llame al [**método IScheduledWorkItem::GetIdleWait.**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> </dl>

 

 




