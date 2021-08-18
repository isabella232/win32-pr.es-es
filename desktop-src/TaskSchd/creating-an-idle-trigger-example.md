---
title: Creación de un ejemplo de desencadenador inactivo
description: Para crear un desencadenador inactivo, debe especificar un desencadenador inactivo al crear el desencadenador y debe establecer el tiempo de inactividad de la tarea. Para obtener información sobre las condiciones de inactividad, vea Condiciones de inactividad de tareas.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac38eb3eb7520fde552f009a718fe188d247e3f9fef943f0f0f79ba6ea85970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139548"
---
# <a name="creating-an-idle-trigger-example"></a>Creación de un ejemplo de desencadenador inactivo

Para crear un desencadenador inactivo, debe especificar un desencadenador inactivo al crear el desencadenador y debe establecer el tiempo de inactividad de la tarea. Para obtener información sobre las condiciones de inactividad, vea [Task Idle Conditions](task-idle-conditions.md).

Después de crear el desencadenador inactivo, llame [**a IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el nuevo desencadenador en el disco.

En el procedimiento siguiente se describe cómo crear un desencadenador inactivo para una tarea conocida.

**Para crear un desencadenador inactivo para una tarea conocida**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto. (En este ejemplo se da por supuesto que Programador de tareas servicio está en ejecución).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "Tarea de prueba").
3.  Llame [**a SetIdleWait para**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) establecer cuánto tiempo debe permanecer inactivo el sistema antes de que se active el desencadenador. (Tenga en **cuenta que SetIdleWait** se hereda de [**IScheduledWorkItem).**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)
4.  Defina la [**estructura TASK \_ TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) y llame a [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear el desencadenador inactivo. (Tenga en **cuenta que CreateTrigger** se hereda de [**IScheduledWorkItem).**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)
5.  Guarde la tarea con el nuevo desencadenador inactivo en el disco [**mediante IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz COM estándar compatible con la [**interfaz ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)
6.  Llame **a ITask::Release para** liberar todos los recursos. (Tenga en [**cuenta que Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Para obtener un ejemplo de código de                         | Vea                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Creación de un desencadenador inactivo para una tarea existente | [Ejemplo de código de C/C++: Creación de un desencadenador inactivo](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 