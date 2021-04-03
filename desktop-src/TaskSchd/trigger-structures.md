---
title: Estructuras de desencadenador para Programador de tareas 1,0
description: Programador de tareas 1,0 utiliza varias estructuras para definir los criterios de un desencadenador.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075854"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>Estructuras de desencadenador para Programador de tareas 1,0

Programador de tareas 1,0 utiliza varias estructuras para definir los criterios de un desencadenador.

> [!Note]  
> Para obtener más información sobre los desencadenadores de Programador de tareas 2,0, consulte [interfaces de desencadenador](trigger-interfaces.md).

 

## <a name="task-scheduler-10-structures"></a>Programador de tareas estructuras 1,0

En la ilustración siguiente se muestra la estructura del [**\_ desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Tiene tres miembros obligatorios (**wBeginYear**, **wBeginMonth** y **wBeginDay**) que se deben establecer al crear un nuevo desencadenador. (Para saltar a la página de referencia de esta estructura, haga clic en el nombre de la estructura en la ilustración).

![estructura del desencadenador de tarea](images/tsktri1.png)

Tenga en cuenta que el miembro **TriggerType** utiliza la enumeración de [**tipo de \_ desencadenador \_ de tarea**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) y el miembro de **tipo** utiliza una estructura de **\_ \_ Unión de desencadenador de tarea** . La enumeración del **\_ \_ tipo de desencadenador de tarea** se usa para especificar el tipo de desencadenador (tipos de desencadenador basados en eventos y tiempos). La estructura de [**\_ \_ Unión de tipo de desencadenador**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) se usa para combinar las estructuras [**Daily**](/windows/desktop/api/Mstask/ns-mstask-daily), [**Weekly**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (Day of month) y [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (Day of Week) que se utilizan para especificar Cuándo se activará un desencadenador basado en el tiempo.

Si **TriggerType** especifica un desencadenador de una vez o un desencadenador basado en eventos, se omite el miembro de **tipo** . La estructura de [**\_ \_ Unión de tipo de desencadenador**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) se usa solo si el miembro **TriggerType** especifica un desencadenador de fecha diaria, semanal, día del mes o mensual.

Además, el valor del miembro de **tipo** indica qué miembro de la estructura [**de \_ \_ Unión del tipo de desencadenador**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) se utiliza. En la ilustración siguiente se muestra la relación entre los valores de la enumeración de [**\_ \_ tipo de desencadenador de tarea**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) y los miembros de la estructura de **estructura de \_ tipo \_ de desencadenador** . (Para saltar a las páginas de referencia de estas estructuras, haga clic en el nombre de la estructura en la ilustración).

![relación entre los valores de enumeración de tipo de desencadenador de tarea y los miembros de la estructura de estructura tipo de desencadenador](images/tsktri3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> <dt>

[Tipos de desencadenador](trigger-types.md)
</dt> <dt>

[Interfaces de desencadenador](trigger-interfaces.md)
</dt> </dl>

 

 




