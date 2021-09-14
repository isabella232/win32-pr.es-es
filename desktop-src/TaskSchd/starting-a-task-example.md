---
title: Iniciar un ejemplo de tarea
description: Para iniciar una tarea, llame al método Run de la interfaz ITask. Run es un método asincrónico que intenta ejecutar la tarea y devuelve en cuanto se inicia la tarea. El Programador de tareas servicio debe ejecutarse correctamente para que este método se ejecute correctamente.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886484"
---
# <a name="starting-a-task-example"></a>Iniciar un ejemplo de tarea

Para iniciar una tarea, llame al [**método Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) de la [**interfaz ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask) **Run** es un método asincrónico que intenta ejecutar la tarea y devuelve en cuanto se inicia la tarea. El Programador de tareas servicio debe ejecutarse correctamente para que este método se ejecute correctamente.

En el procedimiento siguiente se describe cómo iniciar una tarea.

**Para iniciar una tarea**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto. (En este ejemplo se da por supuesto que Programador de tareas servicio está en ejecución).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "Tarea de prueba").
3.  Llame [**a Ejecutar**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) para iniciar la tarea. Tenga en cuenta que la interfaz ITask hereda este [**método.**](/windows/desktop/api/Mstask/nn-mstask-itask)
4.  Continúe el procesamiento según sea necesario.
5.  Llame **a ITask::Release** para liberar recursos y [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para no inicializar COM. En este ejemplo se [**llama a Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar el puntero a la interfaz [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask) (Tenga en **cuenta que Release** es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por **ITask).**



| Para obtener un ejemplo de código de    | Vea                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Ejecución de una tarea existente | [Ejemplo de código de C/C++: Iniciar una tarea](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 