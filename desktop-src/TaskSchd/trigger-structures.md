---
title: Estructuras de desencadenador para Programador de tareas 1.0
description: Programador de tareas 1.0 usa varias estructuras para definir los criterios de un desencadenador.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891425"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>Estructuras de desencadenador para Programador de tareas 1.0

Programador de tareas 1.0 usa varias estructuras para definir los criterios de un desencadenador.

> [!Note]  
> Para obtener más información sobre Programador de tareas desencadenadores 2.0, vea [Interfaces de desencadenador](trigger-interfaces.md).

 

## <a name="task-scheduler-10-structures"></a>Programador de tareas 1.0 Estructuras

En la ilustración siguiente se muestra la [**estructura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Tiene tres miembros necesarios **(wBeginYear,** **wBeginMonth** y **wBeginDay)** que se deben establecer al crear un nuevo desencadenador. (Para saltar a la página de referencia de esta estructura, haga clic en el nombre de la estructura en la ilustración).

![estructura del desencadenador de tareas](images/tsktri1.png)

Tenga en cuenta que el **miembro TriggerType** usa la enumeración [**TASK TRIGGER \_ \_ TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) y el **miembro Type** usa una estructura TASK TRIGGER **\_ \_ UNION.** La **\_ enumeración TASK TRIGGER \_ TYPE** se usa para especificar el tipo de desencadenador (tipos de desencadenador basados en el tiempo y en eventos). La [**estructura TRIGGER TYPE \_ \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) se usa para combinar las estructuras [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (día del mes) y [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (día de la semana) que se usan para especificar cuándo se activará un desencadenador basado en el tiempo.

Si **TriggerType** especifica un desencadenador basado en un solo tiempo o un desencadenador basado en eventos, se omite el **miembro Type.** La [**estructura TRIGGER TYPE \_ \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) solo se usa si el miembro **TriggerType** especifica un desencadenador diario, semanal, de día del mes o mensual basado en el día de la semana.

Además, el valor del miembro **Type** indica qué miembro de la [**estructura TRIGGER TYPE \_ \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) se usa. En la ilustración siguiente se muestra la relación entre los valores de la enumeración [**TASK \_ TRIGGER \_ TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) y los miembros de la **estructura TRIGGER TYPE \_ \_ STRUCTURE.** (Para saltar a las páginas de referencia de estas estructuras, haga clic en el nombre de la estructura en la ilustración).

![relación entre los valores de enumeración del tipo de desencadenador de tareas y los miembros de la estructura de tipo de desencadenador](images/tsktri3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> <dt>

[Tipos de desencadenador](trigger-types.md)
</dt> <dt>

[Interfaces de desencadenador](trigger-interfaces.md)
</dt> </dl>

 

 




