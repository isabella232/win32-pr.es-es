---
title: Crear una tarea mediante el ejemplo NewWorkItem
description: Al crear una tarea, usará dos interfaces Programador de tareas ITaskScheduler y ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- crear elementos de trabajo Programador de tareas
- Programador de tareas de elementos de trabajo, crear tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359202"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Crear una tarea mediante el ejemplo NewWorkItem

Al crear una tarea, usará dos interfaces Programador de tareas: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) y [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). Debe proporcionar un nombre único para la tarea, el identificador de clase del objeto de tarea y el identificador de interfaz de **ITask**. El identificador de clase y el identificador de interfaz se muestran en el ejemplo de código que aparece a continuación de este tema.

> [!Note]  
> También puede crear una tarea mediante una llamada a [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem). Al realizar esta ruta, es su responsabilidad crear una instancia del objeto de **tarea** (que admite la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ) y, a continuación, agregar la tarea con el nombre que proporcione.

 

> [!Note]  
> De forma predeterminada, solo un miembro del grupo administradores, operadores de copia de seguridad o operadores de servidor puede crear tareas en Windows Server 2003. Un miembro del grupo administradores puede cambiar el descriptor de seguridad de la \\ carpeta de tareas de Windows para permitir que otros usuarios creen tareas.

 

El nombre que proporcione para la tarea debe ser único en la carpeta tareas programadas. Si ya existe una tarea con el mismo nombre, [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) devuelve el \_ archivo de error \_ . Si obtiene este valor devuelto, debe especificar un nombre diferente e intentar crear la tarea de nuevo.

En el procedimiento siguiente se describe cómo crear una nueva tarea de elemento de trabajo.

**Para crear una nueva tarea de elemento de trabajo**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) para crear una nueva tarea. (Este método devuelve un puntero a una interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ).
3.  Guarde la nueva tarea en el disco llamando a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar compatible con la interfaz **ITask** ).
4.  Llame a **ITask:: Release** para liberar todos los recursos. (Tenga en cuenta que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).



| Para obtener un ejemplo de código de  | Vea                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Crear una única tarea | [Ejemplo de código de C/C++: crear una tarea mediante NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 