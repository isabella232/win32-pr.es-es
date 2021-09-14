---
title: Establecer ejemplos de propiedades de elemento de trabajo
description: Para establecer las propiedades de un elemento de trabajo, llame a ITaskScheduler Activate para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para establecer la propiedad de tarea que le interesa. Actualmente, los únicos elementos de trabajo válidos son las tareas.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- establecer propiedades de elemento de trabajo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886513"
---
# <a name="setting-work-item-property-examples"></a>Establecer ejemplos de propiedades de elemento de trabajo

Para establecer las propiedades de un elemento de trabajo, llame a [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para establecer la propiedad de tarea que le interesa. Actualmente, los únicos elementos de trabajo válidos son las tareas.

Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo establecer las propiedades que se aplican a todos los elementos de trabajo. Para otras propiedades que son únicas para las tareas, vea [Establecer ejemplos de propiedades de tarea](setting-task-property-examples.md).

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan después de que ya no sean necesarias.

 

En los ejemplos siguientes, el objeto modificado siempre se guarda en el disco mediante una llamada a [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz COM estándar heredada por el objeto de tarea).

En el procedimiento siguiente se describe cómo establecer una propiedad de tarea.

**Para establecer una propiedad de tarea**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto. (En estos ejemplos se supone que Programador de tareas servicio está en ejecución).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que las tareas son actualmente el único tipo válido de elemento de trabajo).
3.  Llame al método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) adecuado para establecer la propiedad que le interesa. Tenga en cuenta que la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) hereda los métodos **IScheduledWorkItem.**
4.  Llame [**a IPersistFile::Save para**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) almacenar el objeto de tarea modificado en el disco.



| Para obtener un ejemplo de código de                            | Vea                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Establecimiento de la información de la cuenta para una tarea conocida | [Ejemplo de código de C/C++: Configuración de la información de la cuenta de tarea](c-c-code-example-setting-task-account-information.md) |
| Establecimiento del comentario de una tarea conocida              | [Ejemplo de código de C/C++: Establecer comentario de tarea](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 