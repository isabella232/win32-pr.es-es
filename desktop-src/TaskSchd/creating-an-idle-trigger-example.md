---
title: Ejemplo de creación de un desencadenador inactivo
description: Para crear un desencadenador inactivo, debe especificar un desencadenador de inactividad al crear el desencadenador y debe establecer el tiempo de inactividad de la tarea. Para obtener información sobre las condiciones de inactividad, consulte condiciones de inactividad de tareas.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359237"
---
# <a name="creating-an-idle-trigger-example"></a>Ejemplo de creación de un desencadenador inactivo

Para crear un desencadenador inactivo, debe especificar un desencadenador de inactividad al crear el desencadenador y debe establecer el tiempo de inactividad de la tarea. Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).

Después de crear el desencadenador Idle, llame a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el nuevo desencadenador en el disco.

En el procedimiento siguiente se describe cómo crear un desencadenador inactivo para una tarea conocida.

**Para crear un desencadenador inactivo para una tarea conocida**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").
3.  Llame a [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) para establecer cuánto tiempo debe permanecer inactivo el sistema antes de que se active el desencadenador. (Tenga en cuenta que **SetIdleWait** se hereda de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).
4.  Defina la estructura del [**\_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea y llame a [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear el desencadenador inactivo. (Tenga en cuenta que **CreateTrigger** se hereda de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).
5.  Guarde la tarea con el nuevo desencadenador de inactividad en el disco mediante [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar compatible con la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ).
6.  Llame a **ITask:: Release** para liberar todos los recursos. (Tenga en cuenta que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).



| Para obtener un ejemplo de código de                         | Vea                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Crear un desencadenador inactivo para una tarea existente | [Ejemplo de código de C/C++: creación de un desencadenador inactivo](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 