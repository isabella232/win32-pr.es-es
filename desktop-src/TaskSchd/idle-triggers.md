---
title: Desencadenadores inactivos para Programador de tareas 1,0
description: Un desencadenador inactivo es un desencadenador basado en eventos que se desencadena un número específico de veces después de que el equipo se vuelva inactivo. Hay varias condiciones que definen Cuándo un equipo pasa a estar inactivo, como cuando no se produce ninguna entrada de teclado o de mouse.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685510"
---
# <a name="idle-triggers-for-task-scheduler-10"></a>Desencadenadores inactivos para Programador de tareas 1,0

Un desencadenador inactivo es un desencadenador basado en eventos que se desencadena un número específico de veces después de que el equipo se vuelva inactivo. Hay varias condiciones que definen Cuándo un equipo pasa a estar inactivo, como cuando no se produce ninguna entrada de teclado o de mouse.

Los desencadenadores inactivos se crean especificando \_ el desencadenador de evento de tarea \_ \_ en \_ inactivo en el miembro de [**\_ \_ tipo de desencadenador**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) de tarea de la estructura del [**\_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea. El desencadenador idle se activa cuando el sistema se queda inactivo durante el período de tiempo especificado por el tiempo de espera de inactividad del elemento de trabajo.

> [!Note]  
> Cuando \_ \_ se especifica desencadenador de evento \_ de tarea en \_ inactivo, se omiten los miembros **wStartHour**, **wStartMinute** y **Type** de la estructura del [**\_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea.

 

Puede establecer el tiempo de espera de inactividad de un elemento de trabajo llamando al método [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) . Este método establece la cantidad de tiempo (en minutos) que el sistema debe permanecer inactivo antes de que se active el desencadenador y se ejecute el elemento de trabajo.

Para recuperar el tiempo de inactividad de una tarea, llame al método [**IScheduledWorkItem:: GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> </dl>

 

 




