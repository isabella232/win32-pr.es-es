---
title: Ejemplo de recuperación de una página de tareas
description: Para recuperar una página de tareas, debe llamar a ITask QueryInterface para recuperar la interfaz IProvideTaskPage y, a continuación, llamar a IProvideTaskPage GetPage. El método GetPage devuelve un identificador a la página, que se puede usar para mostrar la página solicitada.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- recuperando Programador de tareas de página de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077919"
---
# <a name="retrieving-a-task-page-example"></a>Ejemplo de recuperación de una página de tareas

Para recuperar una página de tareas, debe llamar a **ITask:: QueryInterface** para recuperar la interfaz [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) y, a continuación, llamar a [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage). El método **GetPage** devuelve un identificador a la página, que se puede usar para mostrar la página solicitada.

> [!Note]  
> En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.

 

En el procedimiento siguiente se describe cómo crear un nuevo desencadenador.

**Para crear un nuevo desencadenador**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").
3.  Llame a **ITask:: QueryInterface** para recuperar la interfaz [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) y [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) para recuperar la página.
4.  Con el identificador de página devuelto, muestre la página.



| Para obtener un ejemplo de código de                                   | Vea                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Recuperar y mostrar la página de tareas de una tarea conocida | [Recuperación de una página de tareas](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 