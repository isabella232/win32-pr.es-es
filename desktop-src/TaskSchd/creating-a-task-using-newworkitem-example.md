---
title: Crear una tarea mediante el ejemplo NewWorkItem
description: Al crear una tarea, usará dos interfaces Programador de tareas ITaskScheduler e ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- crear elementos de trabajo Programador de tareas
- elementos de trabajo Programador de tareas , crear tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d0e0d216c5aaccee6a51cbac939b2b3bfa421338e12d66ffdd3b8cf055862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139588"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Crear una tarea mediante el ejemplo NewWorkItem

Al crear una tarea, usará dos interfaces Programador de tareas: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) e [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). Debe proporcionar un nombre único para la tarea, el identificador de clase del objeto de tarea y el identificador de interfaz de **ITask**. El identificador de clase y el identificador de interfaz se muestran en el ejemplo de código siguiente a este tema.

> [!Note]  
> También puede crear una tarea llamando a [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem). Al realizar esta ruta, es responsabilidad suya crear una instancia del objeto **Task** (que admite la interfaz [**ITask)**](/windows/desktop/api/Mstask/nn-mstask-itask) y, a continuación, agregar la tarea con el nombre que proporcione.

 

> [!Note]  
> De forma predeterminada, solo un miembro del grupo Administradores, Operadores de copia de seguridad o Operadores de servidor puede crear tareas en Windows Server 2003. Un miembro del grupo Administradores puede cambiar el descriptor de seguridad de la carpeta Windows Tarea para permitir que \\ otros usuarios creen tareas.

 

El nombre que proporcione para la tarea debe ser único dentro de la carpeta Tareas programadas. Si ya existe una tarea con el mismo nombre, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) devuelve ERROR \_ FILE \_ EXISTS. Si obtiene este valor devuelto, debe especificar un nombre diferente e intentar crear la tarea de nuevo.

En el procedimiento siguiente se describe cómo crear una nueva tarea de elemento de trabajo.

**Para crear una nueva tarea de elemento de trabajo**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un Programador de tareas objeto. (En este ejemplo se supone que el Programador de tareas se está ejecutando).
2.  Llame [**a ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) para crear una nueva tarea. (Este método devuelve un puntero a una [**interfaz ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)
3.  Guarde la nueva tarea en el disco mediante una [**llamada a IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz COM estándar compatible con la **interfaz ITask).**
4.  Llame **a ITask::Release para** liberar todos los recursos. (Tenga en [**cuenta que Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Para obtener un ejemplo de código de  | Vea                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Creación de una sola tarea | [Ejemplo de código de C/C++: Creación de una tarea mediante NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 