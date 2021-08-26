---
title: Creación de un nuevo desencadenador
description: Para crear un desencadenador, debe usar tres interfaces.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0111fe8c45fdac5618407500b2168bf09c4ec01c5d68e78342f14d6bf103ff78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100445"
---
# <a name="creating-a-new-trigger"></a>Creación de un nuevo desencadenador

Para crear un desencadenador, debe usar tres interfaces. [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) proporciona el método [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear el objeto desencadenador, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) proporciona el método [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para establecer los criterios para el desencadenador y la interfaz COM [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) proporciona un método **Save** para guardar el nuevo desencadenador en el disco.

En el procedimiento siguiente se describe cómo crear un nuevo desencadenador.

**Para crear un nuevo desencadenador**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un Programador de tareas objeto . (En este ejemplo se supone que el Programador de tareas se está ejecutando).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que este ejemplo obtiene la tarea "Test Task").
3.  Llame [**a CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear un objeto desencadenador. (Tenga en [**cuenta que CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) se hereda de [**IScheduledWorkItem).**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)
4.  Defina una [**estructura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Tenga en cuenta que los miembros wBeginDay, wBeginMonth y wBeginYear de **TASK \_ TRIGGER** deben establecerse en un día, mes y año válidos, respectivamente.
5.  Llame [**a ITaskTrigger::SetTrigger para**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) establecer los criterios del desencadenador.
6.  Guarde la tarea con el nuevo desencadenador en el disco [**mediante IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz COM estándar compatible con la [**interfaz ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)
7.  Llame [**a Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar todos los recursos. (Tenga en **cuenta que Release** es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Para obtener un ejemplo de código de                       | Vea                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Creación de un desencadenador para una tarea existente | [Ejemplo de código de C/C++: Creación de un desencadenador de tareas](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 