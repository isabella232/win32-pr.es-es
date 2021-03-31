---
title: Configuración de ejemplos de propiedades de elementos de trabajo
description: Para establecer las propiedades de un elemento de trabajo, llame a ITaskScheduler activate para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para establecer la propiedad de tarea que le interese. Actualmente, los únicos elementos de trabajo válidos son tareas.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- establecer las propiedades de los elementos de trabajo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995470"
---
# <a name="setting-work-item-property-examples"></a>Configuración de ejemplos de propiedades de elementos de trabajo

Para establecer las propiedades de un elemento de trabajo, llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para establecer la propiedad de tarea que le interese. Actualmente, los únicos elementos de trabajo válidos son tareas.

Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo establecer las propiedades que se aplican a todos los elementos de trabajo. Para otras propiedades que son exclusivas de las tareas, consulte Configuración de los [ejemplos de propiedades de tarea](setting-task-property-examples.md).

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.

 

En los ejemplos siguientes, el objeto modificado siempre se guarda en el disco mediante una llamada a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar heredada por el objeto de tarea).

En el procedimiento siguiente se describe cómo establecer una propiedad de tarea.

**Para establecer una propiedad de tarea**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En estos ejemplos se supone que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que las tareas son actualmente el único tipo válido de elemento de trabajo).
3.  Llame al método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) adecuado para establecer la propiedad que le interese. Tenga en cuenta que la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) hereda los métodos **IScheduledWorkItem** .
4.  Llame a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para almacenar el objeto de tarea modificado en el disco.



| Para obtener un ejemplo de código de                            | Vea                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Establecer la información de la cuenta para una tarea conocida | [Ejemplo de código de C/C++: establecer la información de la cuenta de tarea](c-c-code-example-setting-task-account-information.md) |
| Establecer el comentario de una tarea conocida              | [Ejemplo de código de C/C++: establecer comentario de tarea](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 