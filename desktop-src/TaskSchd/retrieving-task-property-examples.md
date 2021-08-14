---
title: Recuperar ejemplos de propiedades de tarea
description: Para recuperar las propiedades de una tarea, llame a ITaskScheduler Activate para obtener la interfaz del objeto de tarea y, a continuación, llame al método ITask adecuado para recuperar la propiedad de tarea que le interesa.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- recuperar propiedades de tarea Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e46554c32d9d30941fd837b91e80e8e20d915b0f1c68a665fd72c8f1624c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002393"
---
# <a name="retrieving-task-property-examples"></a>Recuperar ejemplos de propiedades de tarea

Para recuperar las propiedades de una tarea, llame a [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz del objeto de tarea y, a continuación, llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para recuperar la propiedad de tarea que le interesa. Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo recuperar las distintas propiedades de tarea.

Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo recuperar las propiedades que son únicas para los objetos de tarea. Para obtener [*otras propiedades de elemento*](w.md) de trabajo que también se aplican a las tareas, vea [Recuperación de ejemplos de elementos de trabajo](retrieving-work-item-property-examples.md).

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan después de que ya no sean necesarias.

 

Tenga en cuenta que si va a recuperar una propiedad de cadena (como el nombre de la aplicación, los parámetros o el directorio de trabajo), debe llamar a [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.

En el procedimiento siguiente se describe cómo recuperar una propiedad de tarea.

**Para recuperar una propiedad de tarea**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un Programador de tareas objeto . (En estos ejemplos se supone que Programador de tareas servicio está en ejecución).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que este ejemplo obtiene la tarea "Test Task").
3.  Llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para recuperar la propiedad que le interesa.
4.  Procese la propiedad según sea necesario. (Estos ejemplos imprimen la propiedad en la pantalla).
5.  Si la propiedad devuelta es una cadena, llame a [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.



| Para obtener un ejemplo de código de                                                                                                                           | Vea                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Recuperación del nombre de la aplicación asociada a una tarea determinada                                                                             | [Ejemplo de código de C/C++: Recuperar el nombre de la aplicación de tarea](c-c-code-example-retrieving-the-task-application-name.md)   |
| Recuperación de la cantidad máxima de tiempo que la tarea puede ejecutarse y mostrar ese número en la pantalla                                                 | [Ejemplo de código de C/C++: recuperación de la tarea MaxRunTime](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Recuperar la cadena de parámetro que se ejecuta cuando se ejecuta la tarea y mostrar esa cadena en la pantalla                                  | [Ejemplo de código de C/C++: Recuperar parámetros de tarea](c-c-code-example-retrieving-task-parameters.md)                       |
| Recuperación del [*nivel de prioridad*](p.md) de la tarea                                                                    | [Ejemplo de código de C/C++: Recuperar prioridad de tarea](c-c-code-example-retrieving-task-priority.md)                           |
| Recuperar el directorio [*de trabajo*](w.md) de una tarea y mostrar la ruta de acceso al directorio de trabajo en la pantalla | [Ejemplo de código de C/C++: recuperar el directorio de trabajo de la tarea](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 