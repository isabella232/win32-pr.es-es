---
title: Crear un nuevo desencadenador
description: Para crear un desencadenador, debe usar tres interfaces.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421076"
---
# <a name="creating-a-new-trigger"></a>Crear un nuevo desencadenador

Para crear un desencadenador, debe usar tres interfaces. [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) proporciona el método [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear el objeto de desencadenador, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) proporciona el método [**ITaskTrigger:: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para establecer los criterios del desencadenador y la interfaz com [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) proporciona un método para **Guardar** el nuevo desencadenador en el disco.

En el procedimiento siguiente se describe cómo crear un nuevo desencadenador.

**Para crear un nuevo desencadenador**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").
3.  Llame a [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear un objeto desencadenador. (Tenga en cuenta que [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) se hereda de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).
4.  Defina una estructura de [**\_ desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Tenga en cuenta que los miembros wBeginDay, wBeginMonth y wBeginYear del **\_ desencadenador de tarea** deben establecerse en un día, un mes y un año válidos, respectivamente.
5.  Llame a [**ITaskTrigger:: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para establecer los criterios del desencadenador.
6.  Guarde la tarea con el nuevo desencadenador en el disco mediante [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar compatible con la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ).
7.  Llame a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar todos los recursos. (Tenga en cuenta que **Release** es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).



| Para obtener un ejemplo de código de                       | Vea                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Crear un nuevo desencadenador para una tarea existente | [Ejemplo de código de C/C++: creación de un desencadenador de tarea](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 