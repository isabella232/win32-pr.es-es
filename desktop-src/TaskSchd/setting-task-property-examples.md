---
title: Configuración de ejemplos de propiedades de tarea
description: Para establecer las propiedades de una tarea, llame a ITaskScheduler activate para recuperar la interfaz del objeto de tarea y, después, llame al método ITask adecuado para establecer la propiedad de tarea que le interese.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- establecer las propiedades de la tarea Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685764"
---
# <a name="setting-task-property-examples"></a>Configuración de ejemplos de propiedades de tarea

Para establecer las propiedades de una tarea, llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar la interfaz del objeto de tarea y, después, llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para establecer la propiedad de tarea que le interese.

Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo establecer las propiedades que son exclusivas de los objetos de tarea. Para otras propiedades de [*elementos de trabajo*](w.md) que también se aplican a las tareas, vea [establecer ejemplos de propiedades de elementos de trabajo](setting-work-item-property-examples.md).

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.

 

En los ejemplos siguientes, el objeto de tarea modificado siempre se guarda en el disco mediante una llamada a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar heredada por el objeto de tarea).

En el procedimiento siguiente se describe cómo establecer una propiedad de tarea.

**Para establecer una propiedad de tarea**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En estos ejemplos se supone que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").
3.  Llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para establecer la propiedad que le interese.
4.  Llame a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para almacenar el objeto de tarea modificado en el disco.



| Para obtener un ejemplo de código de                                                                                                                                | Vea                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Establecer el nombre de la aplicación asociada a una tarea conocida                                                                                     | [Ejemplo de código de C/C++: establecer el nombre de la aplicación](c-c-code-example-setting-application-name.md)   |
| Establecer el tiempo de ejecución máximo de una tarea conocida                                                                                                         | [Ejemplo de código de C/C++: establecer MaxRunTime](c-c-code-example-setting-maxruntime.md)               |
| Borrar todos los parámetros de línea de comandos asociados a una tarea conocida                                                                                    | [Ejemplo de código de C/C++: establecer parámetros de tarea](c-c-code-example-setting-task-parameters.md)     |
| En este ejemplo se establece la prioridad de una tarea de prueba y, a continuación, se guarda la tarea. En este ejemplo se da por supuesto que la tarea de prueba ya existe en el equipo local. | [Ejemplo de código de C/C++: establecer la prioridad de la tarea](c-c-code-example-setting-task-priority.md)         |
| Establecer el [*Directorio de trabajo*](w.md) de una tarea conocida                                                                  | [Ejemplo de código de C/C++: establecer el directorio de trabajo](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 