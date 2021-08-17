---
title: Recuperar ejemplos de propiedades de elemento de trabajo
description: Para recuperar las propiedades de un elemento de trabajo, llame a ITaskScheduler Activate para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para recuperar la propiedad de tarea que le interesa.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- recuperar propiedades de elementos de trabajo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3519f3f995e4a5c49a58f0c8be590b34a82381bfd534b61bac6ff8aba05de33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059983"
---
# <a name="retrieving-work-item-property-examples"></a>Recuperar ejemplos de propiedades de elemento de trabajo

Para recuperar las propiedades de un elemento de trabajo, llame a [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para recuperar la propiedad de tarea que le interesa. Actualmente, los únicos elementos de trabajo válidos son las tareas.

Los ejemplos de código que aparecen en la parte inferior de esta página muestran cómo recuperar las propiedades que se aplican a todos los elementos de trabajo. Para otras propiedades que son únicas para las tareas, vea [Establecer ejemplos de propiedades de tarea](setting-task-property-examples.md).

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan después de que ya no sean necesarias.

 

Tenga en cuenta que si va a recuperar una propiedad de cadena (como el comentario de un elemento de trabajo), debe llamar a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.

En el procedimiento siguiente se describe cómo recuperar una propiedad de tarea.

**Para recuperar una propiedad de tarea**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un Programador de tareas objeto . (En estos ejemplos se supone que Programador de tareas servicio está en ejecución).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que las tareas son actualmente el único tipo válido de elemento de trabajo).
3.  Llame al método adecuado para recuperar la propiedad que le interesa.
4.  Procese la propiedad según sea necesario. (Estos ejemplos simplemente imprimen la propiedad en la pantalla).
5.  Si la propiedad devuelta es una cadena, llame a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.



| Para obtener un ejemplo de código de                                                                        | Vea                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Recuperación de la información de cuenta de una tarea conocida                                           | [Ejemplo de código de C/C++: recuperar información de la cuenta de tarea](c-c-code-example-retrieving-task-account-information.md)       |
| Recuperación de la cadena de comentario de una tarea conocida                                                | [Ejemplo de código de C/C++: Recuperar un comentario de tarea](c-c-code-example-retrieving-a-task-comment.md)                           |
| Recuperar el nombre del creador de la tarea y mostrarlo en la pantalla               | [Ejemplo de código de C/C++: Recuperación del creador de tareas](c-c-code-example-retrieving-the-task-creator.md)                       |
| Recuperación del último código de salida devuelto por una tarea conocida                                       | [Ejemplo de código de C/C++: Recuperación del código de salida de la tarea](c-c-code-example-retrieving-task-exit-code.md)                           |
| Recuperar el tiempo de espera de inactividad de la tarea y mostrarlo en la pantalla                    | [Ejemplo de código de C/C++: Recuperación del tiempo de inactividad y espera de la tarea](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| Recuperar la hora de la última ejecución de la tarea y mostrarla en la pantalla                    | [Ejemplo de código de C/C++: Recuperación de la tarea MostRecentRun Time](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| Recuperar la próxima vez que se programa la ejecución de la tarea y mostrar esa hora en la pantalla | [Ejemplo de código de C/C++: Recuperar la tarea NextRun Time](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| Recuperar los tiempos de ejecución de la tarea y mostrarlos en la pantalla                       | [Ejemplo de código de C/C++: recuperar tiempos de ejecución de tareas](c-c-code-example-retrieving-task-run-times.md)                           |
| Recuperar el estado actual de la tarea y mostrarlo en la pantalla                    | [Ejemplo de código de C/C++: Recuperar el estado de la tarea](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 