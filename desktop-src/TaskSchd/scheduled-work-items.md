---
title: Elementos de trabajo programados
description: El Programador de tareas usa dos términos para describir lo que puede programar tareas y elementos de trabajo.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- elementos de trabajo Programador de tareas
- elementos de trabajo Programador de tareas , en comparación con las tareas
- tareas Programador de tareas
- tareas Programador de tareas , en comparación con los elementos de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19455b6d1402439403629aa5f6fca81621571fc90d9e6d8b204e741c5129414
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080438"
---
# <a name="scheduled-work-items"></a>Elementos de trabajo programados

El Programador de tareas usa dos términos para describir lo que puede programar: elementos de trabajo y tareas. De estos dos términos, [*el elemento de trabajo*](w.md) es un término más general que describe cualquier tipo de elemento que se puede programar. Un *elemento de* trabajo puede ser cualquier elemento que Programador de tareas servicio se ejecute a la vez especificado por los desencadenadores del elemento.

Por el contrario, [*una tarea*](t.md) es un tipo específico de elemento de trabajo. Actualmente, el único tipo de elemento de trabajo programado que se admite es una tarea.

La [**interfaz IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contiene métodos que son compatibles con todos los tipos de elementos de trabajo programados. Por ejemplo, la información de la cuenta, los tiempos de ejecución y los comentarios definidos por la aplicación son propiedades que se pueden aplicar a todos los tipos de elementos de trabajo. Estas propiedades se pueden establecer y recuperar a través de la **interfaz IScheduledWorkItem.**

La [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contiene métodos que solo son compatibles con las tareas.

La interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) hereda actualmente los métodos de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) y, en el futuro, los heredarán otras interfaces de elemento de trabajo.

| Para obtener ejemplos de                                              | Vea                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Crear una nueva tarea.                                         | [Crear una tarea mediante el ejemplo NewWorkItem](creating-a-task-using-newworkitem-example.md) |
| Ejecución de una tarea existente.                                    | [Iniciar un ejemplo de tarea](starting-a-task-example.md)                                     |
| Recuperación de propiedades que se aplican a todos los tipos de elementos de trabajo. | [Recuperación de ejemplos de propiedades de elementos de trabajo](retrieving-work-item-property-examples.md)       |
| Establecer propiedades que se aplican a todos los tipos de elementos de trabajo.    | [Establecer ejemplos de propiedades de elemento de trabajo](setting-work-item-property-examples.md)             |



 

 

 




