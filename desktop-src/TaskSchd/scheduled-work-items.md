---
title: Elementos de trabajo programados
description: En el Programador de tareas se usan dos términos para describir lo que puede programar elementos de trabajo y tareas.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- Programador de tareas de elementos de trabajo
- Programador de tareas de elementos de trabajo, en comparación con las tareas
- Programador de tareas de tareas
- tareas Programador de tareas, comparación con los elementos de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356935"
---
# <a name="scheduled-work-items"></a>Elementos de trabajo programados

En el Programador de tareas se usan dos términos para describir lo que puede programar: elementos de trabajo y tareas. De estos dos términos, [*elemento de trabajo*](w.md) es un término más general que describe cualquier tipo de elemento que se puede programar. Un *elemento de trabajo* puede ser cualquier elemento que el servicio Programador de tareas se ejecute a la vez que se especifica en los desencadenadores del elemento.

Por el contrario, una [*tarea*](t.md) es un tipo específico de elemento de trabajo. Actualmente, el único tipo de elemento de trabajo programado que se admite es una tarea.

La interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contiene métodos que son compatibles con todos los tipos de elementos de trabajo programados. Por ejemplo, la información de la cuenta, los tiempos de ejecución y los comentarios definidos por la aplicación son propiedades que se pueden aplicar a todos los tipos de elementos de trabajo. Estas propiedades se pueden establecer y recuperar a través de la interfaz **IScheduledWorkItem** .

La interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contiene métodos que solo son compatibles con las tareas.

Los métodos de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) los hereda actualmente la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) y, en el futuro, las heredarán otras interfaces de elementos de trabajo.

| Para obtener ejemplos de                                              | Vea                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Crear una nueva tarea.                                         | [Crear una tarea mediante el ejemplo NewWorkItem](creating-a-task-using-newworkitem-example.md) |
| Ejecutar una tarea existente.                                    | [Ejemplo de inicio de una tarea](starting-a-task-example.md)                                     |
| Recuperando propiedades que se aplican a todos los tipos de elementos de trabajo. | [Recuperar ejemplos de propiedades de elementos de trabajo](retrieving-work-item-property-examples.md)       |
| Establecer las propiedades que se aplican a todos los tipos de elementos de trabajo.    | [Configuración de ejemplos de propiedades de elementos de trabajo](setting-work-item-property-examples.md)             |



 

 

 




