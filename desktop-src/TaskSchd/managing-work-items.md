---
title: Manipular elementos de trabajo
description: La interfaz IScheduledWorkItem proporciona métodos para recuperar y establecer las propiedades de los elementos de trabajo. crear, recuperar y eliminar desencadenadores de elementos de trabajo (el establecimiento del desencadenador debe realizarse con el método ITaskTrigger SetTrigger); y para ejecutar, finalizar y eliminar el elemento de trabajo. Nota para las propiedades de un tipo específico de elemento de trabajo, consulte la interfaz para ese tipo de objeto. Por ejemplo, no se puede establecer el nivel de prioridad de un elemento de trabajo; sin embargo, puede usar los métodos de la interfaz ITask para recuperar y establecer la prioridad de una tarea.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- Programador de tareas de elementos de trabajo, administrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792561"
---
# <a name="manipulating-work-items"></a>Manipular elementos de trabajo

La interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) proporciona métodos para recuperar y establecer las propiedades de los elementos de trabajo. crear, recuperar y eliminar desencadenadores de elementos de trabajo (el establecimiento del desencadenador debe realizarse con el método [**ITaskTrigger:: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); y para ejecutar, finalizar y eliminar el elemento de trabajo.

> [!Note]  
> En el caso de las propiedades de un tipo específico de elemento de trabajo, consulte la interfaz para ese tipo de objeto. Por ejemplo, no se puede establecer el nivel de prioridad de un elemento de trabajo; sin embargo, puede usar los métodos de la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) para recuperar y establecer la prioridad de una tarea.

 

Siempre que modifique un elemento de trabajo, debe llamar al objeto [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el elemento de trabajo modificado en el disco. La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar que es compatible con la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .

| Para obtener ejemplos de                                                            | Vea                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Recuperar propiedades que se aplican a todos los tipos de elementos de trabajo                | [Recuperar ejemplos de propiedades de elementos de trabajo](retrieving-work-item-property-examples.md) |
| Establecer propiedades que se aplican a todos los tipos de elementos de trabajo                   | [Configuración de ejemplos de propiedades de elementos de trabajo](setting-work-item-property-examples.md)       |
| Ejecución de una tarea conocida                                                       | [Ejemplo de inicio de una tarea](starting-a-task-example.md)                               |
| Finalizar una tarea en ejecución                                                 | [Ejemplo de finalización de una tarea](terminating-a-task-example.md)                         |
| Crear un nuevo desencadenador para una tarea conocida                                    | [Crear un nuevo desencadenador](creating-a-new-trigger.md)                                 |
| Crear un desencadenador de inactividad basado en eventos para una tarea conocida                      | [Ejemplo de creación de un desencadenador inactivo](creating-an-idle-trigger-example.md)             |
| Recuperar la cadena de desencadenador de todos los desencadenadores asociados a una tarea conocida | [Ejemplo de recuperación de cadenas de desencadenador](retrieving-trigger-strings-example.md)         |



 

 

 