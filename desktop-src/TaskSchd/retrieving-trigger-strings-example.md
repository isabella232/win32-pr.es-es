---
title: Ejemplo de recuperación de cadenas de desencadenador
description: Puede recuperar las cadenas de desencadenador de un desencadenador conocido mediante la interfaz IScheduledWorkItem o ITaskTrigger, en función del tipo de objeto con el que esté trabajando.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- recuperar cadenas de desencadenador Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685762"
---
# <a name="retrieving-trigger-strings-example"></a>Ejemplo de recuperación de cadenas de desencadenador

Puede recuperar las cadenas de desencadenador de un desencadenador conocido mediante la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) o [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , en función del tipo de objeto con el que esté trabajando.

Al trabajar con un [*objeto de tarea*](t.md), use los métodos de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) para recuperar las cadenas de desencadenador de un elemento de trabajo.

Cuando trabaje con un objeto de [*desencadenador de tarea*](t.md), use los métodos de la interfaz [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar la cadena de desencadenador del desencadenador.

En el ejemplo siguiente se muestra cómo usar [**IScheduledWorkItem:: GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) para mostrar las cadenas de todos los desencadenadores asociados a una tarea conocida.

En el procedimiento siguiente se describe cómo recuperar las cadenas de desencadenador de una tarea.

**Para recuperar las cadenas de desencadenador de una tarea**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").
3.  Llame a **ITask:: GetTriggerCount** para averiguar el número de desencadenadores asociados a una tarea. (Tenga en cuenta que [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).
4.  Mostrar las cadenas de desencadenador, llamando a **ITask:: GetTriggerString** para cada desencadenador asociado a la tarea. (Tenga en cuenta que [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).
5.  Libera todos los recursos. Llame a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar las cadenas del desencadenador y **ITask:: Release** para liberar la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . (Tenga en cuenta que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por **ITask**).



| Para obtener un ejemplo de código de                                                         | Vea                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Recuperar una cadena de desencadenador para todos los desencadenadores asociados a una tarea conocida | [Ejemplo de código: recuperar cadenas de desencadenador](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 