---
title: Ejemplo de la recuperación de una página de tareas
description: Para recuperar una página de tareas, debe llamar a ITask QueryInterface para recuperar la interfaz IProvideTaskPage y, a continuación, llamar a IProvideTaskPage GetPage. El método GetPage devuelve un identificador a la página, que se puede usar para mostrar la página solicitada.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- recuperar la página de tareas Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d619f76b4de416fe2bef9faa679851c613df05e427d6203a6a91936644ad07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872275"
---
# <a name="retrieving-a-task-page-example"></a>Ejemplo de la recuperación de una página de tareas

Para recuperar una página de tareas, debe llamar a **ITask::QueryInterface** para recuperar la interfaz [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) y, a continuación, llamar a [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage). El **método GetPage** devuelve un identificador a la página, que se puede usar para mostrar la página solicitada.

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan después de que ya no sean necesarias.

 

En el procedimiento siguiente se describe cómo crear un nuevo desencadenador.

**Para crear un nuevo desencadenador**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto. (En este ejemplo se da por supuesto que Programador de tareas servicio está en ejecución).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "Tarea de prueba").
3.  Llame **a ITask::QueryInterface** para recuperar la interfaz [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) y [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) para recuperar la página.
4.  Con el identificador de página devuelto, muestre la página.



| Para obtener un ejemplo de código de                                   | Vea                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Recuperar y mostrar la página Tarea de una tarea conocida | [Recuperar una página de tareas](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 