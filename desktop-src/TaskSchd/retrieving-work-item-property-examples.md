---
title: Recuperar ejemplos de propiedades de elementos de trabajo
description: Para recuperar las propiedades de un elemento de trabajo, llame a ITaskScheduler activate para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para recuperar la propiedad de tarea que le interesa.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- recuperando propiedades de elementos de trabajo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a51c623301a4a3b53369713abe95ea1dafba80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420988"
---
# <a name="retrieving-work-item-property-examples"></a>Recuperar ejemplos de propiedades de elementos de trabajo

Para recuperar las propiedades de un elemento de trabajo, llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para recuperar la propiedad de tarea que le interese. Actualmente, los únicos elementos de trabajo válidos son tareas.

Los ejemplos de código que aparecen en la parte inferior de esta página muestran cómo recuperar las propiedades que se aplican a todos los elementos de trabajo. Para otras propiedades que son exclusivas de las tareas, consulte Configuración de los [ejemplos de propiedades de tarea](setting-task-property-examples.md).

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.

 

Tenga en cuenta que si va a recuperar una propiedad de cadena (como comentario para un elemento de trabajo), debe llamar a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.

En el procedimiento siguiente se describe cómo recuperar una propiedad de tarea.

**Para recuperar una propiedad de tarea**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En estos ejemplos se supone que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que las tareas son actualmente el único tipo válido de elemento de trabajo).
3.  Llame al método adecuado para recuperar la propiedad que le interese.
4.  Procese la propiedad según sea necesario. (Estos ejemplos simplemente imprimen la propiedad en la pantalla).
5.  Si la propiedad devuelta es una cadena, llame a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.



| Para obtener un ejemplo de código de                                                                        | Vea                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Recuperar la información de la cuenta de una tarea conocida                                           | [Ejemplo de código de C/C++: recuperar información de la cuenta de tarea](c-c-code-example-retrieving-task-account-information.md)       |
| Recuperar la cadena de comentario de una tarea conocida                                                | [Ejemplo de código de C/C++: recuperar un Comentario de tarea](c-c-code-example-retrieving-a-task-comment.md)                           |
| Recuperar el nombre del creador de la tarea y mostrarla en la pantalla               | [Ejemplo de código de C/C++: recuperar el creador de la tarea](c-c-code-example-retrieving-the-task-creator.md)                       |
| Recuperar el último código de salida devuelto por una tarea conocida                                       | [Ejemplo de código de C/C++: recuperar el código de salida de la tarea](c-c-code-example-retrieving-task-exit-code.md)                           |
| Recuperar el tiempo de espera de inactividad de la tarea y mostrarlo en la pantalla                    | [Ejemplo de código de C/C++: recuperar el tiempo de espera de inactividad de la tarea](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| Recuperar la hora en que se ejecutó la tarea por última vez y mostrarla en la pantalla                    | [Ejemplo de código de C/C++: recuperar la hora de MostRecentRun de la tarea](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| Recuperar la próxima vez que se programa la ejecución de la tarea y mostrar esa hora en la pantalla | [Ejemplo de código de C/C++: recuperar la hora de NextRun de la tarea](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| Recuperar los tiempos de ejecución de la tarea y mostrarlos en la pantalla                       | [Ejemplo de código de C/C++: recuperar los tiempos de ejecución de la tarea](c-c-code-example-retrieving-task-run-times.md)                           |
| Recuperar el estado actual de la tarea y mostrarla en la pantalla                    | [Ejemplo de código de C/C++: recuperar el estado de la tarea](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 