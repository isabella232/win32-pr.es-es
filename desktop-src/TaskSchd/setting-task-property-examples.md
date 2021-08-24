---
title: Ejemplos de propiedades de tarea de configuración
description: Para establecer las propiedades de una tarea, llame a ITaskScheduler Activate para recuperar la interfaz del objeto de tarea y, a continuación, llame al método ITask adecuado para establecer la propiedad de tarea que le interesa.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- establecer propiedades de tarea Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deac57ac28a16108eb886cc56cf697cd768ca7d2e351c4517728c2972be8582f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681635"
---
# <a name="setting-task-property-examples"></a>Ejemplos de propiedades de tarea de configuración

Para establecer las propiedades de una tarea, llame a [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar la interfaz del objeto de tarea y, a continuación, llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para establecer la propiedad de tarea que le interesa.

Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo establecer las propiedades que son únicas para los objetos de tarea. Para ver [*otras propiedades de elementos*](w.md) de trabajo que también se aplican a tareas, vea [Establecer ejemplos de propiedades de elemento de trabajo.](setting-work-item-property-examples.md)

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan después de que ya no sean necesarias.

 

En los ejemplos siguientes, el objeto de tarea modificado siempre se guarda en el disco mediante una llamada a [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz COM estándar heredada por el objeto de tarea).

En el procedimiento siguiente se describe cómo establecer una propiedad de tarea.

**Para establecer una propiedad de tarea**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto. (En estos ejemplos se supone que el Programador de tareas se está ejecutando).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "Tarea de prueba").
3.  Llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para establecer la propiedad que le interesa.
4.  Llame [**a IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para almacenar el objeto de tarea modificado en el disco.



| Para obtener un ejemplo de código de                                                                                                                                | Vea                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Establecimiento del nombre de la aplicación asociada a una tarea conocida                                                                                     | [Ejemplo de código de C/C++: Establecer el nombre de la aplicación](c-c-code-example-setting-application-name.md)   |
| Establecimiento del tiempo de ejecución máximo de una tarea conocida                                                                                                         | [Ejemplo de código de C/C++: configuración de MaxRunTime](c-c-code-example-setting-maxruntime.md)               |
| Borrar todos los parámetros de línea de comandos asociados a una tarea conocida                                                                                    | [Ejemplo de código de C/C++: Establecer parámetros de tarea](c-c-code-example-setting-task-parameters.md)     |
| En este ejemplo se establece la prioridad de una tarea de prueba y, a continuación, se guarda la tarea. En este ejemplo se supone que la tarea de prueba ya existe en el equipo local. | [Ejemplo de código de C/C++: establecer la prioridad de la tarea](c-c-code-example-setting-task-priority.md)         |
| Establecimiento del [*directorio de trabajo*](w.md) de una tarea conocida                                                                  | [Ejemplo de código de C/C++: configuración del directorio de trabajo](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 