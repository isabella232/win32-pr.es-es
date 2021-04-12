---
title: Recuperación de ejemplos de propiedades de tarea
description: Para recuperar las propiedades de una tarea, llame a ITaskScheduler activate para obtener la recuperación de la interfaz del objeto de tarea y, a continuación, llame al método ITask adecuado para recuperar la propiedad de tarea que le interesa.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- recuperación de las propiedades de la tarea Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359278"
---
# <a name="retrieving-task-property-examples"></a>Recuperación de ejemplos de propiedades de tarea

Para recuperar las propiedades de una tarea, llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la recuperación de la interfaz del objeto de tarea y, después, llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para recuperar la propiedad de tarea que le interesa. Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo recuperar las distintas propiedades de tarea.

Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo recuperar las propiedades que son exclusivas de los objetos de tarea. Para otras propiedades de [*elementos de trabajo*](w.md) que también se aplican a las tareas, vea [recuperar ejemplos de elementos de trabajo](retrieving-work-item-property-examples.md).

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.

 

Tenga en cuenta que si va a recuperar una propiedad de cadena (como el nombre de la aplicación, los parámetros o el directorio de trabajo), debe llamar a [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.

En el procedimiento siguiente se describe cómo recuperar una propiedad de tarea.

**Para recuperar una propiedad de tarea**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En estos ejemplos se supone que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").
3.  Llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para recuperar la propiedad que le interese.
4.  Procese la propiedad según sea necesario. (Estos ejemplos imprimen la propiedad en la pantalla).
5.  Si la propiedad devuelta es una cadena, llame a [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.



| Para obtener un ejemplo de código de                                                                                                                           | Vea                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Recuperar el nombre de la aplicación asociada a una tarea determinada                                                                             | [Ejemplo de código de C/C++: recuperar el nombre de la aplicación de tarea](c-c-code-example-retrieving-the-task-application-name.md)   |
| Recuperar la cantidad máxima de tiempo que la tarea puede ejecutarse y mostrar ese número en la pantalla                                                 | [Ejemplo de código de C/C++: recuperar la tarea MaxRunTime](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Recuperar la cadena de parámetro que se ejecuta cuando se ejecuta la tarea y mostrar esa cadena en la pantalla                                  | [Ejemplo de código de C/C++: recuperar parámetros de tarea](c-c-code-example-retrieving-task-parameters.md)                       |
| Recuperar el [*nivel de prioridad*](p.md) de la tarea                                                                    | [Ejemplo de código de C/C++: recuperar la prioridad de la tarea](c-c-code-example-retrieving-task-priority.md)                           |
| Recuperar el [*Directorio de trabajo*](w.md) de una tarea y mostrar la ruta de acceso al directorio de trabajo en la pantalla | [Ejemplo de código de C/C++: recuperar el directorio de trabajo de la tarea](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 