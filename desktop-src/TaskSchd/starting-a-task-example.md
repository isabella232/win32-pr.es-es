---
title: Ejemplo de inicio de una tarea
description: Para iniciar una tarea, llame al método Run de la interfaz ITask. Run es un método asincrónico que intenta ejecutar la tarea y vuelve en cuanto se inicia la tarea. El servicio de Programador de tareas debe estar en ejecución para que este método se ejecute correctamente.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685779"
---
# <a name="starting-a-task-example"></a>Ejemplo de inicio de una tarea

Para iniciar una tarea, llame al método [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) de la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . **Run** es un método asincrónico que intenta ejecutar la tarea y vuelve en cuanto se inicia la tarea. El servicio de Programador de tareas debe estar en ejecución para que este método se ejecute correctamente.

En el procedimiento siguiente se describe cómo iniciar una tarea.

**Para iniciar una tarea**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").
3.  Llame a [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) para iniciar la tarea. Tenga en cuenta que este método es heredado por la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
4.  Continúe el procesamiento según sea necesario.
5.  Llame a **ITask:: Release** para liberar los recursos y [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para anular la inicialización de com. En este ejemplo se llama a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar el puntero a la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . (Tenga en cuenta que **Release** es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por **ITask**).



| Para obtener un ejemplo de código de    | Vea                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Ejecutar una tarea existente | [Ejemplo de código de C/C++: iniciar una tarea](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 