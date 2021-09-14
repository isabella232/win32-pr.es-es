---
title: Ejemplo de enumeración de tareas
description: Para enumerar las tareas, debe llamar a ITaskScheduler Enum para crear un objeto de enumeración. A continuación, use la interfaz IEnumWorkItems del objeto de enumeración para enumerar las tareas de la carpeta Tareas programadas.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068666"
---
# <a name="enumerating-tasks-example"></a>Ejemplo de enumeración de tareas

Para enumerar las tareas, debe llamar a [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para crear un objeto [*de enumeración*](e.md). A continuación, use la interfaz [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) del objeto de enumeración para enumerar las tareas de la carpeta Tareas programadas.

En el procedimiento siguiente se describe cómo enumerar las tareas en la carpeta Tareas programadas.

**Para enumerar las tareas en la carpeta Tareas programadas**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto . (En este ejemplo se supone que el Programador de tareas se está ejecutando).
2.  Llame [**a ITaskScheduler::Enum para**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) obtener un objeto de enumeración.
3.  Llame [**a IEnumWorkItems::Next para**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) recuperar las tareas. (En este ejemplo se intenta recuperar cinco tareas con cada llamada).
4.  Procese las tareas devueltas. (Este ejemplo simplemente imprime el nombre de cada tarea en la pantalla.
5.  Liberar recursos. Llame [**a CoTaskMemFree para**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) liberar la memoria usada para los nombres.



| Para obtener un ejemplo de código de                                                         | Vea                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Enumeración de todas las tareas de la carpeta Tareas programadas del equipo local | [Ejemplo de código de C/C++: Enumeración de tareas](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 