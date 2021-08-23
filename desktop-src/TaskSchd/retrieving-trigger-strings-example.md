---
title: Ejemplo de recuperación de cadenas de desencadenador
description: Puede recuperar las cadenas de desencadenador de un desencadenador conocido mediante la interfaz IScheduledWorkItem o ITaskTrigger, en función del tipo de objeto con el que trabaje.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- recuperar cadenas de desencadenador Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a05f95f19aaa68927059c87f7a73f162266454137fbe088923b25dce7ed3ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002383"
---
# <a name="retrieving-trigger-strings-example"></a>Ejemplo de recuperación de cadenas de desencadenador

Puede recuperar las cadenas de desencadenador de un desencadenador conocido mediante la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) o [**ITaskTrigger,**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) en función del tipo de objeto con el que trabaje.

Al trabajar con un [*objeto de tarea*](t.md), use los métodos de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) para recuperar las cadenas de desencadenador de un elemento de trabajo.

Cuando trabaje con un [*objeto*](t.md)de desencadenador de tareas , use los métodos de la interfaz [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar la cadena de desencadenador del desencadenador.

En el ejemplo siguiente se muestra cómo usar [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) para mostrar las cadenas de todos los desencadenadores asociados a una tarea conocida.

En el procedimiento siguiente se describe cómo recuperar las cadenas de desencadenador de una tarea.

**Para recuperar las cadenas de desencadenador de una tarea**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto. (En este ejemplo se da por supuesto que Programador de tareas servicio está en ejecución).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "Tarea de prueba").
3.  Llame **a ITask::GetTriggerCount para** averiguar cuántos desencadenadores están asociados a una tarea. (Tenga en [**cuenta que GetTriggerCount es**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)
4.  Muestre las cadenas de desencadenador, llamando **a ITask::GetTriggerString** para cada desencadenador asociado a la tarea. (Tenga en [**cuenta que GetTriggerString es**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)
5.  Liberar todos los recursos. Llame [**a CoTaskMemFree para**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) liberar las cadenas de desencadenador e **ITask::Release para** liberar la interfaz [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask) (Tenga en [**cuenta que Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por **ITask).**



| Para obtener un ejemplo de código de                                                         | Vea                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Recuperación de una cadena de desencadenador para todos los desencadenadores asociados a una tarea conocida | [Ejemplo de código: Recuperación de cadenas de desencadenador](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 