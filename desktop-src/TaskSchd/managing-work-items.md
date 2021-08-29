---
title: Manipulación de elementos de trabajo
description: La interfaz IScheduledWorkItem proporciona métodos para recuperar y establecer propiedades de elemento de trabajo; crear, recuperar y eliminar desencadenadores para elementos de trabajo (establecer el desencadenador debe realizarse con el método SetTrigger de ITaskTrigger); y para ejecutar, terminar y eliminar el elemento de trabajo. Nota Para las propiedades de un tipo específico de elemento de trabajo, consulte la interfaz para ese tipo de objeto. Por ejemplo, no puede establecer el nivel de prioridad de un elemento de trabajo; sin embargo, puede usar los métodos de la interfaz ITask para recuperar y establecer la prioridad de una tarea.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- elementos de trabajo Programador de tareas , administrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aca2a904391926ae46749d72421fe20fe21932f758dc6e935883c4a2f750c5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517665"
---
# <a name="manipulating-work-items"></a>Manipulación de elementos de trabajo

La [**interfaz IScheduledWorkItem proporciona métodos**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) para recuperar y establecer propiedades de elemento de trabajo; crear, recuperar y eliminar desencadenadores para elementos de trabajo (establecer el desencadenador debe realizarse con el método [**ITaskTrigger::SetTrigger);**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) y para ejecutar, terminar y eliminar el elemento de trabajo.

> [!Note]  
> Para las propiedades de un tipo específico de elemento de trabajo, consulte la interfaz para ese tipo de objeto. Por ejemplo, no puede establecer el nivel de prioridad de un elemento de trabajo; sin embargo, puede usar los métodos de la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) para recuperar y establecer la prioridad de una tarea.

 

Siempre que modifique un elemento de trabajo, debe llamar al objeto [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el elemento de trabajo modificado en el disco. La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz COM estándar que es compatible con la [**interfaz ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)

| Para obtener ejemplos de                                                            | Vea                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Recuperación de propiedades que se aplican a todos los tipos de elementos de trabajo                | [Recuperar ejemplos de propiedades de elemento de trabajo](retrieving-work-item-property-examples.md) |
| Establecimiento de propiedades que se aplican a todos los tipos de elementos de trabajo                   | [Establecer ejemplos de propiedades de elemento de trabajo](setting-work-item-property-examples.md)       |
| Ejecución de una tarea conocida                                                       | [Iniciar un ejemplo de tarea](starting-a-task-example.md)                               |
| Terminación de una tarea en ejecución                                                 | [Terminar un ejemplo de tarea](terminating-a-task-example.md)                         |
| Creación de un desencadenador para una tarea conocida                                    | [Creación de un nuevo desencadenador](creating-a-new-trigger.md)                                 |
| Creación de un desencadenador inactivo basado en eventos para una tarea conocida                      | [Creación de un ejemplo de desencadenador inactivo](creating-an-idle-trigger-example.md)             |
| Recuperación de la cadena de desencadenador de todos los desencadenadores asociados a una tarea conocida | [Ejemplo de recuperación de cadenas de desencadenador](retrieving-trigger-strings-example.md)         |



 

 

 