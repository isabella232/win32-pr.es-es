---
title: Edición de un elemento de trabajo mediante páginas de propiedades
description: Puede editar las propiedades de un elemento de trabajo mediante la interfaz gráfica de usuario proporcionada por Programador de tareas Service.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- editar elementos de trabajo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0121a9e3100922ecdd1d529aa81b498d377724959abb5c3380337df82817e338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100435"
---
# <a name="editing-a-work-item-using-property-pages"></a>Edición de un elemento de trabajo mediante páginas de propiedades

Puede editar las propiedades de un elemento de trabajo mediante la interfaz gráfica de usuario proporcionada por Programador de tareas Service. (Actualmente, los únicos elementos de trabajo válidos son las tareas).

En el procedimiento siguiente se describe cómo editar una tarea mediante sus páginas de propiedades.

**Para editar una tarea mediante sus páginas de propiedades**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto. (En estos ejemplos se supone que el Programador de tareas se está ejecutando).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que las tareas son actualmente el único tipo válido de elemento de trabajo).
3.  Llame [**a IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) para mostrar las páginas de propiedades de la tarea.
4.  Edite las propiedades de la tarea según sea necesario y haga clic en Aceptar para aceptar los nuevos valores y quitar las páginas de propiedades mostradas.



| Para obtener un ejemplo de código de                                                                                      | Vea                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Mostrar las páginas de propiedades de una tarea conocida y permitir que un usuario edite las propiedades del elemento de trabajo | [Ejemplo de código de C/C++: Edición de un elemento de trabajo](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 